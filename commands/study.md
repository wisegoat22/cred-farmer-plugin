---
description: Learn one Claude certification objective from the Cred Farmer study guide
argument-hint: <code> <objective or topic>
---

Teach one objective with the objective-tutor skill. Arguments: $ARGUMENTS

1. Read the certification code and the topic from the arguments; ask for whichever is missing.
2. Match the topic to an objective id with `get_exam_blueprint`.
3. Call `get_study_section`, teach the core of it briefly and link the `url` it returns.
4. Check understanding with one or two questions on that objective, one at a time.
