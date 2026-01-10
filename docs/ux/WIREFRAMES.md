# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is THREE-LAYER.

1) LAYER 1 (AI Navigator) provides CLARITY with zero risk.
   - Conversational UI helps users find resources.
   - Max 5 clarifying questions, honest timelines (2-6 weeks typical).
   - Identifies gaps and opens door to Layer 2.

2) LAYER 2 (Community Bridge) provides IMMEDIACY with low risk.
   - Request form for short-term needs ($10-$25, 48-72h).
   - Helper matching algorithm (geography + capacity).
   - Four forms of help: Time, Items, Cash, Access.
   - Helper agency: form, visibility, expectation.

3) LAYER 3 (Continuity Reserve) is LAST RESORT with tight control.
   - Very small amounts ($10-$25 max).
   - One active use at a time.
   - Only when community matching fails (24h elapsed).
   - No interest, no fees.

4) COMMUNITY CREDIT is the GLUE.
   - Private score tracking capacity extended + reliability demonstrated.
   - Unlocks priority matching, longer windows, fewer cooldowns.
   - Never public, never leaderboards, never flexing.

Terminology rules:
- Continuity Reserve is NOT a loan. It's a micro-credit safety net.
- Community Credit is PRIVATE (no public scores).
- Helpers have AGENCY (choose form, visibility, expectation).
- No predatory fees, no public shaming, no hidden terms.
- Dignity-first design.

If any document or wireframe conflicts with this model, it is WRONG and must be rewritten to match.

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, MODE indicator (LAYER 1 / LAYER 2 / LAYER 3 / CREDIT), 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.
- Every wireframe answers: Which layer does this serve? What moves the user forward?

All wireframes in this repo must follow ONE visual grammar:
- Use vertical rails, section blocks, and column layouts.
- Use the Inkwell-style planning layout.
- Do NOT introduce boxed UI mockups, new ASCII art styles, or different layout conventions.
- Every wireframe must be a zoom of the same canonical system:
  AI NAVIGATOR (Layer 1) → COMMUNITY BRIDGE (Layer 2) → CONTINUITY RESERVE (Layer 3) → COMMUNITY CREDIT

Required conventions:
- Each wireframe must include:
  - HEADER line
  - Page/Mode name
  - 2-3 column layout where relevant
  - Clear section headings (ALL CAPS)
- Symbols:
  [ ] pending / not started
  [x] confirmed / fulfilled / completed
  [>] active / in-progress
  [?] suggested / stubbed
- Every screen must clearly indicate whether it operates on:
  (A) AI NAVIGATOR (Layer 1)
  (B) COMMUNITY BRIDGE (Layer 2)
  (C) CONTINUITY RESERVE (Layer 3)
  (D) COMMUNITY CREDIT
  (E) HELPER PREFERENCES

If any wireframe is not traceable to this system, rewrite or delete it.


================================================================================
WIREFRAME LEGEND
================================================================================
| Symbols: [ ] pending | [x] confirmed | [>] active | [?] suggested

