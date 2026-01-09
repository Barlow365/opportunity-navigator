# Opportunity Navigator - Risk Management & Controls

**Version:** 1.0
**Last Updated:** January 2026
**Status:** Risk Design Specification

---

## Executive Summary

Opportunity Navigator involves financial transactions (community giving + continuity reserve) which creates financial, legal, and operational risks. This document outlines controls to prevent system abuse, liquidity crises, and legal violations.

**Key Principle:** Sustainability through **automatic protection**, not human judgment.

---

## Financial Risks

### Risk 1: Reserve Depletion

**Scenario:** Too many users access continuity reserve, pool runs dry.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Small Caps** | $10-$25 per user max |
| **One at a Time** | Only 1 active reserve per user |
| **Auto-Tightening** | When liquidity <30%, reduce caps to $10 |
| **Helper-First Routing** | Always try community match before reserve |
| **Cooldown Periods** | 30 days between reserve uses |

**Liquidity Thresholds:**
- >70% liquidity → Normal operations ($25 max)
- 50-70% → Reduced caps ($15 max)
- 30-50% → Minimal caps ($10 max)
- <30% → Temporary pause, helper-only routing

### Risk 2: Low Repayment Rate

**Scenario:** Users don't repay voluntary reserve, pool doesn't replenish.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Voluntary, Not Required** | No legal obligation to repay |
| **Incentivize Repayment** | +25 community credit for repayment |
| **Access Priority** | Repayers get priority on future help |
| **Systemic Consequences** | Non-repayers face longer cooldowns (no harassment) |

**Expected Repayment Rate:** 60-80% (based on SoLo Funds 94% repayment)

### Risk 3: Helper Fatigue

**Scenario:** Helpers give once, never return.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Set Limits** | Helpers set monthly limits ($50/month typical) |
| **No Pressure** | Never required to give |
| **Recognition** | Community credit visible to user (not public) |
| **Match Quality** | Only match when helper capacity available |
| **Feedback Loop** | Show impact ("Your $25 helped Sarah keep her job") |

---

## Legal & Compliance Risks

### Risk 4: Micro-Lending Regulations

**Scenario:** Continuity reserve classified as lending, triggers CFPB regulations.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **No Interest** | Zero fees, zero interest |
| **Voluntary Repayment** | Not legally enforceable debt |
| **Small Amounts** | Under typical lending thresholds |
| **Clear Terms** | "This is not a loan" disclosure |
| **Legal Review** | Consult lawyer in all operating states |

**Regulatory Considerations:**
- **CFPB Small-Dollar Loan Rule:** Applies to lenders, not voluntary assistance
- **State usury laws:** Not applicable (no interest charged)
- **Truth in Lending Act:** Not applicable (no repayment required)

**Legal Framing:**
```
"The Continuity Reserve is emergency assistance, not a loan.
Repayment is voluntary and not legally required.
This is a community support tool, not a financial product."
```

### Risk 5: Money Transmitter License

**Scenario:** Facilitating helper→user payments requires state licenses.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Use Stripe** | Payments handled by licensed processor |
| **No Custody** | Platform never holds user funds |
| **Direct Transfer** | Helper → User direct via Stripe |
| **Consult Lawyer** | Verify compliance per state |

### Risk 6: Privacy & Data Protection

**Scenario:** User data exposed, privacy violated.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **No Public Requests** | Requests never shown publicly |
| **Anonymous Options** | Helpers can give anonymously |
| **GDPR Compliance** | Full data protection (if EU users) |
| **Encryption** | All sensitive data encrypted at rest |
| **Minimal Data** | Only collect what's necessary |

---

## Abuse & Fraud Risks

### Risk 7: System Gaming

**Scenario:** Users create multiple accounts, exploit reserve repeatedly.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Phone Verification** | One phone number per account |
| **IP Tracking** | Flag multiple accounts from same IP |
| **Community Credit Requirement** | New users start with low trust score |
| **Cooldown Periods** | 30 days between reserve uses |
| **Behavioral Analysis** | Flag suspicious patterns (ML in Phase 2) |

### Risk 8: Helper Exploitation

**Scenario:** Helpers feel pressured or exploited.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Set Limits** | Helpers define max capacity upfront |
| **No Obligation** | Can decline any match |
| **Transparency** | See request details before committing |
| **Feedback System** | Report abuse or pressure |

### Risk 9: Fake Requests

**Scenario:** Users submit false needs to get money.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Specific Requests** | "I need $25 for gas" not "I need money" |
| **Community Credit Gates** | New users get smaller amounts |
| **Helper Discretion** | Helpers choose whether to give |
| **Pattern Detection** | Flag users with repeated similar requests |

---

## Operational Risks

### Risk 10: Matching Failures

