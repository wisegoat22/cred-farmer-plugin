---
description: Show your measured Cred Farmer progress for a Claude certification
argument-hint: <code>
---

Show Cred Farmer progress with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code from the arguments; ask for it if it is missing.
2. Call `get_my_progress` and report the readiness score with its stage and gate, the weakest
   objectives, the streak, and how many answers were given in Claude.
3. Readiness is read from timed mocks only: offer `get_mock_exam_link` for a new reading, and
   `get_next_step` for the drill their results point to. Never predict a pass.
