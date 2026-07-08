# Quiz CLI
An interactive command-line quiz game for learning JavaScript and Node.js fundamentals.

## Overview
Quiz CLI is a Node.js terminal application that loads quiz questions from `data/questions.json`, lets you choose a category and number of questions, and then runs an interactive multiple-choice quiz in the terminal.

The app demonstrates:
- ES modules
- Async/await and Promises
- File system reading
- Readline-based user input
- Classes and OOP
- Array manipulation and destructuring
- ANSI terminal colors

## Features
- Interactive terminal UI with colored output
- Category selection
- Question-count selection (`All questions`, `3 questions`, or `5 questions` when available)
- Randomized question order within each quiz
- Progress display during the quiz
- Immediate feedback for correct and incorrect answers
- Explanations shown after each question when available
- Final score summary with performance message
- Review of missed questions at the end
- Built with only Node.js built-in modules; no external dependencies are declared

## Requirements
- Node.js `>=18.0.0`
- A terminal that supports ANSI color escape codes

## Setup / Installation
1. Clone the repository.
2. Make sure you are using Node.js 18 or newer.
3. No package installation is required because the project does not declare any external dependencies.

## Configuration
Quiz content is stored in:

- `data/questions.json`

The JSON structure is:

- `categories`
  - category ID such as `javascript`, `nodejs`, or `general`
  - `name`
  - `questions[]`
    - `question`
    - `options[]`
    - `answer` (0-based index of the correct option)
    - optional `explanation`

## Usage
### Run the quiz
```bash
npm start
```

This runs:
```bash
node index.js
```

### Gameplay flow
1. Choose a category.
2. Choose how many questions to answer.
3. Press Enter to begin.
4. Enter the number of the answer choice for each question.
5. Review your score and any missed questions.
6. Choose whether to play again.

### Example terminal interaction
```text
Choose a category:
  1. JavaScript Basics
  2. Node.js Fundamentals
  3. General Programming

Your choice (enter number): 1

How many questions?
  1. All questions
  2. 3 questions
  3. 5 questions

Your choice (enter number): 2
```

## Testing
The repository includes this script:

```bash
npm test
```

This runs Node's built-in test runner (`node --test`). At the moment, no test files are present in the repository.

## Project Structure
```text
.
├── index.js              # Application entry point
├── package.json          # Project metadata and npm scripts
├── README.md             # Project documentation
├── data/
│   └── questions.json    # Quiz categories and questions
└── src/
    ├── colors.js         # ANSI color helpers
    ├── input.js          # Readline helpers for prompts and selections
    └── quiz.js           # Quiz class and game logic
```

## Key Implementation Details
- `index.js` loads quiz data from `data/questions.json`, displays the banner, and controls the main game loop.
- `src/input.js` wraps Node's `readline` module for prompts, selection menus, confirmations, and pause screens.
- `src/quiz.js` contains the `Quiz` class, which shuffles questions, tracks answers, renders progress, and prints results.
- `src/colors.js` provides reusable ANSI color formatting helpers for terminal output.

## Available Quiz Categories
The bundled question bank currently includes:
- JavaScript Basics
- Node.js Fundamentals
- General Programming

## License
MIT (as declared in `package.json`).

## Missing / To Verify
- There is no standalone `LICENSE` file in the repository.
- There are currently no automated test files, even though `npm test` is configured.
