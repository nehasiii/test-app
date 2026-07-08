# Quiz CLI

An interactive command-line quiz game for learning JavaScript and Node.js fundamentals.

## Features

- Interactive multiple-choice quiz experience
- Built with modern ES modules and async/await
- Category selection and question count options
- Score summary with explanations for incorrect answers
- No external dependencies required

## Requirements

- Node.js 18 or newer

## Getting Started

### Install

```bash
git clone <repository-url>
cd test-app
```

### Run the quiz

```bash
npm start
```

No additional dependencies are required.

## How It Works

1. Choose a quiz category
2. Pick how many questions to answer
3. Select the correct answer for each question
4. Review your score and explanations at the end

## Project Structure

```text
index.js            # App entry point
src/colors.js       # Terminal color helpers
src/input.js        # Readline-based input helpers
src/quiz.js         # Quiz logic and scoring
data/questions.json # Quiz questions
```

## Scripts

- `npm start` - Run the quiz
- `npm test` - Run the test suite

## License

MIT
