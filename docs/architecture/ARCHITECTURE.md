**🔍 ZOOM: PRODUCT_MAP → Data Models & Technical Stack**


# Opportunity Navigator - Technical Architecture

**Version:** 1.0
**Last Updated:** January 2026

---

## Technology Stack

### Frontend
- **Framework:** React + TypeScript
- **UI:** Tailwind CSS
- **State:** Zustand
- **Build:** Vite

### Backend
- **Framework:** Python + FastAPI
- **Database:** PostgreSQL
- **Cache:** Redis (sessions, matching queue)
- **AI:** OpenAI API or Claude (conversational navigator)
- **Payments:** Stripe (helper→user transfers, reserve)
- **Task Queue:** Celery (background jobs)

### Infrastructure
- **Hosting:** Vercel (frontend) + Railway (backend)
- **Monitoring:** Sentry (errors) + PostHog (analytics)
- **Email:** Resend

---

## Data Models

### Core Tables

**users**
- id, email, password_hash, name, phone (verified), zip_code, role (user/helper/both)

**requests**
- id, user_id, need_description, amount (if cash), timeframe, category, status, created_at

**matches**
- id, request_id, helper_id, form (time/items/cash/access), visibility, expectation, status

**community_credit**
- user_id, capacity_extended, reliability_score, total_credits, last_updated

**reserve_transactions**
- id, user_id, amount, window_end, repaid (boolean), repaid_at

**helper_profiles**
- user_id, max_monthly_cash, max_radius_miles, preferred_categories (array)

---

## API Design

### AI Navigator
- POST `/api/navigator/chat` (send message → AI response)
- GET `/api/navigator/programs` (get matched programs)

### Community Bridge
- POST `/api/requests/create` (submit help request)
- GET `/api/requests/status/:id` (check status)
- GET `/api/matches/available` (helpers see available matches)
- POST `/api/matches/accept` (helper accepts match)

### Continuity Reserve
- POST `/api/reserve/request` (request reserve access)
- POST `/api/reserve/repay` (voluntary repayment)

### Community Credit
- GET `/api/credit/:userId` (get credit score)
- POST `/api/credit/award` (award credits for action)

---

## Matching Algorithm

```python
def match_request(request_id):
    request = get_request(request_id)

    # Filter helpers by:
    # 1. Geographic proximity
    helpers = filter_by_zip(request.zip_code, radius_miles=25)

    # 2. Capacity available
    helpers = filter_by_capacity(helpers, request.amount)

    # 3. Category alignment
    helpers = filter_by_category(helpers, request.category)

    # 4. Sort by community credit (priority)
    helpers = sort_by_credit(helpers, descending=True)

    # Notify top 5 helpers
    notify_helpers(helpers[:5], request)
```

---

## Reserve Liquidity Management

```python
def check_reserve_liquidity():
    liquidity_pct = get_reserve_balance() / get_reserve_target()

    if liquidity_pct < 0.30:
        # Pause new reserves, helper-only routing
        set_reserve_status("paused")
        max_amount = 0
    elif liquidity_pct < 0.50:
        # Minimal caps
        max_amount = 10
    elif liquidity_pct < 0.70:
        # Reduced caps
        max_amount = 15
    else:
        # Normal operations
        max_amount = 25

    update_reserve_caps(max_amount)
```

---

## Security

- HTTPS only
- JWT authentication
- bcrypt password hashing
- Phone verification (Twilio)
- Input validation (Pydantic)
- Rate limiting (100 req/min)
- No public request display

---

## Performance Targets

| Metric | Target |
|--------|--------|
| AI response time | <3s |
| Matching speed | <10 minutes |
| Payment processing | <1 minute |
| Page load | <2s |

---

**Simple, secure, sustainable.**
