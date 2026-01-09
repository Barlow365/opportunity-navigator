# Opportunity Navigator - Features Guide

**Comprehensive Feature Specifications**

---

## Three-Layer System

### Layer 1: AI Opportunity Navigator

**Purpose:** Clarity, dignity, trust

**Features:**
- Conversational UI (text-based chat)
- Natural language input ("I'm short on rent")
- Clarifying questions (max 5)
- Program matching (benefits, resources, nonprofits)
- Honest timelines ("This takes 2-6 weeks")
- Gap detection ("That doesn't solve today")

**AI Constraints:**
- Does NOT approve benefits
- Does NOT give legal/financial advice
- Does NOT promise outcomes

### Layer 2: Community Bridge

**Purpose:** Immediacy, human reliability

**Request Features:**
- Specific need description
- Amount (if cash: $10-$25)
- Timeframe (urgent, 1 week, flexible)
- Category (housing, food, transportation, childcare)

**Helper Features:**
- Choose form: Time, Items, Cash, Access
- Choose visibility: Anonymous, First name, Full profile
- Choose expectation: Gift, Repay when able, Pay it forward
- Set monthly limits ($50 typical)
- Geographic range (5, 10, 25 miles)

**Matching Algorithm:**
- Geographic proximity
- Helper capacity available
- Category alignment
- Community credit score (priority)

### Layer 3: Continuity Reserve

**Purpose:** Last resort when community can't help

**Features:**
- Small amounts ($10-$25)
- Short windows (48-72 hours)
- One active use at a time
- No interest, zero fees
- Voluntary repayment

**Access Criteria:**
- No active reserve
- Community match failed after 24 hours
- Urgent need confirmed
- Community credit score > threshold

---

## Community Credit System

**Two Dimensions:**
1. **Capacity Extended:** Total value of help given
2. **Reliability Demonstrated:** Follow-through rate

**Credits Earned:**
- Give time: +10 per hour
- Give items: +value estimate
- Give cash: +$1 per dollar
- Resolve cleanly: +50 bonus
- Repay reserve: +25 bonus
- Pay it forward: +25 bonus

**Credits Unlock:**
- Priority matching
- Longer reserve windows
- Fewer cooldowns
- Nonprofit grant access (Phase 2)
- Partner matching pools (Phase 2)

**Display:** Private (only user sees their score)

---

## User Flows

### Flow 1: User Needs Help

```
1. User describes need to AI
2. AI asks clarifying questions
3. AI shows programs + timelines
4. AI identifies gap: "Doesn't solve today"
5. AI offers: "Would you like community help?"
6. User accepts → fills request form
7. System matches with helpers
8. Helper(s) accept → help provided
9. User marks "Resolved"
10. Helpers earn community credit
```

### Flow 2: Helper Offers Support

```
1. User signs up as helper
2. Sets preferences:
   - Forms: Time, Items, Cash (up to $50/month)
   - Geographic range: 10 miles
   - Categories: Families, Emergencies
3. System notifies when match available
4. Helper views request details
5. Helper chooses:
   - Form: Cash ($25)
   - Visibility: First name
   - Expectation: Pay it forward
6. Clicks "I'll Help"
7. Payment sent via Stripe
8. User receives help
9. Helper earns +25 community credit
```

### Flow 3: Continuity Reserve (Last Resort)

```
1. User requests help, no community match after 24h
2. System: "Continuity Reserve available ($25)"
3. User confirms urgency
4. System checks criteria → approved
5. $25 sent immediately
6. 72-hour window begins
7. User voluntarily repays (or doesn't) → no harassment
8. If repaid: +25 community credit, reserve replenished
```

---

## Anti-Features (Intentionally Excluded)

| Feature | Why Not |
|---------|---------|
| **Public Requests** | Preserves dignity, no shaming |
| **Leaderboards** | Not a competition, not social pressure |
| **Forced Repayment** | Voluntary only, no legal debt |
| **High Interest** | Zero interest, zero fees |
| **Aggressive Collection** | Systemic consequences, no harassment |
| **Data Selling** | Privacy-first, never sell data |

---

**Clarity. Community. Continuity.**
