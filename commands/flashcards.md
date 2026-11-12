---
description: Review your due Cred Farmer flashcards for a Claude certification
argument-hint: <code>
---

Review Cred Farmer flashcards with the exam-coach skill. Arguments: $ARGUMENTS

1. Read the certification code from the arguments; ask for it if it is missing.
2. Call `get_due_flashcards`. Show the front of one card, wait for the learner's recall, then
   show the back.
3. Ask how well they recalled it (again, hard, good or easy) and record it with
   `rate_flashcard`, then move to the next card.
4. Without a sign-in, `get_free_flashcards` gives free cards to review without saving ratings.
