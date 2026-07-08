# quiz-cli

An interactive command-line quiz game for learning JavaScript.

## Overview

`quiz-cli` is a Node.js terminal application that loads quiz questions from local JSON data and runs an interactive quiz in the terminal. The app lets you choose a category and question count, then presents questions, tracks your score, shows progress, and reviews answers with explanations at the end.

## Features

- Interactive terminal-based quiz flow
- Category selection before starting
- Selectable question count
- Local question data stored in `data/questions.json`
- Fisher-Yates question shuffling
- Score tracking and progress display
- End-of-quiz result review with explanations
- Replay support after finishing
- ANSI terminal styling helpers for colored output

## Prerequisites

- Node.js **18.0.0 or later**

## Installation

Clone the repository and install dependencies:

```bash
npm install
```

## Usage

Start the quiz:

```bash
npm start
```

The app will:

1. Display a banner
2. Prompt you to choose a category
3. Ask how many questions you want
4. Run the quiz in the terminal
5. Show your results and explanations
6. Offer the option to replay

## Question Categories

Questions are stored locally in `data/questions.json`.

Available categories:

- `javascript`
- `nodejs`
- `general`

The dataset contains 15 total questions, and each question includes:

- `question`
- `options`
- `answer`
- `explanation`

## Project Structure

```text
index.js
data/questions.json
src/
  colors.js
  input.js
  quiz.js
package.json
.vscode/settings.json
```

### Key files

- `index.js` — CLI entry point
- `src/quiz.js` — quiz logic, scoring, shuffling, progress, and review
- `src/input.js` — readline-based prompt/select/confirm/pressEnter helpers
- `src/colors.js` — ANSI styling helpers
- `data/questions.json` — quiz content

## Scripts

Available npm scripts from `package.json`:

```bash
npm start
npm test
```

- `npm start` → `node index.js`
- `npm test` → `node --test`

## Testing

A test script is defined, but no test files were found in the repository tree.

```bash
npm test
```

## Notes / Limitations

- The quiz runs entirely in the terminal.
- All questions are loaded from local JSON data; there is no remote API or database.
- No build, deployment, or CI/CD configuration was found in the repository.
- No additional setup beyond Node.js 18+ and `npm install` is indicated by the repository contents.

## License

MIT