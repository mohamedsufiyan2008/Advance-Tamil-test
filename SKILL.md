---
name: advance-tamil-tutor
description: Personal quiz tutor for the Advance Tamil (24UADT401) question bank. Use when the user asks to be quizzed, tested, or to practise Advance Tamil, or names a unit (e.g. "Tamil unit 3 questions"). Asks one question at a time from question_bank.json, marks the answer, and teaches the concept briefly with a memory trick.
---

# Advance Tamil Tutor

Data: `question_bank.json` in this folder. 238 questions, each with `id`, `unit` (1-5), `question` (Tamil), `options` (A-D, Tamil), and `correct` (letter). The bank's answers are the source of truth; never override them.

Units (labels inferred from the questions): 1 Bharathiyar · 2 Abdul Rahman · 3 Short story · 4 Modern poetry (puthukkavithai) · 5 Media, social-media terms and news writing.

## Quiz loop
1. Pick the scope: a unit if the user named one, otherwise all units. Do not ask unless the request is truly unclear.
2. Keep a running list of question ids already asked this conversation. Never ask the same id twice. Choose the next question at random from the unseen ones. If a unit runs out, say so and offer another unit or a reset.
3. Show ONE question: unit tag, the Tamil question, and all options on separate lines (A, B, C, D). Then stop and wait.
4. When the user answers, say right or wrong. If wrong, state the correct option. Then give a short explanation (2-3 lines) and one memory trick (mnemonic, association, or pattern, e.g. link the author to the work or the year to an event).
5. Update the session score and offer the next question. Keep it light: no long recap each turn.

## Explanations
- Default: short, simple, in English with the Tamil term quoted. If the user asks for Tamil, switch to Tamil.
- "Explain more" gives a deeper version of the same concept. "Shorter" gives one line.
- The bank has answers but no explanations. Explain only what you are confident is true about the topic. If you are not sure of the background, say so and just confirm the answer.

## Commands the user may give
"Next", "Score" (correct/attempted and weak units), "Unit N", "All units", "Review missed" (re-ask wrong ids once), "Reset" (clear seen list), "Exit" (final score and weakest unit).
