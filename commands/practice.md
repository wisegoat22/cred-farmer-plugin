---
description: Answer free Claude certification practice questions, no account needed
argument-hint: <code> [objective or domain]
---

Ask free Cred Farmer practice questions with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code from the arguments; ask for it if it is missing. If a topic is
   given, match it to an objective id or a domain number with `get_exam_blueprint`.
2. Call `get_practice_question` with the filter, passing the `item_ref` of every question
   already asked in `exclude` so none repeats.
3. Show the stem and every option exactly as returned. Wait for the learner's answer, with no
   hints, then grade it with `check_practice_answer` and explain from the returned rationale.
4. Offer the next question. Nothing is saved; for drills that track progress, offer
   `/cred-farmer:drill`.
