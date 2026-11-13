---
description: Set up Cred Farmer for a Claude certification, from enrolment to today's first step
argument-hint: <code> [exam date YYYY-MM-DD]
---

Get a learner started with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code and, if given, the exam date. With no code, help choose one with
   `/cred-farmer:exams` first.
2. Call `enroll_certification` with the date and a weekly goal if they give one (2, 4, 6, 8, 10
   or 12 sessions a week). This needs a free Cred Farmer account; Claude shows a Connect button.
3. Call `get_study_plan` and summarise the weekly pace, then `get_next_step` for what to do
   today, and offer to start it.
