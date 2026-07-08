# quiz-cli

An interactive Node.js command-line quiz game that loads multiple-choice questions from JSON, lets you choose a category and number of questions, and then scores your answers with colored terminal output.

## Overview

`quiz-cli` is a small, self-contained terminal app built with Node.js and ES modules. It reads quiz questions from `data/questions.json`, prompts you to select a category and question count, then runs an interactive quiz session.

During the quiz, the app:

- shuffles questions
- tracks score and progress
- shows immediate correctness feedback
- displays explanations
- presents a final results summary
- reviews incorrect answers at the end

## Features

- Interactive terminal quiz flow
- Category selection
- Configurable number of questions
- Multiple-choice questions loaded from JSON
- Score tracking and progress display
- Explanations for each answer
- Final results and incorrect-answer review
- ANSI-colored output for readable terminal UX
- No external npm dependencies

## Requirements

- **Node.js 18+**
- A terminal that supports ANSI colors

## Setup / Installation

Clone the repository and install dependencies:

```bash
npm install
```

> There are no external dependencies listed in `package.json`, but running `npm install` will still prepare the project as a standard Node.js app.

## Running the App

Start the quiz:

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

## Usage

When the app starts, it will:

1. show a banner
2. prompt you to choose a quiz category
3. prompt you to choose how many questions to answer
4. ask each question interactively
5. show your score and review incorrect answers

### Example Flow

```bash
npm start
```

You will then be guided through the quiz in the terminal.

## Testing

The project includes a Node test script:

```bash
npm test
```

This runs:

```bash
node --test
```

## Project Structure

```text
.
├── index.js
├── package.json
├── data/
│   └── questions.json
└── src/
    ├── colors.js
    ├── input.js
    └── quiz.js
```

### File Guide

- `index.js` — application entry point
- `package.json` — project metadata and scripts
- `data/questions.json` — quiz question bank
- `src/colors.js` — ANSI color helpers
- `src/input.js` — readline-based prompt/select/confirm helpers
- `src/quiz.js` — quiz engine and scoring logic

## Question Categories

The question bank is grouped into these categories:

- `javascript`
- `nodejs`
- `general`

Each question includes:

- `question`
- `options`
- `answer` index
- `explanation`

## Implementation Notes

- The project uses **ES Modules** via `"type": "module"` in `package.json`
- The quiz logic uses a **Fisher-Yates shuffle**
- Input handling is built on Node’s readline interface
- Output formatting is handled with simple ANSI color utilities, without external libraries

## Development

Useful scripts:

```bash
npm start   # run the quiz
npm test    # run tests
```

## License

This project is released under the MIT License, as declared in `package.json`.
