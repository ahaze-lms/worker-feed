# Instagram-Style LMS Feed Concept (Toolbox Talks)

## Product Goal
Give learners a scrollable, personalized **safety feed** after login so required talks feel familiar and engaging (like social content), while preserving compliance rigor.

## Core Feed Objects
Each card in the feed should include:
- Talk title + number (e.g., `#1 Fall Protection — General Requirements`)
- Duration (`10 min`)
- Hazard category (`Fall`, `Struck-By`, etc.)
- Compliance metadata (`primary_cfr`, OSHA priority)
- Why this is recommended (role, jobsite risk, due date)
- Primary CTA (`Start Talk`) and secondary actions (`Save`, `Share`, `Assign to crew`)

## Suggested Information Architecture
1. **Global nav**
   - Feed
   - My Assignments
   - Compliance
   - Streaks/Badges
2. **Feed controls**
   - Quick filters: All, Fatal Four, Category chips
   - Sort: Recommended, Due Soon, Recently Added
3. **Card stream**
   - Vertical mobile-first cards
   - Dynamic ranking from risk + due dates + completion gaps
4. **Right rail (desktop) / bottom sheet (mobile)**
   - Personal progress
   - Team trends
   - Streak nudges

## Ranking Idea (Simple v1)
`rank_score = risk_weight + due_urgency + role_relevance + freshness - completed_recently_penalty`

Example weighting:
- Fatal Four: +30
- Due within 72 hours: +25
- Matches learner job role: +20
- Crew trend/topic spike: +10
- Completed in past 14 days: -40

## Engagement Features (without hurting compliance)
- “Why this appears” explanation to increase trust.
- 1-tap completion reminders tied to shift start.
- Team leaderboard based on **on-time completions**, not vanity likes.
- Reaction prompts can be safety-focused (“Discuss with crew”).

## Compliance Guardrails
- Feed should not hide mandatory content behind algorithmic ranking.
- Hard-pin overdue or legally required talks to top positions.
- Log timestamps, completion status, and assessment results for audits.
- Preserve CFR metadata in every completion record.

## Deliverable in this repo
A visual static mockup is available here:
- `mockups/toolbox-talks-feed-mockup.html`
