# Advance Tamil Tutor (24UADT401)

A simple quiz app for practising the Advance Tamil question bank. It runs in any web browser, works offline, and needs no installation.

## Features

- 238 questions across 5 units
- One question at a time, with options A to D
- Instant right or wrong marking, and the correct answer is shown
- Practise all units together or one unit at a time
- Running score during each session
- No repeated questions within a session
- Review the questions you missed at the end
- Reset the seen list to start fresh

## Units

| Unit | Theme | Questions |
|------|-------|-----------|
| 1 | Bharathiyar | 48 |
| 2 | Abdul Rahman | 50 |
| 3 | Short story | 50 |
| 4 | Modern poetry | 50 |
| 5 | Media and news writing | 40 |

Unit themes were inferred from the questions, so check them against your syllabus.

## How to use

1. Open `advance-tamil-tutor.html` in a browser.
2. Pick "All units" or a single unit.
3. Tap an option to answer, then tap Next.
4. At the end, review your missed questions or return to the menu.

Your progress lives only in the open page. Refreshing the page resets the score and the seen list.

## Files

| File | Purpose |
|------|---------|
| `advance-tamil-tutor.html` | The quiz app, with all questions built in |
| `advance-tamil-tutor/question_bank.json` | The cleaned question data |
| `advance-tamil-tutor/SKILL.md` | Skill for quizzing with Claude, with short explanations and memory tricks |

The web app shows the correct answer but has no explanations, because the source spreadsheet contains none. For explanations and memory tricks, use the skill with Claude.

## Host on GitHub Pages

1. Create a new public repository.
2. Upload `advance-tamil-tutor.html`. Rename it to `index.html` if you want a shorter link.
3. Go to Settings, then Pages. Choose the `main` branch and the `/ (root)` folder, then Save.
4. After a few minutes the app is live at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Source

Questions come from the college online exam question file `ADVANCE_TAMIL_24UADT401.xlsx` (Guru Nanak College, Autonomous, batch 2024). For personal study use.
