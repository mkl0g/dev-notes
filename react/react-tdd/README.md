## React Test Driven Development

Just a few notes about my experience with TDD in React development.

I use [Jest](https://github.com/facebook/jest) to write tests.

Install **Jest** using npm:

```
npm install --save-dev jest
```

Some tips for writing tests in React:

- Write name of ***describe*** section as name of component
- Write name of ***test*** section as present-tense verb

For example:

```javascript
describe('Article', () => {
  // ...
  it('renders the title', () => {})
})
```

Because when you will see information about pass/fail tests - you will read that as a sentence: ***Article renders the title***

- Use Triangulation method

Basically you should use data from different source in tests. Because if you will use hard-coded data in tests and in some component - tests will pass

- You should never refactor or rework your code while you are in **red** test

