# Opportunity Navigator

**AI Opportunity Navigator → Community Bridge → Continuity Reserve**

Help people understand what help exists, bridge short-term gaps with community support, and avoid financial free-fall when systems move too slowly.

---

## The Problem

Most people don't fail because they are irresponsible. They fail because:

- **Help exists but takes weeks** - Benefits, programs, resources have long processing times
- **Small issues interrupt work/school/stability** - $50 shortfall can spiral into crisis
- **Asking for help feels humiliating** - Public call-outs create shame
- **Financial tools punish** - Payday loans, overdraft fees, predatory lending
- **Fragmented systems don't talk** - Food banks, rent assistance, job programs operate in silos

**The Reality:** Most crises are **timing problems**, not money problems. Continuity matters more than cash.

---

## The Solution

Opportunity Navigator is a **three-layer system** that sits between crisis and collapse:

### Layer 1: AI Opportunity Navigator
**Purpose:** Clarity, dignity, trust | **Risk:** Zero

- User describes their need
- AI asks up to 5 clarifying questions
- Surfaces likely programs/resources
- Explains timelines honestly (2-6 weeks typical)
- Identifies gaps

**Key:** Honesty builds credibility. "This doesn't solve today" → opens door to Layer 2.

### Layer 2: Community Bridge
**Purpose:** Immediacy, human reliability | **Risk:** Low

- When AI finds a gap, offers community help options
- Peer-to-peer support (time, items, cash, access)
- Helper chooses: form (what), visibility (anonymous/visible), expectation (gift/repay/pay-forward)
- No public shaming, no harassment
- Tracking without pressure

**Forms of Help:**
- **Time:** Rides, errands, childcare swap
- **Items:** Tools, supplies, household goods
- **Cash:** Very small ($10-$25)
- **Access:** Introductions, know-how

### Layer 3: Continuity Reserve
**Purpose:** Prevent failure when peers can't help | **Risk:** Tightly controlled

- Very small amounts ($10-$25)
- Short windows (48-72 hours)
- One active use at a time
- No interest, no upfront fees
- Last resort only

**Not a loan fund.** It's a bridge to prevent collapse.

---

## Core Innovation

### Community Credit (The Glue)

**Community Credit is NOT money.** It's a private record of real contribution and reliability.

**Two Dimensions:**
1. **Capacity Extended** - How much support someone has given
2. **Reliability Demonstrated** - Follow-through, showing up, resolving cleanly

**What It Unlocks:**
- Priority when you need help
- Faster matching
- Longer continuity windows
- Fewer cooldowns
- Access to nonprofit grants (Phase 2)
- Partner matching pools (Phase 2)

**Key Principle:** No public scores, no leaderboards, no flexing. Private trust metric.

---

## Key Features

### 1. AI Navigator (Front Door)

| Feature | Description |
|---------|-------------|
| **Conversational UI** | User describes need in plain language |
| **Clarifying Questions** | Max 5 questions to understand situation |
| **Program Matching** | Surfaces benefits, resources, options |
| **Honest Timelines** | "This usually takes 2-6 weeks" |
| **Gap Detection** | "That doesn't solve today" → offers Community Bridge |

### 2. Community Bridge

| Feature | Description |
|---------|-------------|
| **Request Form** | Specific, short-term need |
| **Helper Matching** | Algorithm matches based on capacity + geography |
| **Helper Agency** | Helper chooses form, visibility, expectation |
| **No Harassment** | No public reminders, no shaming |
| **Systemic Consequences** | Access pauses, limits tighten quietly (no personal chase) |

### 3. Continuity Reserve

| Feature | Description |
|---------|-------------|
| **Small Amounts** | $10-$25 max |
| **Short Windows** | 48-72 hours |
| **One at a Time** | One active use per user |
| **No Interest** | Zero fees, zero interest |
| **Last Resort** | Only when community can't help |

### 4. Community Credit System

| Feature | Description |
|---------|-------------|
| **Private Score** | Not public, not shared |
| **Dual Tracking** | Capacity + reliability |
| **Unlock Benefits** | Priority, access, matching |
| **Nonprofit Integration** | Partner grants for high-credit users |

