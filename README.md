## How this app works

- All 'Must-haves' instructions have been met.
- As a user drags the sliders, their onChange handlers dynamically set the App component state with their values.
- The Display component takes the App state values as 'year' and 'amount' props respectively and uses their values to automatically calculate both 'APR' percentages and a monthly repayment.
- Both APR and repayments are displayed within a reusable DisplayChild component.

## Improvements

- Lines 25-32 and 33-42 could have been refactored into 2 reusable components for easier testing.
- I would have loved to do the tests with Jest and Enzyme.
- Styling always be improved, perhaps using styled-components.

## Installation

### Setup

- unzip the compressed folder
- from your terminal, `cd` into the folder
- run the command `npm i` to install the dependencies
- to run the application type `npm start` after installing the dependencies

### Tests

- Note: I did not manage to do unit tests with Jest and Enzyme for this project, but would love to be able to do so at some point later!

- while still in the directory from your terminal, run `npm run test` to run any default snapshot tests

## Documentation

### Amount Range Slider

- a controlled component that can accept number values between 1000 and 20000
- increases or decreases by a number value of 100 at a time ('step' prop)

### Years Range Slider

- a controlled component that can accept number values between 1 and 5
- the values indicate the amount of years rather than months
- increases or decreases by a number value of 0.5 years at a time ('step' prop), to represent changes of 6 months at a time

### Display component

- must have two props: 'years' and 'amount', both values are numbers.

### DisplayChild component

- must have two props: 'func' and 'text'. 'Func' takes in a function as its value and 'text' a string.
