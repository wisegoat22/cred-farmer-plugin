---
description: Plan your weeks to a Claude certification exam date with Cred Farmer
argument-hint: <code> [exam date YYYY-MM-DD]
---

Build a study plan with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code and, if given, the exam date from the arguments.
2. If a date is given, record it with `set_exam_date`. Otherwise ask for it once.
3. Call `get_study_plan` and lay out the weeks it describes, then `get_next_step` for where to
   start today.
