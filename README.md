# Full Stack Open – Part 1: Exercises 1.6–1.14

**Author:** Murad Alam

| Exercises | Project | Folder |
|---|---|---|
| 1.6–1.11 | Unicafe (feedback & statistics) | [part1/unicafe](./part1/unicafe) |
| 1.12–1.14 | Anecdotes (voluntary) | [part1/anecdotes](./part1/anecdotes) |

## How to run

```bash
cd part1/unicafe      # or part1/anecdotes
npm install
npm run dev
```

## What I did

### Unicafe (1.6–1.11)
- **1.6** Built a feedback app with three buttons (good, neutral, bad), each with its own `useState` counter.
- **1.7** Added more statistics: total number of feedbacks, the average score (good = 1, neutral = 0, bad = -1) and the percentage of positive feedback.
- **1.8** Moved the statistics into their own `Statistics` component. State stays in `App` and is passed down as props.
- **1.9** The statistics are only shown after feedback has been given; before that the app says "No feedback given" (conditional rendering).
- **1.10** Split the UI into small components: `Button` for the buttons and `StatisticLine` for one row of statistics.
- **1.11** Showed the statistics in an HTML table.

### Anecdotes (1.12–1.14)
- **1.12** A "next anecdote" button shows a random software-engineering anecdote.
- **1.13** Added voting. Votes are kept in an array in state, one counter per anecdote. The array is copied before it is updated instead of being changed directly.
- **1.14** Shows the anecdote with the most votes.

## What I learned
- How to use the `useState` hook to keep and update state in a React component.
- Handling events (`onClick`) and passing event handler functions as props.
- Lifting state up: keeping state in the parent and passing values down to child components.
- Splitting the UI into small, reusable components (`Button`, `StatisticLine`, `Statistics`).
- Conditional rendering, e.g. showing a message when there is no data yet.
- Not defining components inside other components, and never mutating state directly. With arrays and objects, make a copy first (`[...votes]`) and set the copy as the new state.
- Calculating values from existing state (total, average, positive %) instead of storing them in their own state.
- Setting up and running a React project with Vite.
