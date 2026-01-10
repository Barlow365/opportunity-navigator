# Opportunity Navigator - SITEMAP

**🔍 ZOOM: PRODUCT_MAP → Navigation & Entry**

This document expands on `docs/PRODUCT_MAP.md`:
- **Parent Section**: Navigation & Entry + All Routes
- **Purpose**: Complete route structure with authentication, layouts, and three-layer system mapping
- **Binding**: All routes described here MUST exist in PRODUCT_MAP first

**Navigation**: [README](../../README.md) → [PRODUCT_MAP](../PRODUCT_MAP.md) → This Document

---

## Site Architecture Overview

**Route Pattern**: Public routes at root level, authenticated app routes under `/navigator`, `/request`, `/reserve`, etc.

**Total Routes**: 12 pages

**Three-Layer System**:
- **Layer 1** (AI Navigator): `/navigator`
- **Layer 2** (Community Bridge): `/request`, `/helper-preferences`
- **Layer 3** (Continuity Reserve): `/reserve`

---

## Complete Route Map

```
opportunity-navigator.com/
│
├── PUBLIC ROUTES (Marketing)
│   ├── /                           → Home / Landing Page
│   ├── /how-it-works               → Three-Layer System Explained
│   ├── /features                   → Features Overview
│   ├── /privacy                    → Privacy Policy
│   └── /terms                      → Terms of Service
│
├── AUTH ROUTES (Unauthenticated)
│   ├── /login                      → Sign In
│   └── /signup                     → Create Account
│
├── APP ROUTES (Authenticated)
│   ├── /navigator                  → Layer 1: AI Conversational Navigator
│   ├── /request                    → Layer 2: Community Bridge Request Form
│   ├── /request/:requestId         → Request Status & Matching
│   ├── /reserve                    → Layer 3: Continuity Reserve Application
│   ├── /reserve/:reserveId         → Reserve Status Tracking
│   ├── /community-credit           → Community Credit Dashboard
│   ├── /helper-preferences         → Helper Capacity & Matching Preferences
│   └── /settings                   → User Settings
│
└── HELP
    └── /help                       → Help / FAQ / Support
```

---

## Route Specifications

### 1. PUBLIC ROUTES (Marketing)

#### `/` - Home / Landing Page

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: First impression, value proposition, CTA to sign up

**Layout**: Marketing layout (header, hero, 3-layer explanation, footer)

**Key Elements**:
- Hero: "Clarity. Community. Continuity."
- Tagline: "Help people understand what help exists, bridge short-term gaps with community support, and avoid financial free-fall when systems move too slowly."
- **The Problem**: Most crises are TIMING problems, not money problems
- **The Solution**: 3-layer system visual (AI Navigator → Community Bridge → Continuity Reserve)
- CTA: [Get Started Free]

**Auth State**:
- If logged in → redirect to `/navigator`
- If not logged in → show landing page

---

#### `/how-it-works` - Three-Layer System Explained

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Explain the three-layer system in detail

**Layout**: Marketing layout

**Key Sections**:

**Layer 1: AI Opportunity Navigator**
- Purpose: Clarity, dignity, trust
- Risk: Zero
- What it does: Surfaces programs, honest timelines, identifies gaps
- Example: "Apply to ERAP, but it takes 4-6 weeks. Need help now?"

**Layer 2: Community Bridge**
- Purpose: Immediacy, human reliability
- Risk: Low (community-sized)
- What it does: Peer-to-peer support (time, items, cash, access)
- Helper agency: form, visibility, expectation
- Example: "Jordan offers $25 gas money as a gift"

**Layer 3: Continuity Reserve**
- Purpose: Prevent failure when peers can't help
- Risk: Tightly controlled (last resort)
- What it does: Very small amounts ($10-$25), short windows (48-72h)
- Example: "No community match after 24h → reserve eligible"

**Community Credit**:
- Two dimensions: Capacity Extended + Reliability Demonstrated
- Unlocks: Priority matching, longer windows, fewer cooldowns
- Private (no public scores)

**Visuals**: Step-by-step flow diagrams, layer interaction

---

#### `/features` - Features Overview

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Feature grid highlighting three-layer innovations

