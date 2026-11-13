# Cred Farmer for Claude

Claude certification exam prep inside Claude Code, from [Cred Farmer](https://credfarmer.com).
This plugin connects Claude Code to the Cred Farmer MCP server and adds three skills, eleven
commands and two agents for the Anthropic Claude certification exams (CCAO-F, CCDV-F, CCAR-F and CCAR-P).

## What it adds

- **The Cred Farmer connector** (`.mcp.json`), a remote MCP server at
  `https://credfarmer.com/mcp`. Exam facts, the official blueprints, free practice questions
  graded on the Cred Farmer server and free flashcards work without an account. Drills on the
  full question bank, your progress, flashcard reviews and your study plan need a free
  Cred Farmer account, which you connect in your browser when a tool first asks for it.
- **Three skills**, which Claude uses on its own when they fit:
  - *exam-coach*: one question at a time, never a hint before you answer, exam facts from the
    tools rather than from memory, and no pass predictions.
  - *certification-advisor*: which Claude certification to take, what it covers, costs and
    requires, from the official facts.
  - *objective-tutor*: teaches one exam objective from the Cred Farmer study guide, then checks
    it with a question or two.
- **Eleven commands**:

  | Command | What it does | Account |
  |---|---|---|
  | `/cred-farmer:exams [what you do]` | Compare the exams and pick where to start | No |
  | `/cred-farmer:blueprint <code>` | Domains, weights and objectives of one exam | No |
  | `/cred-farmer:practice <code> [topic]` | Free practice questions, graded with reasons | No |
  | `/cred-farmer:mock <code>` | Links to the free practice exam and the timed mocks | No |
  | `/cred-farmer:start <code> [exam date]` | Enrol, set the date, get today's first step | Free |
  | `/cred-farmer:drill <code> [topic] [size]` | A drill on the full question bank | Free |
  | `/cred-farmer:next <code>` | The drill your own results point to next | Free |
  | `/cred-farmer:study <code> <topic>` | Learn one objective from the study guide | Free |
  | `/cred-farmer:flashcards <code>` | Review your due flashcards | Free |
  | `/cred-farmer:progress <code>` | Your measured readiness and weakest objectives | Free |
  | `/cred-farmer:plan <code> [exam date]` | Your weekly plan to the exam date | Free |

- **Two agents** that work on their own and hand back a written result:
  - *progress-analyst*: a gap report of your weakest objectives against the exam weights, and
    what to do this week.
  - *revision-notes*: a one-page revision sheet from the study guide for the objectives you
    name, or your weakest ones.

## Install

In Claude Code:

```
/plugin marketplace add wisegoat22/cred-farmer-plugin
/plugin install cred-farmer@cred-farmer
```

Or from a terminal: `claude plugin marketplace add wisegoat22/cred-farmer-plugin`, then
`claude plugin install cred-farmer@cred-farmer`. The first time a tool needs your account, Claude
Code asks you to sign in to Cred Farmer in your browser.

## What it sends, and where

Everything goes to one place: `https://credfarmer.com/mcp`, over HTTPS. Claude sends the
arguments of each tool call (a certification code, a question number, the option you chose, a
confidence or flashcard rating, an exam date). Cred Farmer never receives your conversation.
If you connect your account, sign-in happens on credfarmer.com and Claude Code holds an access
token for one hour and a refresh token for up to 90 days of use. The plugin itself runs no local
code, contains no question content and stores nothing.

Timed mock exams and the diagnostic run on credfarmer.com only.

## Disconnect

Open Settings on credfarmer.com and choose Disconnect under Connected apps, or remove the
plugin. Details: [credfarmer.com/claude](https://credfarmer.com/claude) and the
[privacy policy](https://credfarmer.com/privacy).

## Support

hello@credfarmer.com. Cred Farmer is independent and not affiliated with Anthropic.
