**🔍 ZOOM: PRODUCT_MAP → MVP Rules & Constraints**


# Opportunity Navigator - MVP Specification

**Version:** 1.0
**Last Updated:** January 2026

---

## MVP Goal

Validate that people will use an AI-guided system to understand options AND accept community help without shame.

**Core Hypothesis:**
1. People trust AI to explain options without judgment
2. Community help feels justified when framed as "temporary bridge"
3. Small amounts prevent spirals better than nothing
4. Trust tracking (community credit) incentivizes reliability

---

## Minimum Viable Ecosystem

**To validate:** ~100 users, ~30-40 helpers, ~20-30 requests/month

**Proves:**
- People ask for help
- People offer help
- People follow through
- System holds without bailouts

---

## MVP Features (Must-Have)

### 1. AI Opportunity Navigator

| Feature | Specification |
|---------|---------------|
| **Chat Interface** | Text-based conversation |
| **Need Input** | User describes situation in plain language |
| **Clarifying Questions** | AI asks up to 5 questions |
| **Program Matching** | Show 3-5 likely programs with timelines |
| **Gap Detection** | "That takes 2-6 weeks, doesn't solve today" |
| **Community Bridge Offer** | "Would you like to see community help options?" |

**AI Constraints:**
- Does NOT approve benefits
- Does NOT give legal/financial advice
- Does NOT promise outcomes
- DOES explain honestly

### 2. Community Bridge (Peer Support)

| Feature | Specification |
|---------|---------------|
| **Request Form** | Specific need, amount (if cash), timeframe |
| **Helper Matching** | Algorithm matches by geography + capacity |
| **Helper Choice** | Form (time/items/cash), visibility (anon/visible), expectation (gift/repay/forward) |
| **No Public Display** | Requests never shown publicly |
| **Status Tracking** | "Matched" → "Fulfilled" → "Resolved" |

**Helper Options:**
- **Form:** Time, Items, Cash ($10-$25), Access
- **Visibility:** Anonymous, First name, Full profile
- **Expectation:** Gift, Repay when able, Pay it forward

### 3. Continuity Reserve (Last Resort)

| Feature | Specification |
|---------|---------------|
| **Access Criteria** | No active reserve, community match failed, urgent need |
| **Amount:** | $10-$25 (small amounts only) |
| **Window:** | 48-72 hours |
| **No Interest:** | Zero fees, zero interest |
| **One at a Time:** | Only 1 active reserve per user |

**Trigger:** After community match attempt fails + user confirms urgency.

### 4. Community Credit System

| Feature | Specification |
|---------|---------------|
| **Track Capacity** | Total value of help given (time, items, cash) |
| **Track Reliability** | Follow-through rate, timeliness, resolution |
| **Private Score** | Not public, only user + system see |
| **Unlock Benefits** | Priority matching, longer reserve windows, fewer cooldowns |

**Credits Earned:**
- Give time: +10 per hour
- Give items: +value estimate
- Give cash: +$1 per dollar
- Resolve cleanly: +50 bonus
- Repay reserve: +25 bonus

### 5. User Management

| Feature | Specification |
|---------|---------------|
| **Sign Up** | Email + password (simple auth) |
| **Profile** | Name, location (zip), verified phone |
| **Helper Profile** | Mark yourself as helper, set capacity limits |
| **Request History** | View past requests + outcomes |

---

## Out of Scope for MVP

- ❌ Mobile app (web-first)
- ❌ Nonprofit partnerships (manual for MVP)
- ❌ Document uploads
- ❌ Full benefits applications
- ❌ Social feeds
- ❌ Push notifications
- ❌ In-app messaging (email-based for MVP)
- ❌ Public leaderboards
- ❌ Advanced analytics

---

## User Flows

### Flow 1: First-Time User (Needs Help)