**Scenario:** No helpers available when user needs help.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Continuity Reserve** | Backstop when community can't help |
| **Pre-Recruit Helpers** | Onboard helpers before launch |
| **Geographic Expansion** | Expand helper pool over time |
| **Notification System** | Alert helpers when match available |

### Risk 11: AI Misguidance

**Scenario:** AI gives bad advice, user follows it, gets harmed.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Constrained Scope** | AI only surfaces options, doesn't advise |
| **Disclaimers** | "This is not legal or financial advice" |
| **Human Review** | High-stakes cases flagged for review (Phase 2) |
| **Feedback Loop** | Users report incorrect info → improve AI |

---

## Sustainability Risks

### Risk 12: Revenue Insufficient

**Scenario:** Platform can't sustain operations, needs outside funding.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Lean Operations** | Start small, scale slowly |
| **Reinvested Fees** | All revenue reinvested, not extracted |
| **Partner Matching** | Dollar-for-dollar matching from sponsors (Phase 2) |
| **Optional Membership** | $3-$5/month optional (not required) |

**Revenue Streams:**
- Optional membership ($3-$5/month)
- Post-resolution fee ($0.50)
- Round-ups
- Partner matching (Phase 2)

**Break-Even:** 500-1,000 users with 20% membership conversion

---

## Trust & Reputation Risks

### Risk 13: Public Perception as Predatory

**Scenario:** Seen as exploiting vulnerable people.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Transparency** | Open about fees, terms, reserves |
| **No Hidden Costs** | Zero interest, zero fees on reserve |
| **Dignity-First Design** | No shaming, no public call-outs |
| **Community Voice** | User testimonials, feedback prominently shown |

### Risk 14: Helper Burnout

**Scenario:** Helpers feel overwhelmed, stop participating.

**Mitigation:**

| Control | Description |
|---------|-------------|
| **Set Boundaries** | Helpers define limits ($50/month typical) |
| **Recognition** | Community credit, impact stories |
| **No Pressure** | Never required to give |
| **Quality Matches** | Only match when capacity available |

---

## Monitoring & Controls

### Automated Monitoring

| Metric | Alert Threshold | Action |
|--------|-----------------|--------|
| **Reserve Liquidity** | <30% | Auto-tighten caps, pause new reserves |
| **Repayment Rate** | <60% | Increase cooldown periods |
| **Helper Participation** | <10 active helpers | Recruit campaign |
| **Match Failure Rate** | >30% | Review matching algorithm |
| **Abuse Flags** | >3 per user | Manual review |

### Manual Review Triggers

- Reserve request >$25
- User with >3 abuse flags
- Helper with <50% follow-through rate
- Unusual request patterns

---

## Insurance & Liability

### Recommended Coverage

| Type | Coverage | Why |
|------|----------|-----|
| **General Liability** | $1M | User/helper disputes |
| **Cyber Liability** | $1M | Data breach protection |
| **D&O Insurance** | $1M | If incorporated, board protection |
| **E&O (Errors & Omissions)** | $500K | AI misguidance claims |

---

## Regulatory Response Plan

### If Contacted by Regulators

1. **Respond within 48 hours**
2. **Provide documentation** (terms, reserve mechanics, payment flows)
3. **Show non-lending framing** (voluntary, no interest)
4. **Demonstrate safeguards** (liquidity controls, privacy)
5. **Offer to modify** (if concerns raised)

### Potential Modifications

If regulators express concern:
- Remove reserve entirely → community-only
- Add more disclaimers
- Increase verification requirements
- Limit geographic scope

---

## Red Flags to Avoid

| Red Flag | Why It's Bad | How to Avoid |
|----------|--------------|--------------|
| **Interest charged** | Triggers lending laws | Zero interest, voluntary |
| **Required repayment** | Creates legal debt | Voluntary repayment only |
| **Public shaming** | Predatory, unethical | Private system, no harassment |
| **Hidden fees** | Deceptive | Full transparency upfront |
| **Aggressive collection** | Predatory | No collection, systemic only |

---

## Continuous Improvement

### Quarterly Reviews

- **Liquidity Status:** Are reserves sustainable?
- **Abuse Patterns:** New gaming strategies emerging?
- **Helper Health:** Are helpers satisfied?
- **User Outcomes:** Are people being helped effectively?
- **Legal Changes:** New regulations affecting operations?

---

## Conclusion

**Risk Position:** Manageable with proper controls

**Key Controls:**
1. ✅ Small amounts + cooldowns
2. ✅ Auto-tightening based on liquidity
3. ✅ Voluntary repayment (not enforced debt)
4. ✅ No public shaming
5. ✅ Community credit gates access

**Risk Level:** Medium (higher than typical apps, lower than traditional lending)

**Recommendation:** Proceed with MVP + legal review + continuous monitoring.

---

**Protect the system. Protect the users. Sustain the mission.**
