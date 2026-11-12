---
description: Run a Cred Farmer drill for a Claude certification, one question at a time
argument-hint: <code> [objective or domain] [size]
---

Run a Cred Farmer drill with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code (for example CCDV-F) from the arguments. If it is missing, ask
   for it.
2. If a topic is given, match it to an objective id or a domain number with
   `get_exam_blueprint`, then use `start_drill` with kind `objective` or `domain`. With no topic,
   use `get_next_step` and start the drill it names. Pass a size from 5 to 20 when one is given.
3. Show one question at a time and record each answer with `answer_drill_question`.
4. When every question is answered, call `finish_drill` and go through the misses using the
   returned explanations and study links.
