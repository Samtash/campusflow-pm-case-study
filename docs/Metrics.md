# Metrics

How we'd know CampusFlow is working, and how we'd know it's failing.

## North star metric
**Weekly active students who have tasks on at least 3 different days of the coming week.**

**Why this one:** Research showed students keep tasks in their heads and lose track when the week gets busy. If a student has the next week spread across 3 or more days in CampusFlow, they're using it the way it's meant to be used. Just opening the app doesn't count.

**How to count it:** Each Monday, count users who opened the app in the last 7 days and have tasks on 3 or more of the next 7 days.

## The user funnel

| Step | What it means | Target |
|---|---|---|
| 1. Sign up | Downloads and opens the app | Baseline |
| 2. Finish setup | Adds at least 1 repeating commitment and 2 tasks | 70% of sign ups |
| 3. First week | Opens the app on 3 or more days in week 1 | 50% of sign ups |
| 4. Week 2 | Still active in week 2 | 40% of sign ups |
| 5. Week 4 | Still active in week 4 | 25% of sign ups |

Week 2 is the big one. That's where the Google Calendar story fell apart in research.

## Supporting metrics

| Metric | Target | Linked feature |
|---|---|---|
| Time to add a task | Under 10 seconds | F1 Quick add |
| Tasks added by pasting from chat | 20% of all tasks | F2 Paste from chat |
| Repeating commitments per user | At least 1 in week 1 | F3 Repeating commitments |
| Today screen opens per week | 4 or more per active user | F5 Today screen |
| Clash warnings where the user moves something | 30% | F6 Clash warning |
| Reminders that lead to opening the app | 25% | F7 Commitment reminders |

## Outcome metrics
These check if students' lives actually got easier. Measured with a short survey after 4 weeks, using the same questions as the original research.

| Question | Baseline from research | Target |
|---|---|---|
| How often did you forget or almost forget something important this month? | 13 of 22 forgot 2 or more times in 3 months | Fewer than half forget 2 or more times in a month |
| How satisfied are you with how you manage your responsibilities? (1 to 5) | 3.3 average | 4.0 average |
| Did you miss a tuition class, club meeting or other commitment this month? | Common in interviews | Under 20% say yes |

## Guardrail metrics
These make sure CampusFlow doesn't become the problem.

| Metric | Limit | Why it matters |
|---|---|---|
| Time spent planning each week | Under 5 minutes | Setup time is why students quit planners |
| Users who turn off reminders | Under 20% | More than that means reminders are too noisy |
| Tasks deleted without being done | Under 30% | High numbers mean the list is getting messy |

## Events to track

| Event | When it fires |
|---|---|
| app_opened | User opens the app |
| setup_completed | User finishes first time setup |
| task_added | User adds a task. Track if it came from quick add or paste. |
| commitment_added | User adds a repeating commitment |
| task_completed | User marks a task done |
| task_moved | User moves a task to another day |
| clash_shown | Clash warning appears |
| clash_resolved | User keeps or moves the task after a warning |
| reminder_sent | A reminder goes out |
| reminder_opened | User opens the app from a reminder |
| reminders_turned_off | User turns off reminders |

## What we'd do if a metric misses

| If this happens | Likely cause | What to try |
|---|---|---|
| Setup under 70% | Setup is too long or confusing | Cut steps. Let users skip commitments and add them later. |
| Week 2 under 40% | Same pattern as Google Calendar | Talk to 5 users who left. Find what broke. |
| Paste from chat rarely used | Users don't know it exists or it reads dates wrong | Show it during setup. Check date accuracy. |
| Planning time over 5 minutes | Too much manual fixing | Look at where time goes. Make the slowest step one tap. |

## Review rhythm
* **Weekly:** north star and funnel
* **Every 2 weeks:** supporting and guardrail metrics
* **After 4 weeks:** outcome survey
