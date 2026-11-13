---
description: Show what a Claude certification exam covers, domain by domain
argument-hint: <code>
---

Show an exam blueprint with the certification-advisor skill. Arguments: $ARGUMENTS

1. Read the certification code from the arguments; ask for it if it is missing.
2. Call `get_exam_blueprint` and list each domain with its weight, then its objectives with
   their ids, exactly as returned.
3. Point out the heaviest domains, and offer `/cred-farmer:study <code> <objective>` or
   `/cred-farmer:practice <code> <domain>` for any of them.
