# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is THREE-LAYER.

1) LAYER 1 (AI Navigator) provides CLARITY with zero risk.
2) LAYER 2 (Community Bridge) provides IMMEDIACY with low risk.
3) LAYER 3 (Continuity Reserve) is LAST RESORT with tight control.
4) COMMUNITY CREDIT is the GLUE (private score, never public).

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, LAYER indicator, 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.

## Route Catalog
| Route | Layer | Purpose | State transitions |
| --- | --- | --- | --- |
| /navigator | LAYER 1 | AI conversation | Conversation -> Programs |
| /request | LAYER 2 | Submit need | Request -> Matching |
| /request/:id | LAYER 2 | Track match | Matching -> Fulfilled |
| /reserve | LAYER 3 | Apply for reserve | Reserve -> Active |
| /reserve/:id | LAYER 3 | Track reserve | Active -> Resolved |
| /community-credit | CREDIT | View score | N/A |
| /helper-preferences | LAYER 2 | Set capacity | Inactive -> Active helper |

--------------------------------------------------------------------------------
AI NAVIGATOR | MODE: LAYER 1
--------------------------------------------------------------------------------
/navigator
+------------------------------------------------------------------------------+
| HEADER: AI Navigator | Clarity | Zero Risk                                  |
+------------------------------------------------------------------------------+
| DATA LOCATION: CONVERSATION HISTORY                                         |
|                                                                              |
| AI: What do you need help with?                                              |
| USER: I'm behind on rent, worried about eviction                             |
|                                                                              |
| AI: How much are you behind? (1/5)                                           |
| USER: About $800                                                             |
|                                                                              |
| AI: Are you currently working? (2/5)                                         |
| USER: Yes, part-time                                                         |
|                                                                              |
| PROGRAM MATCHING RESULTS:                                                    |
|                                                                              |
| 1. Emergency Rental Assistance (ERAP)                                        |
|    Timeline: 4-6 weeks typical                                               |
|    Amount: Up to 12 months rent                                              |
|    [Apply Link]                                                              |
|                                                                              |
| 2. Community Action Agency                                                   |
|    Timeline: 2-3 weeks                                                       |
|    Amount: $200-$500                                                         |
|    [Schedule Appointment]                                                    |
|                                                                              |
| AI: These programs take 2-6 weeks. That doesn't solve today.                 |
|     Would you like community help?                                           |
|                                                                              |
| ACTION: [Yes, Show Community Options] -> /request (Layer 2)                  |
|         [No, I'm Good] -> Export results                                     |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST FORM | MODE: LAYER 2
--------------------------------------------------------------------------------
/request
+------------------------------------------------------------------------------+
| HEADER: Community Bridge Request | Immediacy | Low Risk                     |
+------------------------------------------------------------------------------+
| DATA LOCATION: REQUEST FORM                                                 |
|                                                                              |
| WHAT DO YOU NEED?                                                            |
| Describe your need:                                                          |
| [Need $25 for gas to get to work interviews this week________________]       |
|                                                                              |
| Amount: [$__25___] (Max $25)                                                 |
| Timeframe: ● 48 hours  ○ 72 hours                                            |
|                                                                              |
| CATEGORY:                                                                    |
| ○ Time (rides, errands)                                                      |
| ● Cash ($10-$25)                                                             |
| ○ Items (tools, goods)                                                       |
| ○ Access (intros, know-how)                                                  |
|                                                                              |
| VISIBILITY:                                                                  |
| ● Anonymous  ○ Visible                                                       |
|                                                                              |
| EXPECTATION:                                                                 |
| ○ Gift  ● Repay when stable  ○ Pay forward                                   |
|                                                                              |
| MATCHING CRITERIA:                                                           |
| - Amount: $10-$25 max                                                        |
| - Timeframe: 48-72h                                                          |
| - Geographic: City                                                           |
| - Category: Cash                                                             |
|                                                                              |
| IF NO MATCH IN 24H: Eligible for Layer 3 (Reserve)                           |
|                                                                              |
| ACTION: [Submit Request] -> /request/:id                                     |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST STATUS (WAITING) | MODE: LAYER 2
--------------------------------------------------------------------------------
/request/:requestId
+------------------------------------------------------------------------------+
| HEADER: Request Status | Waiting for Match | Posted 2 hours ago             |
+------------------------------------------------------------------------------+
| DATA LOCATION: REQUEST TRACKING                                             |
|                                                                              |
| YOUR REQUEST IS ACTIVE:                                                      |
| Status: [>] Waiting for helper match                                         |
| Expires: In 22 hours (if no match)                                           |
|                                                                              |
| What you requested:                                                          |
| "$25 for gas for work interviews"                                            |
|                                                                              |
| MATCHING PROGRESS:                                                           |
| ████████░░░░░░░░ Searching...                                                |
| 8 helpers notified                                                           |
| Typically matches within 12 hours                                            |
|                                                                              |
| WHAT HAPPENS NEXT:                                                           |
| ✓ If matched: Connect with helper                                            |
| ✓ If no match (24h): Layer 3 eligible                                        |
|                                                                              |
| STATE TRANSITIONS:                                                           |
| Waiting ---> Matched ---> Fulfilled                                          |
| Waiting ---> No Match ---> Reserve                                           |
|                                                                              |
| ACTION: [Cancel Request]                                                     |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST STATUS (MATCHED) | MODE: LAYER 2
--------------------------------------------------------------------------------
/request/:requestId
+------------------------------------------------------------------------------+
| HEADER: Request Matched! | Helper Found | Jordan M.                         |
+------------------------------------------------------------------------------+
| DATA LOCATION: MATCH RECORD                                                 |
|                                                                              |
| MATCHED!                                                                     |
| Helper: Jordan M. (High Community Credit)                                    |
| Offering: $25 cash                                                           |
| Visibility: Anonymous (shared name)                                          |
| Expectation: Gift                                                            |
|                                                                              |
| Jordan says: "I've been there. Hope this helps with the interviews!"         |
|                                                                              |
| HELPER DETAILS:                                                              |
| Capacity Extended: $120 (3 helps)                                            |
| Reliability: 100% (all resolved)                                             |
|                                                                              |
| NEXT STEPS:                                                                  |
| - Jordan will send payment via Venmo                                         |
| - Check messages for details                                                 |
| - Confirm receipt when you get it                                            |
|                                                                              |
| PAYMENT FLOW:                                                                |
| Jordan sends payment -> You confirm receipt -> Jordan earns +$25 credit      |
|                                                                              |
| ACTION: [Message Jordan] [Confirm Receipt]                                   |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
HELPER PREFERENCES | MODE: LAYER 2
--------------------------------------------------------------------------------
/helper-preferences
+------------------------------------------------------------------------------+
| HEADER: Helper Preferences | Become a Helper | Set Capacity                |
+------------------------------------------------------------------------------+
| DATA LOCATION: HELPER PROFILE                                               |
|                                                                              |
| YOUR COMMUNITY CREDIT: 145 points (High)                                     |
| - Capacity Extended: $120 (3 helps)                                          |
| - Reliability: 100% (all resolved)                                           |
|                                                                              |
| FORMS OF HELP (select all):                                                  |
| [x] Time (rides, errands, childcare)                                         |
| [x] Cash ($10-$25)                                                           |
| [x] Items (tools, supplies, goods)                                           |
| [ ] Access (introductions, know-how)                                         |
|                                                                              |
| MONTHLY CAPACITY:                                                            |
| Cash: [$___50___] (Rec: $25-$100)                                            |
| Time: [___5___] hours/month                                                  |
|                                                                              |
| Used this month: $25 cash | 2 hours                                          |
| Remaining: $25 cash | 3 hours                                                |
|                                                                              |
| VISIBILITY:                                                                  |
| ● Visible (share name)  ○ Anonymous                                          |
|                                                                              |
| EXPECTATION DEFAULT:                                                         |
| ● Gift  ○ Repay when stable  ○ Pay forward                                   |
|                                                                              |
| MATCHING PREFERENCES:                                                        |
| Geographic: ● City  ○ County  ○ State                                        |
| Notifications: ● Daily digest  ○ Immediate  ○ Weekly                         |
|                                                                              |
| ACTION: [Save Preferences] [Activate]                                        |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
CONTINUITY RESERVE APPLICATION | MODE: LAYER 3
--------------------------------------------------------------------------------
/reserve
+------------------------------------------------------------------------------+
| HEADER: Continuity Reserve | Last Resort | Tightly Controlled               |
+------------------------------------------------------------------------------+
| DATA LOCATION: RESERVE APPLICATION                                          |
|                                                                              |
| REQUIREMENTS:                                                                |
| ✓ Community match failed (24h elapsed)                                       |
| ✓ No active reserve use                                                      |
| ✓ Urgent need confirmed                                                      |
| ✓ Community Credit > 50 (you have 145)                                       |
|                                                                              |
| YOUR REQUEST:                                                                |
| "$25 for gas for work interviews"                                            |
| Status: No community match after 24h                                         |
|                                                                              |
| RESERVE AMOUNT: [$__25___] (Max $25)                                         |
|                                                                              |
| WHY IS THIS URGENT?                                                          |
| [I have 3 job interviews this week____________________________]              |
| [Without gas, I can't get there_______________________________]              |
|                                                                              |
| EXPECTED RESOLUTION:                                                         |
| ● Paycheck on Friday (3 days)                                                |
| ○ Benefit payment (5-7 days)                                                 |
| ○ Other: [_____________________]                                             |
|                                                                              |
| RESERVE CHARACTERISTICS:                                                     |
| - Amount: $10-$25 max                                                        |
| - Window: 48-72 hours                                                        |
| - One active use at a time                                                   |
| - No interest, no fees                                                       |
| - Last resort only                                                           |
|                                                                              |
| IF NOT RESOLVED:                                                             |
| - Access pauses (no personal chase)                                          |
| - Limits tighten quietly                                                     |
| - No aggressive collection                                                   |
|                                                                              |
| ACTION: [Submit Application] -> /reserve/:id                                 |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
RESERVE STATUS (ACTIVE) | MODE: LAYER 3
--------------------------------------------------------------------------------
/reserve/:reserveId
+------------------------------------------------------------------------------+
| HEADER: Reserve Active | $25 | Window: 72 hours | Expires in 71h            |
+------------------------------------------------------------------------------+
| DATA LOCATION: RESERVE TRACKING                                             |
|                                                                              |
| ACTIVE RESERVE:                                                              |
| Amount: $25                                                                  |
| Received: Today                                                              |
| Window: 72 hours (expires in 71h)                                            |
| Expected resolution: Paycheck (2 days)                                       |
|                                                                              |
| PROGRESS TRACKER:                                                            |
| Day 1: ●●●●●●●●●●●● (You are here)                                          |
| Day 2: ○○○○○○○○○○○○                                                          |
| Day 3: ○○○○○○○○○○○○ (Paycheck)                                               |
|                                                                              |
| RESOLUTION OPTIONS:                                                          |
| [Mark as Resolved]                                                           |
| [Voluntary Repayment]                                                        |
| [Need Extension]                                                             |
|                                                                              |
| EARLY RESOLUTION BONUS:                                                      |
| Resolve early: +25 Community Credit                                          |
| Resolve on time: +10 Community Credit                                        |
| Extension: No credit                                                         |
|                                                                              |
| ACTION: [Mark as Resolved] -> /community-credit (earn bonus)                 |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
COMMUNITY CREDIT DASHBOARD | MODE: COMMUNITY CREDIT
--------------------------------------------------------------------------------
/community-credit
+------------------------------------------------------------------------------+
| HEADER: Community Credit | Private Score | Never Public                     |
+------------------------------------------------------------------------------+
| DATA LOCATION: CREDIT HISTORY                                               |
|                                                                              |
| YOUR SCORE: 145 points (High)                                                |
| Capacity Extended: 120 pts ████████░                                         |
| Reliability:        25 pts ███░░░░░░                                         |
|                                                                              |
| WHAT IT UNLOCKS:                                                             |
| ✓ Priority matching (matched first)                                          |
| ✓ Longer reserve windows (72h vs 48h)                                        |
| ✓ Fewer cooldowns (request again sooner)                                     |
| ✓ Access to nonprofit grants (Phase 2)                                       |
|                                                                              |
| HOW YOU EARNED IT:                                                           |
|                                                                              |
| CAPACITY EXTENDED:                                                           |
| [x] Helped Jordan ($25 gas) - 2d ago                                         |
| [x] Gave ride to Sarah - 1w ago                                              |
| [x] Loaned tools to Alex - 2w ago                                            |
|                                                                              |
| RELIABILITY DEMONSTRATED:                                                    |
| [x] All 3 helps resolved cleanly (+50)                                       |
| [x] Repaid reserve early 2d ahead (+25)                                      |
|                                                                              |
| KEEP BUILDING:                                                               |
| - Help community members (capacity)                                          |
| - Resolve requests cleanly (reliability)                                     |
| - Repay reserves early (reliability bonus)                                   |
| - Pay forward (help after being helped)                                      |
|                                                                              |
| PRIVATE SCORE:                                                               |
| No public scores, leaderboards, or flexing                                   |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: SETTINGS
--------------------------------------------------------------------------------
/settings
+------------------------------------------------------------------------------+
| HEADER: Settings | Account | Location | Privacy | Notifications            |
+------------------------------------------------------------------------------+
| DATA LOCATION: USER SETTINGS                                                |
|                                                                              |
| ACCOUNT:                                                                     |
| Name:  [Jordan Smith______________]                                          |
| Email: [jordan@example.com________]                                          |
| Phone: [(555) 123-4567____________]                                          |
| Password: [••••••••] [Change]                                                |
|                                                                              |
| LOCATION (for helper matching):                                              |
| City: [Los Angeles________________]                                          |
| State: [California________________]                                          |
| ZIP: [90001_______________________]                                          |
|                                                                              |
| PRIVACY:                                                                     |
| Profile Visibility: ● Private                                                |
| Community Credit: ● Private (never public)                                   |
| [ ] Share credit with helpers                                                |
|                                                                              |
| NOTIFICATIONS:                                                               |
| [x] Request matched                                                          |
| [x] Reserve approved/denied                                                  |
| [x] Community Credit milestones                                              |
| [ ] Weekly summary                                                           |
|                                                                              |
| ACTION: [Save Changes]                                                       |
|                                                                              |
| DANGER ZONE: [Deactivate Account] (Credit preserved 6 months)                |
+------------------------------------------------------------------------------+