**Key Features Displayed**:

**Layer 1 Features**:
- Conversational AI navigator
- Max 5 clarifying questions
- Honest timelines (2-6 weeks typical)
- Program matching
- Gap detection

**Layer 2 Features**:
- Helper matching algorithm
- Four forms of help (Time, Items, Cash, Access)
- Helper agency (form, visibility, expectation)
- No public shaming
- Systemic consequences (not personal chase)

**Layer 3 Features**:
- Very small amounts ($10-$25)
- Short windows (48-72h)
- One active use at a time
- No interest, no fees
- Last resort only

**Community Credit Features**:
- Private score
- Dual-dimensional (capacity + reliability)
- Unlocks benefits
- Never public

**CTA**: [Sign Up Free]

---

#### `/privacy` - Privacy Policy

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Legal compliance, user data handling

**Key Points**:
- What data we collect (need descriptions, location, payment info)
- How we use it (matching, credit calculation, reserve eligibility)
- Who we share it with (helpers - only when matched, anonymously if preferred)
- User rights (GDPR, CCPA)
- Community Credit privacy (NEVER shared publicly)

**Critical**: Dignity-first design, no selling data, no public shaming

---

#### `/terms` - Terms of Service

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Legal terms, user agreement

**Key Points**:
- NOT a loan (Continuity Reserve is a micro-credit safety net)
- User responsibilities (honest representation, good faith use)
- Helper responsibilities (follow through, no harassment)
- Account termination (abuse, fraud)
- Liability limits
- Dispute resolution

---

### 2. AUTH ROUTES (Unauthenticated)

#### `/login` - Sign In

**PRODUCT_MAP Reference**: Navigation & Entry → Auth Routes

**Purpose**: Existing user login

**Layout**: Centered auth form

**Form Fields**:
- Email (required)
- Password (required)
- "Remember me" checkbox
- "Forgot password?" link

**Actions**:
- [Sign In] → POST `/api/auth/login` → redirect to `/navigator`
- "Don't have an account?" → `/signup`

**Validation**:
- Email format
- Password minimum 8 chars

---

#### `/signup` - Create Account

**PRODUCT_MAP Reference**: Navigation & Entry → Auth Routes

**Purpose**: New user registration

**Layout**: Centered auth form

**Form Fields**:
- Name (required)
- Email (required)
- Phone (optional, recommended for SMS notifications)
- Password (required, min 8 chars)
- Confirm Password (required, must match)
- Location (City, State, ZIP) - required for helper matching

**Actions**:
- [Create Account] → POST `/api/auth/register` → redirect to `/navigator`
- "Already have an account?" → `/login`

**Validation**:
- Email unique
- Password strength
- ZIP code format

**Privacy Note**: "We use your location to match you with nearby helpers. We never share your address publicly."

---

### 3. APP ROUTES (Authenticated)

#### `/navigator` - Layer 1: AI Opportunity Navigator

**PRODUCT_MAP Reference**: LAYER 1: AI OPPORTUNITY NAVIGATOR

**Purpose**: Conversational AI to help users find resources and identify gaps

**Layout**: App layout with chat interface

**Interface**:

**Chat Window**:
```
┌──────────────────────────────────────┐
│ AI: Hi! I'm here to help you find   │
│     resources. What do you need help │
│     with?                            │
│                                      │
│ USER: I'm behind on rent             │
│                                      │
│ AI: I understand. Let me ask a few  │
│     questions... (1/5)               │
└──────────────────────────────────────┘

[Type your message...]  [Send]
```

**Conversation Flow**:
1. AI asks up to 5 clarifying questions
2. AI surfaces 3-5 programs with:
   - Eligibility requirements
   - Amount/support offered
   - Honest timeline (e.g., "4-6 weeks typical")
   - Application links