--------------------------------------------------------------------------------
HOME PAGE (PUBLIC MARKETING) | MODE: N/A
--------------------------------------------------------------------------------
/
+--------------------------------------------------------------------------------------+
| HEADER: Logo | How It Works | Features | Login | Sign Up                            |
+--------------------------------------------------------------------------------------+
| HERO SECTION                                                                         |
| +-----------------------------------------------------------------------------------+|
| | Clarity. Community. Continuity.                                                  ||
| |                                                                                   ||
| | Help people understand what help exists, bridge short-term gaps with             ||
| | community support, and avoid financial free-fall when systems move too slowly.   ||
| |                                                                                   ||
| | [Get Started Free] [See How It Works]                                            ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| THE PROBLEM                                                                          |
| +-----------------------------------------------------------------------------------+|
| | Most people don't fail because they are irresponsible. They fail because:        ||
| | - Help exists but takes weeks (benefits, programs, resources)                    ||
| | - Small issues interrupt work/school ($50 shortfall spirals)                     ||
| | - Asking for help feels humiliating                                              ||
| | - Financial tools punish (payday loans, overdraft fees)                          ||
| |                                                                                   ||
| | The Reality: Most crises are TIMING problems, not money problems.                ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| THE SOLUTION (3 LAYERS)                                                              |
| +---------+ +---------+ +---------+                                                  |
| | LAYER 1 | | LAYER 2 | | LAYER 3 |                                                  |
| | AI      | | COMM.   | | CONTIN. |                                                  |
| | NAVIGA- | | BRIDGE  | | RESERVE |                                                  |
| | TOR     | |         | |         |                                                  |
| | Clarity | | Immedi- | | Safety  |                                                  |
| |         | | acy     | | Net     |                                                  |
| | Zero    | | Low     | | Tightly |                                                  |
| | Risk    | | Risk    | | Control |                                                  |
| +---------+ +---------+ +---------+                                                  |
+--------------------------------------------------------------------------------------+
| FOOTER: Privacy | Terms | Help | Contact                                             |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
AI NAVIGATOR (CONVERSATIONAL UI) | MODE: AI NAVIGATOR (Layer 1)
--------------------------------------------------------------------------------
/navigator
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | AI Navigator | Dashboard                            |
+--------------------------------------------------------------------------------------+
| CONVERSATION INTERFACE                                                               |
| +-----------------------------------------------------------------------------------+|
| | AI: Hi! I'm here to help you find resources. What do you need help with?         ||
| |                                                                                   ||
| | USER: I'm behind on rent and worried about eviction                              ||
| |                                                                                   ||
| | AI: I understand. Let me ask a few questions to find the right resources.        ||
| |     How much are you behind? (1/5)                                               ||
| |                                                                                   ||
| | USER: About $800                                                                 ||
| |                                                                                   ||
| | AI: Got it. Are you currently working or receiving any income? (2/5)            ||
| |                                                                                   ||
| | USER: Yes, I work part-time                                                      ||
| |                                                                                   ||
| | AI: Do you live in [detected city/state]? (3/5)                                 ||
| |                                                                                   ||
| | USER: Yes                                                                        ||
| |                                                                                   ||
| | AI: Based on what you've told me, here are 3 programs that might help:          ||
| |                                                                                   ||
| | +-------------------------------------------------------------------------------+ ||
| | | 1. Emergency Rental Assistance Program (ERAP)                                 | ||
| | |    Eligibility: Income below 80% AMI, proof of hardship                       | ||
| | |    Amount: Up to 12 months rent + utilities                                  | ||
| | |    Timeline: 4-6 weeks typical (application + review)                        | ||
| | |    Apply: [Link to ERAP]                                                      | ||
| | +-------------------------------------------------------------------------------+ ||
| | +-------------------------------------------------------------------------------+ ||
| | | 2. Community Action Agency - Emergency Assistance                             | ||
| | |    Eligibility: Case-by-case basis                                            | ||
| | |    Amount: Typically $200-$500                                               | ||
| | |    Timeline: 2-3 weeks (appointment + approval)                              | ||
| | |    Apply: [Schedule Appointment]                                              | ||
| | +-------------------------------------------------------------------------------+ ||
| | +-------------------------------------------------------------------------------+ ||
| | | 3. United Way 211 - Local Resources                                           | ||
| | |    Free referral service connecting to local help                             | ||
| | |    Timeline: Immediate referrals, but program timelines vary                 | ||
| | |    Call: 211 or [Visit Website]                                               | ||
| | +-------------------------------------------------------------------------------+ ||
| |                                                                                   ||
| | AI: Important: These programs typically take 2-6 weeks. That doesn't solve       ||
| |     today. Would you like to see if community members can help bridge the gap?  ||
| |                                                                                   ||
| | [Yes, Show Community Options] [No, I'm Good] [Start New Search]                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| ACTIONS                                                                              |
| [Export Results] [Start Over] [View Community Bridge]                               |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST FORM (COMMUNITY BRIDGE) | MODE: COMMUNITY BRIDGE (Layer 2)
--------------------------------------------------------------------------------
/request
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Community Bridge Request | Dashboard                |
+--------------------------------------------------------------------------------------+
| REQUEST FORM                                                                         |
| +-----------------------------------------------------------------------------------+|
| | WHAT DO YOU NEED?                                                                 ||
| |                                                                                   ||
| | Describe your need:                                                               ||
| | [____________________________________________________________]                    ||
| | [____________________________________________________________]                    ||
| | [____________________________________________________________]                    ||
| |                                                                                   ||
| | Example: "Need $25 for gas to get to work interviews this week"                 ||
| |                                                                                   ||
| | Amount needed (if cash): [$_____] (Max $25)                                      ||
| |                                                                                   ||
| | Timeframe: How soon? [48 hours v] [72 hours] [1 week]                           ||
| |                                                                                   ||
| | Category:                                                                         ||
| | ○ Time (rides, errands, childcare)                                               ||
| | ● Cash ($10-$25)                                                                 ||
| | ○ Items (tools, supplies, household goods)                                       ||
| | ○ Access (introductions, know-how)                                               ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| MATCHING PREFERENCES                                                                 |
| +-----------------------------------------------------------------------------------+|
| | How would you like helpers to be matched?                                         ||
| |                                                                                   ||
| | Geographic range:  ○ Neighborhood  ● City  ○ County  ○ State                    ||
| |                                                                                   ||
| | Visibility preference:                                                            ||
| | ● Anonymous (helper sees need, not your name)                                    ||
| | ○ Visible (share my name + profile)                                              ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| EXPECTATIONS                                                                         |
| +-----------------------------------------------------------------------------------+|
| | What's your intent?                                                               ||
| |                                                                                   ||
| | ○ Gift (no expectation to repay)                                                 ||
| | ● Repay when stable (informal, no deadline)                                      ||
| | ○ Pay forward (help someone else later)                                          ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| REVIEW & SUBMIT                                                                      |
| +-----------------------------------------------------------------------------------+|
| | Your request will be shared with community members who have capacity.            ||
| | If no one can help within 24 hours, you may be eligible for Continuity Reserve.  ||
| |                                                                                   ||
| | [Cancel] [Submit Request]                                                         ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST STATUS (WAITING FOR MATCH) | MODE: COMMUNITY BRIDGE (Layer 2)
--------------------------------------------------------------------------------
/request/:requestId
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Request Status | Dashboard                          |
+--------------------------------------------------------------------------------------+
| REQUEST STATUS                                                                       |
| +-----------------------------------------------------------------------------------+|
| | Your request is active                                                            ||
| |                                                                                   ||
| | Status: [>] Waiting for helper match                                             ||
| | Posted: 2 hours ago                                                              ||
| | Expires: In 22 hours (if no match)                                               ||
| |                                                                                   ||
| | What you requested:                                                               ||
| | "$25 for gas to get to work interviews this week"                                ||
| |                                                                                   ||
| | Amount: $25                                                                       ||
| | Timeframe: 48 hours                                                              ||
| | Category: Cash                                                                    ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| MATCHING PROGRESS                                                                    |
| +-----------------------------------------------------------------------------------+|
| | We're searching for helpers in your area with capacity.                          ||
| |                                                                                   ||
| | +-------------------------------------------------------------------------------+ ||
| | | ████████░░░░░░░░░░░░░ Searching... (8 helpers notified)                       | ||
| | +-------------------------------------------------------------------------------+ ||
| |                                                                                   ||
| | Typically matches within 12 hours.                                               ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| WHAT HAPPENS NEXT                                                                    |
| +-----------------------------------------------------------------------------------+|
| | ✓ If matched: You'll be notified and connected with helper                      ||
| | ✓ If no match within 24h: You may apply for Continuity Reserve (last resort)    ||
| | ✓ You can cancel anytime: [Cancel Request]                                       ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
HELPER MATCHING RESULT | MODE: COMMUNITY BRIDGE (Layer 2)
--------------------------------------------------------------------------------
/request/:requestId (matched)
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Request Matched! | Dashboard                         |
+--------------------------------------------------------------------------------------+
| MATCHED!                                                                             |
| +-----------------------------------------------------------------------------------+|
| | Great news! A community member can help.                                          ||
| |                                                                                   ||
| | Helper: Jordan M. (Community Credit: High)                                       ||
| | Offering: $25 cash                                                                ||
| | Visibility: Anonymous (helper chose to share name)                               ||
| | Expectation: Gift (no repayment expected)                                        ||
| |                                                                                   ||
| | Jordan says: "I've been there. Hope this helps with the interviews!"            ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| NEXT STEPS                                                                           |
| +-----------------------------------------------------------------------------------+|
| | How to connect:                                                                   ||
| | - Jordan will send payment via [Venmo/CashApp/Zelle]                            ||
| | - Check your messages for payment details                                        ||
| | - Confirm receipt when you get it                                                ||
| |                                                                                   ||
| | [Message Jordan] [Confirm Receipt]                                               ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| AFTER FULFILLMENT                                                                    |
| +-----------------------------------------------------------------------------------+|
| | Once you confirm receipt:                                                         ||
| | - Jordan earns Community Credit (+$25 capacity extended)                         ||
| | - You can leave a thank you note (optional)                                      ||
| | - Request closes                                                                  ||
| |                                                                                   ||
| | If you resolve this yourself or no longer need help:                             ||
| | [Cancel Request] [Mark as Resolved]                                               ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
HELPER PREFERENCES | MODE: HELPER PREFERENCES
--------------------------------------------------------------------------------
/helper-preferences
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Helper Preferences | Dashboard                      |
+--------------------------------------------------------------------------------------+
| HELPER PROFILE                                                                       |
| +-----------------------------------------------------------------------------------+|
| | Become a helper and support community members in need.                            ||
| |                                                                                   ||
| | Your Community Credit: 145 points (High)                                         ||
| | - Capacity Extended: $120 (3 helps)                                              ||
| | - Reliability: 100% (all 3 resolved cleanly)                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| MONTHLY CAPACITY                                                                     |
| +-----------------------------------------------------------------------------------+|
| | How much can you offer per month?                                                 ||
| |                                                                                   ||
| | Cash: [$____50___] (Recommended: $25-$100)                                       ||
| | Time: [___5_] hours per month                                                    ||
| |                                                                                   ||
| | Used this month: $25 cash | 2 hours                                             ||
| | Remaining: $25 cash | 3 hours                                                   ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| FORMS OF HELP                                                                        |
| +-----------------------------------------------------------------------------------+|
| | What forms of help can you offer? (Select all that apply)                        ||
| |                                                                                   ||
| | [X] Time (rides, errands, childcare swap)                                        ||
| | [X] Cash ($10-$25)                                                               ||
| | [X] Items (tools, supplies, household goods)                                     ||
| | [ ] Access (introductions, know-how)                                             ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| MATCHING PREFERENCES                                                                 |
| +-----------------------------------------------------------------------------------+|
| | Geographic range: How far can you help?                                           ||
| | ○ Neighborhood  ● City  ○ County  ○ State                                       ||
| |                                                                                   ||
| | Visibility: How do you want to appear?                                           ||
| | ○ Anonymous (need doesn't see your name)                                         ||
| | ● Visible (share my name with requester)                                         ||
| |                                                                                   ||
| | Expectation default:                                                              ||
| | ● Gift (no repayment expected)                                                   ||
| | ○ Repay when stable                                                              ||
| | ○ Pay forward                                                                    ||
| |                                                                                   ||
| | You can change this per-request.                                                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| NOTIFICATION PREFERENCES                                                             |
| +-----------------------------------------------------------------------------------+|
| | How often do you want to be notified of needs?                                    ||
| |                                                                                   ||
| | ● Daily digest (1 email per day with all new requests)                           ||
| | ○ Immediate (as requests come in)                                                ||
| | ○ Weekly summary                                                                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| SAVE & ACTIVATE                                                                      |
| [Cancel] [Save Preferences] [Activate Helper Status]                                |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
CONTINUITY RESERVE APPLICATION | MODE: CONTINUITY RESERVE (Layer 3)
--------------------------------------------------------------------------------
/reserve
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Continuity Reserve | Dashboard                      |
+--------------------------------------------------------------------------------------+
| CONTINUITY RESERVE (LAST RESORT)                                                     |
| +-----------------------------------------------------------------------------------+|
| | The Continuity Reserve is a micro-credit safety net when community can't help.   ||
| |                                                                                   ||
| | Requirements:                                                                     ||
| | ✓ Community match failed (24h elapsed)                                           ||
| | ✓ No active reserve use                                                          ||
| | ✓ Urgent need confirmed                                                          ||
| | ✓ Community Credit > 50 points (you have 145)                                    ||
| |                                                                                   ||
| | Amount: $10-$25 max                                                              ||
| | Window: 48-72 hours to resolve                                                   ||
| | Interest: Zero                                                                    ||
| | Fees: Zero                                                                        ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| APPLICATION                                                                          |
| +-----------------------------------------------------------------------------------+|
| | Your request: "$25 for gas to get to work interviews this week"                  ||
| | Status: No community match after 24 hours                                        ||
| |                                                                                   ||
| | Reserve amount requested: [$__25___] (Max $25)                                   ||
| |                                                                                   ||
| | Why is this urgent?                                                               ||
| | [____________________________________________________________]                    ||
| | [____________________________________________________________]                    ||
| |                                                                                   ||
| | Example: "I have 3 job interviews this week. Without gas, I can't get there."   ||
| |                                                                                   ||
| | Expected resolution: How will you resolve this?                                  ||
| | ○ Paycheck on Friday (3 days)                                                    ||
| | ○ Benefit payment expected (5-7 days)                                            ||
| | ○ Other: [_____________________]                                                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| REVIEW & SUBMIT                                                                      |
| +-----------------------------------------------------------------------------------+|
| | Reserve terms:                                                                    ||
| | - Amount: $25                                                                     ||
| | - Window: 72 hours (expected resolution: 3 days)                                 ||
| | - No interest, no fees                                                            ||
| | - Voluntary repayment when stable (no forced collection)                         ||
| | - If not resolved: Access pauses, limits tighten (no personal chase)             ||
| |                                                                                   ||
| | [Cancel] [Submit Application]                                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
RESERVE STATUS (ACTIVE) | MODE: CONTINUITY RESERVE (Layer 3)
--------------------------------------------------------------------------------
/reserve/:reserveId
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Reserve Active | Dashboard                          |
+--------------------------------------------------------------------------------------+
| ACTIVE RESERVE                                                                       |
| +-----------------------------------------------------------------------------------+|
| | Your reserve is active                                                            ||
| |                                                                                   ||
| | Amount: $25                                                                       ||
| | Received: Today                                                                   ||
| | Window: 72 hours (expires in 71 hours)                                           ||
| | Expected resolution: Paycheck on Friday (2 days)                                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| PROGRESS TRACKER                                                                     |
| +-----------------------------------------------------------------------------------+|
| | +-------------------------------------------------------------------------------+ ||
| | | Day 1 ●●●●●●●●●●●●●●●●●●●● (You are here)                                   | ||
| | | Day 2 ○○○○○○○○○○○○○○○○○○○○                                                   | ||
| | | Day 3 ○○○○○○○○○○○○○○○○○○○○ (Expected paycheck)                               | ||
| | +-------------------------------------------------------------------------------+ ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| ACTIONS                                                                              |
| +-----------------------------------------------------------------------------------+|
| | When you're ready to resolve:                                                     ||
| | [Mark as Resolved] [Voluntary Repayment] [Need Extension]                        ||
| |                                                                                   ||
| | If you resolve early, you earn Community Credit bonus.                           ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
COMMUNITY CREDIT DASHBOARD | MODE: COMMUNITY CREDIT
--------------------------------------------------------------------------------
/community-credit
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Community Credit | Dashboard                        |
+--------------------------------------------------------------------------------------+
| YOUR COMMUNITY CREDIT                                                                |
| +-----------------------------------------------------------------------------------+|
| | Community Credit is a PRIVATE score tracking your contributions and reliability. ||
| | It's never public. No leaderboards. No flexing.                                  ||
| |                                                                                   ||
| | Your Score: 145 points (High)                                                    ||
| |                                                                                   ||
| | +-------------------------------------------------------------------------------+ ||
| | | Capacity Extended: 120 pts ███████████████████████░░░░░░                     | ||
| | | Reliability:        25 pts ███████░░░░░░░░░░░░░░░░░░░░░░                     | ||
| | +-------------------------------------------------------------------------------+ ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| HOW YOU EARNED IT                                                                    |
| +-----------------------------------------------------------------------------------+|
| | CAPACITY EXTENDED (what you've given)                                             ||
| | +-------------------------------------------------------------------------------+ ||
| | | [X] Helped Jordan with $25 gas money                     +$25 | 2 days ago    | ||
| | | [X] Gave ride to Sarah for job interview                 +10 hrs | 1 week ago | ||
| | | [X] Loaned tools to Alex for home repair                 +15 pts | 2 weeks    | ||
| | +-------------------------------------------------------------------------------+ ||
| |                                                                                   ||
| | RELIABILITY DEMONSTRATED (how well you followed through)                          ||
| | +-------------------------------------------------------------------------------+ ||
| | | [X] All 3 helps resolved cleanly (no issues)              +50 bonus            | ||
| | | [X] Repaid reserve early (2 days ahead)                   +25 bonus            | ||
| | +-------------------------------------------------------------------------------+ ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| WHAT IT UNLOCKS                                                                      |
| +-----------------------------------------------------------------------------------+|
| | Your Community Credit unlocks:                                                    ||
| | ✓ Priority matching (you get matched first when you need help)                   ||
| | ✓ Longer reserve windows (72h instead of 48h)                                    ||
| | ✓ Fewer cooldowns (request again sooner)                                         ||
| | ✓ Access to nonprofit grants (Phase 2 - coming soon)                             ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| KEEP BUILDING                                                                        |
| +-----------------------------------------------------------------------------------+|
| | Ways to earn more:                                                                ||
| | - Help community members (capacity extended)                                     ||
| | - Resolve requests cleanly (reliability demonstrated)                            ||
| | - Repay reserves early (reliability bonus)                                       ||
| | - Pay forward (help someone after being helped)                                  ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: N/A
--------------------------------------------------------------------------------
/settings
+--------------------------------------------------------------------------------------+
| HEADER: Opportunity Navigator | Settings | Dashboard                                |
+--------------------------------------------------------------------------------------+
| ACCOUNT SETTINGS                                                                     |
| +-----------------------------------------------------------------------------------+|
| | Name:  [Jordan Smith______________]                                               ||
| | Email: [jordan@example.com________]                                               ||
| | Phone: [(555) 123-4567____________]                                               ||
| | Password: [••••••••] [Change Password]                                            ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| LOCATION                                                                             |
| +-----------------------------------------------------------------------------------+|
| | City: [Los Angeles________________]                                               ||
| | State: [California________________]                                               ||
| | ZIP: [90001_______________________]                                               ||
| |                                                                                   ||
| | Used for matching helpers in your area.                                          ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| PRIVACY SETTINGS                                                                     |
| +-----------------------------------------------------------------------------------+|
| | Profile Visibility:                                                               ||
| | ○ Public  ● Private (only visible when requesting/helping)                       ||
| |                                                                                   ||
| | Community Credit Visibility:                                                      ||
| | ● Private (never shared publicly)                                                ||
| | [ ] Share with helpers when requesting                                           ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| NOTIFICATION PREFERENCES                                                             |
| +-----------------------------------------------------------------------------------+|
| | Email Notifications:                                                              ||
| | [X] Request matched                                                               ||
| | [X] Reserve approved/denied                                                       ||
| | [X] Community Credit milestones                                                   ||
| | [ ] Weekly summary                                                                ||
| |                                                                                   ||
| | SMS Notifications (optional):                                                     ||
| | [ ] Critical updates only                                                         ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| DANGER ZONE                                                                          |
| +-----------------------------------------------------------------------------------+|
| | [Deactivate Account] (Community Credit will be preserved for 6 months)           ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
MOBILE RESPONSIVE CONSIDERATIONS
--------------------------------------------------------------------------------

All layouts adapt to mobile with:
- Single column layout (no side-by-side)
- Touch-friendly tap targets (minimum 44x44px)
- Hamburger menu for navigation
- Bottom navigation bar: Navigator | Requests | Credit | Settings
- Conversational UI optimized for mobile chat
- Form inputs stack vertically

MOBILE AI NAVIGATOR EXAMPLE:
+----------------------------------+
| ☰ Opp Navigator          Profile |
+----------------------------------+
| AI NAVIGATOR                     |
+----------------------------------+
| AI: Hi! What do you need help    |
| with?                            |
|                                  |
| [Type your need here_________]   |
|                                  |
| [Send]                           |
+----------------------------------+
| Recent searches:                 |
| - Rent assistance                |
| - Job training                   |
+----------------------------------+
| Navigator | Requests | Settings  |
+----------------------------------+

MOBILE REQUEST FORM EXAMPLE:
+----------------------------------+
| ☰ Community Bridge       Profile |
+----------------------------------+
| WHAT DO YOU NEED?                |
+----------------------------------+
| Describe:                        |
| [_____________________________]  |
| [_____________________________]  |
|                                  |
| Amount: [$_____] (Max $25)       |
|                                  |
| Timeframe: [48 hours v]          |
|                                  |
| Category:                        |
| ○ Time                           |
| ● Cash                           |
| ○ Items                          |
| ○ Access                         |
+----------------------------------+
| [Cancel] [Submit Request]        |
+----------------------------------+
| Navigator | Requests | Settings  |
+----------------------------------+

--------------------------------------------------------------------------------
ANIMATION SPECIFICATIONS
--------------------------------------------------------------------------------

AI NAVIGATOR TYPING INDICATOR:
1. User sends message
2. AI typing indicator appears (3 bouncing dots)
3. Message slides in from left
4. Scroll to bottom smoothly

REQUEST MATCHING ANIMATION:
1. Request submitted
2. "Searching..." spinner with progress bar
3. Helper match notification appears with slide-down
4. Success confetti effect (subtle)

COMMUNITY CREDIT UPDATE:
1. Action completed (help given, reserve repaid)
2. "+25 points" badge floats up from action
3. Merges with Community Credit score
4. Score number counts up with easing
5. Progress bars fill smoothly

RESERVE APPROVAL:
1. Application submitted
2. "Reviewing..." state (2-3 seconds)
3. Approval modal slides up from bottom
4. "Reserve Approved" with checkmark animation
5. Amount displays with slide-in effect

--------------------------------------------------------------------------------
ACCESSIBILITY NOTES
--------------------------------------------------------------------------------

- All images have alt text
- Color contrast ratio minimum 4.5:1 (WCAG AA)
- Keyboard navigation supported (Tab, Enter, Arrow keys)
- Screen reader announcements for:
  - AI responses ("AI Navigator says: Here are 3 programs...")
  - Request status updates ("Request matched with helper Jordan")
  - Community Credit changes ("Earned 25 points for helping Sarah")
  - Reserve status ("Reserve active, 71 hours remaining")
- Focus indicators visible on all interactive elements
- Skip to main content link
- ARIA labels on all icon buttons
- Form validation with clear error messages
- Live regions for chat updates
- Chat history accessible via screen reader
