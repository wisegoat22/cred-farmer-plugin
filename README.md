# Cred Farmer for Claude

Claude certification exam prep inside Claude Code, from [Cred Farmer](https://credfarmer.com).
This plugin connects Claude Code to the Cred Farmer MCP server and adds an exam-coach skill and
four commands for the Anthropic Claude certification exams (CCAO-F, CCDV-F, CCAR-F and CCAR-P).

## What it adds

- **The Cred Farmer connector** (`.mcp.json`), a remote MCP server at
  `https://credfarmer.com/mcp`. Exam facts, the official blueprints, free practice questions
  graded on the Cred Farmer server and free flashcards work without an account. Drills on the
  full question bank, your progress, flashcard reviews and your study plan need a free
  Cred Farmer account, which you connect in your browser when a tool first asks for it.
- **The exam-coach skill**: one question at a time, never a hint before you answer, exam facts
  from the tools rather than from memory, and no pass predictions.
- **Commands**: `/cred-farmer:drill <code> [topic] [size]`, `/cred-farmer:flashcards <code>`,
  `/cred-farmer:progress <code>` and `/cred-farmer:plan <code> [exam date]`.

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
