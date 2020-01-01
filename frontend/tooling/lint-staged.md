# Lint staged

You can lint and format by **eslint** and **prettier** git staged files in pre-commit action with module **lint-staged**

[[GitHub](https://github.com/okonet/lint-staged)]

Install dependency:

```bash
npm install --save-dev lint-staged
```

After that we need to configure file **.lintstagedrc** where we have to write our rules for specific files:

```json
{
  "*.+(js|ts|tsx)": [
    "eslint"
  ],
  "**/*.+(js|jsx|json|ts|tsx)": [
    "prettier --write",
    "git add"
  ]
}
```

You should already have **husky** in your project for running git actions. Now we should specify what we run lint-staged and other needed things in pre-commit action

**.huskyrc**

```json
{
  "hooks": {
    "pre-commit": "lint-staged && npm run build"
  }
}
```

