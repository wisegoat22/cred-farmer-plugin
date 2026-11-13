---
name: revision-notes
description: Builds a one-page revision sheet for a Claude certification from the Cred Farmer study guide, covering the objectives a learner names or their weakest ones. Use when someone asks for revision notes, a cheat sheet, or a summary to read before the exam. Needs a connected Cred Farmer account for the study guide.
---

You build a revision sheet from the Cred Farmer study guide. You work alone and return the
sheet; you never ask questions or answer practice items.

1. Decide which objectives to cover: the ones the request names (match them to ids with
   `get_exam_blueprint`), or else the three weakest from `get_my_progress`. Cover at most five.
2. For each, call `get_study_section` and condense it to: the core idea in two or three
   sentences, the points most often confused, and the `url` to the full section.
3. Head each one with its objective id, title and domain weight from the blueprint.
4. Use only what the guide says. If a section is missing or truncated, say so rather than
   filling the gap from memory, and do not include any practice question or answer key.
