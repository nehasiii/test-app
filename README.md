# quiz-cli

An interactive command-line quiz game for learning JavaScript, Node.js fundamentals, and general programming concepts.

## Overview

`quiz-cli` is a simple Node.js terminal application that loads quiz questions from `data/questions.json`, lets you choose a category and question count, and then walks you through each question with progress tracking, immediate feedback, and a final score summary.

The app is built with native Node.js features only — no external dependencies are required.

## Features

- Interactive terminal UI with colored output
- Category-based quizzes
- Choice of all questions, 3 questions, or 5 questions when available
- Shuffled question order for each run
- Immediate correctness feedback after each answer
- Explanations shown after each question when available
- Final score summary with a performance message
- Review list for incorrect answers
- Replay prompt to start a new quiz session

## Requirements

- Node.js 18 or newer
- A terminal that supports ANSI colors

## Setup / Installation

1. Clone the repository.
2. Make sure you are using Node.js 18+.
3. No package installation is required because the project does not use third-party dependencies.

## Run the App

```bash
npm start
```

You can also run the entry file directly:

```bash
node index.js
```

## Usage

When the quiz starts, you will:

1. Choose a category
2. Choose how many questions to answer
3. Press Enter to begin
4. Select answers by entering the option number shown in the terminal
5. Review your final score and any incorrect answers
6. Choose whether to play again

### Example Flow

```text
Choose a category:
  1. JavaScript Basics
  2. Node.js Fundamentals
  3. General Programming

How many questions?
  1. All questions
  2. 3 questions
  3. 5 questions
```

## Testing

A test script is defined in `package.json`:

```bash
npm test
```

At the time of writing, the repository does not include dedicated test files, so this command is mainly a placeholder for future tests.

## Project Structure

```text
.
├── index.js              # Application entry point and main game loop
├── package.json          # Project metadata and npm scripts
├── data/
│   └── questions.json    # Quiz categories, questions, answers, and explanations
└── src/
    ├── colors.js         # ANSI color helpers for terminal output
    ├── input.js          # Readline-based input helpers
    └── quiz.js           # Quiz class, scoring, progress, and results logic
```

## Configuration and Data

Quiz content is stored in `data/questions.json`.

Each question includes:

- `question`: the prompt shown to the player
- `options`: the answer choices
- `answer`: the zero-based index of the correct option
- `explanation`: a short explanation displayed after answering

## Implementation Notes

- The app uses ES modules (`"type": "module"` in `package.json`).
- `index.js` loads the question bank, manages the main loop, and coordinates gameplay.
- `src/input.js` wraps Node's built-in `readline` module for prompts and selections.
- `src/quiz.js` handles shuffling, scoring, progress display, and final results.
- `src/colors.js` provides simple ANSI color formatting without external packages.

## License

MIT