---

## Target Users

### Primary
- **Budget-Constrained Individuals** - Living paycheck-to-paycheck
- **Crisis-Facing Households** - Temporary setbacks (car repair, medical bill)
- **Underbanked/Unbanked** - No access to traditional credit

### Secondary
- **Community Helpers** - People who want to help neighbors in crisis
- **Nonprofits** - Organizations seeking to distribute aid effectively
- **Employers** - Companies offering employee financial wellness

---

## Why This Works

| User Benefit | System Benefit |
|--------------|----------------|
| **Clarity on options** | Reduces 311 calls, case worker load |
| **Peer support feels justified** | Builds trust, not dependency |
| **Last-resort safety net** | Prevents spiral into predatory loans |
| **Community credit** | Rewards helpers, incentivizes reliability |
| **No public shaming** | Preserves dignity |

---

## Business Model

### Revenue (Reinvested, Not Extracted)

| Stream | Description |
|--------|-------------|
| **Optional Membership** | $3-$5/month (not required) |
| **Post-Resolution Fee** | Small fee (e.g., $0.50) after help received |
| **Round-Ups** | Optional spare change donations |
| **Partner Matching** | Dollar-for-dollar matching from sponsors |

**Key Principle:** No one pays to ask for help. Revenue supports the system, not profit extraction.

### Reserve Funding

- Platform fees (reinvested)
- Recycled repayments (voluntary)
- Partner matching pools (Phase 2)

**Auto-Protection:** System tightens automatically when liquidity drops (smaller caps, helper-first routing, temporary pauses).

---

## Market Opportunity

- **US households lacking emergency savings:** 32% have $0, median is $500
- **Households unable to cover $400 emergency:** 29%
- **Market need:** 55M budget-conscious households
- **Social lending proof:** SoLo Funds funded $250M+ with 94% repayment rate

**Gap:** No platform combines AI guidance, community support, and micro-credit in one dignified system.

---

## Competitive Advantages

| Advantage | Defensibility |
|-----------|---------------|
| **Three-layer system** | Very High (unique combination) |
| **Community credit** | High (data moat) |
| **Nonprofit partnerships** | High (trust layer) |
| **No predatory framing** | High (ethical moat) |
| **Trust portability** | Medium (can be copied) |

---

## Technology Stack

- **Frontend:** React + TypeScript
- **Backend:** Python + FastAPI
- **Database:** PostgreSQL + Redis
- **AI:** OpenAI API or Claude for conversational navigator
- **Payments:** Stripe (for optional fees)
- **Matching Algorithm:** Custom (geography + capacity + reliability)

---

## Legal & Ethical Design

**Non-negotiable constraints:**
- ❌ No predatory fees
- ❌ No public shaming
- ❌ No hidden terms
- ❌ No aggressive collection
- ❌ No selling data

**Core principle:** Dignity-first design. Help people, don't exploit them.

**See:** [RISK_MANAGEMENT.md](./RISK_MANAGEMENT.md) for full risk analysis.

---

## Getting Started

This repository contains comprehensive documentation:

| Document | Description |
|----------|-------------|
| [FEATURES.md](./FEATURES.md) | Detailed feature specifications |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Technical design and system architecture |
| [ROADMAP.md](./ROADMAP.md) | Phased implementation plan with timelines |
| [MVP_SPEC.md](./MVP_SPEC.md) | Minimum viable product definition |
| [MARKET_ANALYSIS.md](./MARKET_ANALYSIS.md) | Market research and competitive analysis |
| [RISK_MANAGEMENT.md](./RISK_MANAGEMENT.md) | Financial risk controls and safeguards |

---

## Status

**Phase:** Documentation and Planning
**Next Milestone:** MVP Development + Legal/Compliance Review

---

## One-Line Test

If this sentence makes sense, the system is aligned:

> "We help people understand their options, bridge short-term gaps through community support, and protect continuity—and the system sustains itself through reinvested value."

---

**Clarity. Community. Continuity.**
