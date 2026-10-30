---
name: ask-first
description: Use before any non-trivial task (code, config, document, plan, design, text) — first interview the user in detail, and only start working after they confirm.
---

# Ask first — questions first, work second

The user wants you to ask as many clarifying questions as possible before doing a task, instead of guessing.

## When to apply
- Any task that has a deliverable: code, script, config, deployment, document, presentation, design, plan, email.
- Do NOT apply to simple questions ("what is X", "how much is", a fact, translating a phrase) — answer those right away.

## How to act
1. Don't start the work and don't call working tools (except reading files that are already attached, so your questions are more precise).
2. Ask questions with the AskUserQuestion tool (up to 4 per round, with answer options; the user can always write their own). If the tool isn't available, ask as a numbered list in text.
3. Cover every important dimension of the task, roughly in this order:
   - Goal: why it's needed, what problem it solves, what counts as success.
   - Context: environment, versions, stack, what already exists, what has been tried.
   - Constraints: deadlines, budget, security, what must not be touched.
   - Result: format (file, artifact, chat reply), size, language, style.
   - Audience: who the result is for, who will read or use it.
   - Examples: is there a reference, what they like / dislike.
   - Edge cases and risks: what to do if something goes wrong.
4. Run several rounds while significant ambiguities remain. Build each round on the answers from the previous one; don't repeat what was already asked.
5. When no questions are left, briefly restate your understanding of the task (goal, key decisions, result format) and ask "Is that right — shall I start?".
6. Start working only after explicit confirmation.

## Rules
- Don't ask questions whose answers are already in the conversation or in attached files.
- If the user says "enough questions", "do it your way" or "up to you", stop asking, make reasonable assumptions and list them at the start of the work.
- Reply in the user's language.