```
1. User lands on site, clicks "Get Help"
2. AI: "What do you need help with?"
3. User: "I'm short on rent, need $150"
4. AI asks clarifying questions:
   - When is rent due?
   - Have you looked into rental assistance?
   - Are you working currently?
5. AI shows programs:
   - County Rental Assistance (2-4 weeks)
   - Salvation Army Emergency Aid (1-2 weeks)
   - 211 Referral Service (immediate)
6. AI: "Those take time. Would you like community help today?"
7. User: "Yes"
8. User fills request form (need: $150, urgent, rent due in 3 days)
9. System matches with helpers
10. Helper accepts (offers $50 as gift)
11. 2 more helpers match ($50 each)
12. Total: $150 raised
13. User receives funds → resolves rent
14. User marks "Resolved" → helpers notified
```

### Flow 2: First-Time Helper

```
1. User signs up, clicks "I Want to Help"
2. Sets helper profile:
   - Willing to give: Time, Items, Cash (up to $50/month)
   - Geographic range: 10 miles
   - Preferred categories: Families, Kids, Emergencies
3. System notifies when match available
4. Helper sees request: "Single mom needs $50 for groceries"
5. Helper chooses:
   - Form: Cash ($50)
   - Visibility: First name only
   - Expectation: Pay it forward
6. Clicks "I'll Help"
7. Payment sent via Stripe → user receives
8. Helper earns +50 community credit
9. 2 weeks later, user marks "Paid Forward" (helped someone else)
10. Helper earns +25 bonus credit
```

### Flow 3: Continuity Reserve (Last Resort)

```
1. User requests help, no community match after 24 hours
2. System: "We couldn't find a match. Continuity Reserve available."
3. User: "I need $25 for gas to get to work"
4. System checks:
   - No active reserve ✓
   - Urgent need ✓
   - First-time or good history ✓
5. Approved: $25 for 72 hours
6. User receives funds immediately
7. Day 3: User pays back (voluntary) → +25 credit
8. Reserve pool replenished
```

---

## Technical Requirements

### Platform
- **Web app** (responsive mobile design)
- **AI:** OpenAI API or Claude for conversational navigator
- **Payments:** Stripe for helper contributions + reserve
- **Matching Algorithm:** Geography + capacity + reliability

### Performance
| Metric | Target |
|--------|--------|
| AI response time | <3 seconds |
| Matching speed | <10 minutes |
| Payment processing | <1 minute |
| Mobile responsive | iOS + Android browsers |

---

## Success Metrics

### Leading Indicators (First 3 months)

| Metric | Target |
|--------|--------|
| Users signed up | 100+ |
| Helpers enrolled | 30-40 |
| Requests submitted | 20-30/month |
| Community matches | 15+ per month |
| Match fulfillment rate | 70%+ |
| Reserve usage | <5 per month (last resort) |
| Repayment rate | 80%+ (voluntary) |

### Qualitative Metrics

- **User Feedback:** "Didn't feel like begging"
- **Helper Feedback:** "Felt good to help directly"
- **Trust:** "System felt fair"
- **No Complaints:** About harassment or shaming

---

## MVP Timeline

| Phase | Duration | Tasks |
|-------|----------|-------|
| **Development** | 8-10 weeks | AI navigator, matching, payments, credit system |
| **Beta Testing** | 3-4 weeks | 20-30 testers (split: helpers + needers) |
| **Launch** | 1 week | Public launch with monitoring |

**Total:** 12-15 weeks from start to launch

---

## MVP Exit Criteria

- [ ] 100+ users (50 helpers, 50 needers)
- [ ] 20+ successful community matches
- [ ] 70%+ fulfillment rate
- [ ] 80%+ voluntary repayment (reserve)
- [ ] No system liquidity issues
- [ ] Positive user sentiment
- [ ] Clear data on trust/reliability correlation

**If criteria met:** Proceed to Phase 2 (nonprofit partnerships, scale)
**If not met:** Iterate on matching algorithm, trust system

---

## Risk Mitigation

| Risk | Mitigation |
|------|------------|
| **No helpers sign up** | Pre-recruit helpers before launch |
| **System abuse** | Community credit gates access |
| **Reserve depletion** | Auto-tighten caps when low liquidity |
| **Legal issues** | Consult lawyer on micro-lending regulations |
| **Privacy concerns** | No public display of requests |

---

**The MVP proves people trust the system and that community help works.**