3. AI identifies gap: "These programs take 2-6 weeks. That doesn't solve today. Would you like community help?"
4. User can:
   - [Yes, Show Community Options] → `/request`
   - [No, I'm Good]
   - [Start New Search]

**Key Features**:
- Max 5 questions (no infinite loops)
- Honest timelines (no false hope)
- Gap detection (opens door to Layer 2)
- Export results

**Empty State**: "What do you need help with?"

---

#### `/request` - Layer 2: Community Bridge Request Form

**PRODUCT_MAP Reference**: LAYER 2: COMMUNITY BRIDGE

**Purpose**: Submit request for community help

**Layout**: App layout with multi-step form

**Form Sections**:

**Section 1: What Do You Need?**
- Describe your need (textarea, 500 char max)
- Example: "Need $25 for gas to get to work interviews this week"
- Amount needed (if cash): [$_____] (Max $25)
- Timeframe: [48 hours v] [72 hours] [1 week]

**Section 2: Category**
- ○ Time (rides, errands, childcare)
- ○ Cash ($10-$25)
- ○ Items (tools, supplies, household goods)
- ○ Access (introductions, know-how)

**Section 3: Matching Preferences**
- Geographic range: ○ Neighborhood ○ City ○ County ○ State
- Visibility: ○ Anonymous (helper sees need, not your name) ○ Visible (share my name)

**Section 4: Expectations**
- What's your intent?
  - ○ Gift (no expectation to repay)
  - ○ Repay when stable (informal, no deadline)
  - ○ Pay forward (help someone else later)

**Review & Submit**:
- Display all entered information
- "Your request will be shared with community members who have capacity."
- "If no one can help within 24 hours, you may be eligible for Continuity Reserve."
- [Cancel] [Submit Request]

**Validation**:
- Need description required
- Amount ≤ $25 if cash
- At least one category selected

**On Submit**: → `/request/:requestId`

---

#### `/request/:requestId` - Request Status & Matching

**PRODUCT_MAP Reference**: LAYER 2: COMMUNITY BRIDGE → Matching

**Purpose**: Track request status, view match results

**Layout**: App layout

**States**:

**State 1: Waiting for Match** (no match yet)
```
┌──────────────────────────────────────┐
│ YOUR REQUEST IS ACTIVE               │
│                                      │
│ Status: [>] Waiting for helper match │
│ Posted: 2 hours ago                  │
│ Expires: In 22 hours (if no match)   │
│                                      │
│ What you requested:                  │
│ "$25 for gas for work interviews"    │
│                                      │
│ ████████░░░░░░░░ Searching...        │
│ (8 helpers notified)                 │
└──────────────────────────────────────┘

[Cancel Request]
```

**State 2: Matched** (helper found)
```
┌──────────────────────────────────────┐
│ MATCHED! 🎉                          │
│                                      │
│ Helper: Jordan M. (High Credit)      │
│ Offering: $25 cash                   │
│ Visibility: Anonymous (shared name)  │
│ Expectation: Gift                    │
│                                      │
│ Jordan says: "I've been there. Hope  │
│ this helps with the interviews!"     │
│                                      │
│ [Message Jordan] [Confirm Receipt]   │
└──────────────────────────────────────┘
```

**State 3: No Match (24h elapsed)**
```
┌──────────────────────────────────────┐
│ NO MATCH FOUND                       │
│                                      │
│ We couldn't find a community helper  │
│ within 24 hours.                     │
│                                      │
│ You may be eligible for Continuity   │
│ Reserve (last resort).               │
│                                      │
│ [Apply for Reserve]                  │
│ [Cancel Request]                     │
└──────────────────────────────────────┘
```

**State 4: Fulfilled**
```
┌──────────────────────────────────────┐
│ FULFILLED ✓                          │
│                                      │
│ Jordan helped you on [date]          │
│                                      │
│ Thank you note (optional):           │
│ [_____________________________]      │
│                                      │
│ [Send Thank You]                     │
└──────────────────────────────────────┘
```

**Actions**:
- Cancel request (anytime before match)
- Message helper (after match)
- Confirm receipt (triggers Community Credit for helper)
- Mark as resolved (if solved independently)

---

#### `/helper-preferences` - Helper Capacity & Matching Preferences

**PRODUCT_MAP Reference**: LAYER 2: COMMUNITY BRIDGE → Helper Features

**Purpose**: Set helper capacity, forms of help, matching preferences

**Layout**: App layout with form sections

**Sections**:

**Section 1: Monthly Capacity**
```
How much can you offer per month?

Cash: [$___50___] (Recommended: $25-$100)
Time: [___5___] hours per month

Used this month: $25 cash | 2 hours
Remaining: $25 cash | 3 hours
```

**Section 2: Forms of Help**
```
What forms of help can you offer? (Select all)

[X] Time (rides, errands, childcare swap)
[X] Cash ($10-$25)
[X] Items (tools, supplies, household goods)
[ ] Access (introductions, know-how)
```

**Section 3: Matching Preferences**
```
Geographic range: How far can you help?
○ Neighborhood  ● City  ○ County  ○ State

Visibility: How do you want to appear?
○ Anonymous (need doesn't see your name)
● Visible (share my name with requester)

Expectation default:
● Gift (no repayment expected)
○ Repay when stable
○ Pay forward

(You can change this per-request)
```

**Section 4: Notification Preferences**
```
How often do you want to be notified?

● Daily digest (1 email per day with all new requests)
○ Immediate (as requests come in)
○ Weekly summary
```

**Actions**:
- [Save Preferences]
- [Activate Helper Status]
- [Pause Helper Status]

**Community Credit Display**:
- "Your Community Credit: 145 points (High)"
- "Capacity Extended: $120 (3 helps)"
- "Reliability: 100% (all 3 resolved cleanly)"

---

#### `/reserve` - Layer 3: Continuity Reserve Application

**PRODUCT_MAP Reference**: LAYER 3: CONTINUITY RESERVE

**Purpose**: Apply for micro-credit safety net (last resort)

**Layout**: App layout with application form

**Eligibility Check** (shown at top):
```
Requirements:
✓ Community match failed (24h elapsed)
✓ No active reserve use
✓ Urgent need confirmed
✓ Community Credit > 50 points (you have 145)
```

**Application Form**:

**Section 1: Request Summary**
- Your request: [pulled from failed request]
- Status: No community match after 24 hours

**Section 2: Reserve Amount**
- Reserve amount requested: [$___25___] (Max $25)

**Section 3: Urgency**
- Why is this urgent? (textarea)
- Example: "I have 3 job interviews this week. Without gas, I can't get there."

**Section 4: Expected Resolution**
- How will you resolve this?
  - ○ Paycheck on [date] (X days)
  - ○ Benefit payment expected (5-7 days)
  - ○ Other: [___________________]

**Review & Submit**:
```
Reserve terms:
- Amount: $25
- Window: 72 hours (expected resolution: 3 days)
- No interest, no fees
- Voluntary repayment when stable (no forced collection)
- If not resolved: Access pauses, limits tighten (no personal chase)

[Cancel] [Submit Application]
```

**Validation**:
- Amount ≤ $25
- Urgency explanation required
- Expected resolution date required

**On Submit**: → `/reserve/:reserveId`

---

#### `/reserve/:reserveId` - Reserve Status Tracking

**PRODUCT_MAP Reference**: LAYER 3: CONTINUITY RESERVE → Reserve Status

**Purpose**: Track active reserve, resolution progress

**Layout**: App layout

**States**:

**State 1: Pending Approval**
```
┌──────────────────────────────────────┐
│ RESERVE APPLICATION PENDING          │
│                                      │
│ We're reviewing your application.    │
│ Typical response: 2-4 hours          │
│                                      │
│ Amount requested: $25                │
└──────────────────────────────────────┘
```

**State 2: Active Reserve**
```
┌──────────────────────────────────────┐
│ ACTIVE RESERVE                       │
│                                      │
│ Amount: $25                          │
│ Received: Today                      │
│ Window: 72 hours (expires in 71h)    │
│ Expected resolution: Paycheck (2 days)│
│                                      │
│ PROGRESS TRACKER:                    │
│ Day 1: ●●●●●●●●●●●●●● (You are here) │
│ Day 2: ○○○○○○○○○○○○○○                │
│ Day 3: ○○○○○○○○○○○○○○ (Paycheck)     │
│                                      │
│ [Mark as Resolved]                   │
│ [Voluntary Repayment]                │
│ [Need Extension]                     │
└──────────────────────────────────────┘
```

**State 3: Resolved**
```
┌──────────────────────────────────────┐
│ RESOLVED ✓                           │
│                                      │
│ Reserve resolved on [date]           │
│ Resolution: Early (1 day ahead)      │
│                                      │
│ Community Credit earned: +25 bonus   │
│ (for early resolution)               │
└──────────────────────────────────────┘
```

**State 4: Extended/Expired**
- Shows extension request status
- If expired: "Access paused. Reach out when stable to restore access."

**Actions**:
- Mark as resolved (when need is met)
- Voluntary repayment (when stable)
- Request extension (if needed)

---

#### `/community-credit` - Community Credit Dashboard

**PRODUCT_MAP Reference**: COMMUNITY CREDIT SYSTEM

**Purpose**: View Community Credit score, history, unlocked benefits

**Layout**: App layout

**Display**:

**Section 1: Your Score**
```
┌──────────────────────────────────────┐
│ YOUR COMMUNITY CREDIT                │
│                                      │
│ Score: 145 points (High)             │
│                                      │
│ Capacity Extended: 120 pts ████████░ │
│ Reliability:        25 pts ███░░░░░░ │
│                                      │
│ Private score. Never public.         │
└──────────────────────────────────────┘
```

**Section 2: How You Earned It**
```
CAPACITY EXTENDED (what you've given)
[X] Helped Jordan with $25 gas        +$25 | 2 days ago
[X] Gave ride to Sarah for interview  +10 hrs | 1 week ago
[X] Loaned tools to Alex              +15 pts | 2 weeks

RELIABILITY DEMONSTRATED (how well you followed through)
[X] All 3 helps resolved cleanly      +50 bonus
[X] Repaid reserve early (2 days)     +25 bonus
```

**Section 3: What It Unlocks**
```
Your Community Credit unlocks:
✓ Priority matching (matched first when you need help)
✓ Longer reserve windows (72h instead of 48h)
✓ Fewer cooldowns (request again sooner)
✓ Access to nonprofit grants (Phase 2 - coming soon)
```

**Section 4: Keep Building**
```
Ways to earn more:
- Help community members (capacity extended)
- Resolve requests cleanly (reliability demonstrated)
- Repay reserves early (reliability bonus)
- Pay forward (help someone after being helped)
```

**Privacy Notice**: "Community Credit is PRIVATE. No public scores, leaderboards, or flexing."

---

#### `/settings` - User Settings

**PRODUCT_MAP Reference**: Settings

**Purpose**: Account, location, privacy, notifications

**Layout**: App layout with sidebar tabs

**Tabs**:

**1. Account**:
- Name
- Email (change email)
- Phone
- Password (change password)
- Delete account (danger zone)

**2. Location**:
- City
- State
- ZIP
- "Used for matching helpers in your area"

**3. Privacy**:
- Profile Visibility: ○ Public ● Private
- Community Credit Visibility: ● Private (never shared publicly)
- [ ] Share Community Credit with helpers when requesting

**4. Notifications**:
- Email Notifications:
  - [X] Request matched
  - [X] Reserve approved/denied
  - [X] Community Credit milestones
  - [ ] Weekly summary
- SMS Notifications (optional):
  - [ ] Critical updates only

**5. Data**:
- Export data (GDPR compliance)
- Delete all data (CCPA compliance)

**Actions**:
- [Save Changes]
- [Deactivate Account]

**Privacy Note**: "Community Credit will be preserved for 6 months if you deactivate."

---

### 4. HELP

#### `/help` - Help / FAQ / Support

**PRODUCT_MAP Reference**: System → Help

**Purpose**: User support, FAQs, contact

**Layout**: Marketing/app hybrid layout

**Sections**:

**FAQs**:
- "How does the three-layer system work?" → Layer 1/2/3 explanation
- "Is this a loan?" → NO (detailed explanation)
- "What is Community Credit?" → Private score, dual-dimensional
- "Can helpers see my personal info?" → Only if you choose "Visible"
- "What happens if I can't repay a reserve?" → Access pauses (no collection)
- "How do I become a helper?" → `/helper-preferences`

**Contact Support**:
- Email form
- Response time: 24-48 hours

**System Status**:
- Uptime
- Incidents
- Maintenance windows

---

## Route Access Control

| Route | Authentication | Redirect If Logged In | Redirect If Not Logged In |
|-------|----------------|----------------------|---------------------------|
| `/` | Public | → `/navigator` | - |
| `/how-it-works` | Public | - | - |
| `/login` | Public | → `/navigator` | - |
| `/signup` | Public | → `/navigator` | - |
| `/navigator` | Required | - | → `/login` |
| `/request` | Required | - | → `/login` |
| `/request/:requestId` | Required | - | → `/login` |
| `/reserve` | Required | - | → `/login` |
| `/reserve/:reserveId` | Required | - | → `/login` |
| `/community-credit` | Required | - | → `/login` |
| `/helper-preferences` | Required | - | → `/login` |
| `/settings` | Required | - | → `/login` |
| `/help` | Public | - | - |

---

## Mobile Navigation

**Bottom Tab Bar** (authenticated app):
```
┌──────────┬──────────┬──────────┬──────────┐
│ Navigator│ Requests │ Credit   │ Settings │
│ 💬       │ 🤝       │ ⭐       │ ⚙️       │
└──────────┴──────────┴──────────┴──────────┘
```

Maps to:
- Navigator → `/navigator`
- Requests → `/request` (or active request if exists)
- Credit → `/community-credit`
- Settings → `/settings`

---

## URL Parameters & Query Strings

**Request Status**:
- `/request/abc123` - Dynamic request ID route

**Reserve Status**:
- `/reserve/xyz789` - Dynamic reserve ID route

**Navigator Preload**:
- `/navigator?preload=rent-assistance` - Pre-populate search with topic

**Helper Activation**:
- `/helper-preferences?activate=true` - Jump to activation step

---

## Feature Flags (All Routes)

**Phase-Based Routing** (controlled via environment variables):

```javascript
FEATURE_AI_NAVIGATOR=true          // Enable/disable Layer 1
FEATURE_COMMUNITY_BRIDGE=true      // Enable/disable Layer 2
FEATURE_CONTINUITY_RESERVE=true    // Enable/disable Layer 3
FEATURE_COMMUNITY_CREDIT=true      // Enable/disable credit system
FEATURE_NONPROFIT_GRANTS=false     // Phase 2 feature (disabled in MVP)
FEATURE_PARTNER_MATCHING=false     // Phase 2 feature (disabled in MVP)
```

---

## Route Summary Table

| # | Route | PRODUCT_MAP Section | Auth | Phase | Layer |
|---|-------|---------------------|------|-------|-------|
| 1 | `/` | Navigation & Entry | Public | MVP | - |
| 2 | `/how-it-works` | Navigation & Entry | Public | MVP | - |
| 3 | `/features` | Navigation & Entry | Public | MVP | - |
| 4 | `/privacy` | Navigation & Entry | Public | MVP | - |
| 5 | `/terms` | Navigation & Entry | Public | MVP | - |
| 6 | `/login` | Navigation & Entry | Public | MVP | - |
| 7 | `/signup` | Navigation & Entry | Public | MVP | - |
| 8 | `/navigator` | Layer 1: AI Navigator | Required | MVP | 1 |
| 9 | `/request` | Layer 2: Community Bridge | Required | MVP | 2 |
| 10 | `/reserve` | Layer 3: Continuity Reserve | Required | MVP | 3 |
| 11 | `/community-credit` | Community Credit System | Required | MVP | All |
| 12 | `/helper-preferences` | Layer 2: Helper Features | Required | MVP | 2 |
| 13 | `/settings` | Settings | Required | MVP | - |
| 14 | `/help` | Help | Public | MVP | - |

**Total MVP Routes**: 14 (12 unique + 2 dynamic: `:requestId`, `:reserveId`)

---

## API Endpoints (Route Support)

See `docs/architecture/ARCHITECTURE.md` for full API specifications.

**Quick Reference**:
- `/api/auth/*` - Authentication
- `/api/navigator/*` - AI conversational navigator
- `/api/requests/*` - Community Bridge requests
- `/api/helpers/*` - Helper matching & preferences
- `/api/reserves/*` - Continuity Reserve system
- `/api/credit/*` - Community Credit tracking

---

**For wireframes of each route, see [WIREFRAMES.md](./WIREFRAMES.md)**
