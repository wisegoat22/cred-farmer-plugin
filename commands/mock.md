---
description: Get the links to a free practice exam and the timed mock exams
argument-hint: <code>
---

Point to the mock exams with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code from the arguments; ask for it if it is missing.
2. Call `get_mock_exam_link` and give each link with what it measures.
3. Say that mocks and the diagnostic are taken on credfarmer.com, not in this chat, and that the
   readiness score is read from timed mocks only. Offer `/cred-farmer:progress <code>` afterwards
   to see the new reading.
