# Configuring Prettier, ESLint and Airbnb style for TypeScript projects in VSCode

## 1. Install `prettier` npm package

```
npm install --save-dev prettier
```

## 2. Turn on the Prettier extension in VSCode

Prettier is a code formatter and a VSCode extension. It allows teams to establish code formatting rules, and then it enforces those rules.

![Prettier search in VSCode](docs/prettier-extension.png)

3. Configure VSCode for formatting on save.
   In Workspace setting, check on "Format on Save" . This creates a file in .vscode/settings.json
   Add the following to the file

```
    "editor.formatOnSave": true,
    "[javascript]": {
        "editor.formatOnSave": true
    },
    "[typescript]": {
        "editor.formatOnSave": true
    }
```

5. Create prettier config file called .prettierrc.json and add the following in the file

```
{
    "trailingComma": "es5",
    "tabWidth": 4,
    "semi": true,
    "singleQuote": true,
    "printWidth": 80
}

```

5. Install eslint

```
npm install --save-dev eslint
```

6. Generate eslintrc.json config file

```
./node_modules/eslint/bin/eslint.js --init
```

7. Install config that prevents rules conflict between eslint and prettier

```
npm install --save-dev eslint-config-prettier
```

8. Install eslint plugin to integrate prettier rules into eslint

```
npm install --save-dev eslint-plugin-prettier
```

9. Configure prettier rules in eslintrc file

```
{
  "extends": ["prettier"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": ["error"]
  },
}
```

10. Install @typescript-eslint/parser

```
npm install @typescript-eslint/parser --save-dev
```

11. Configure .eslintrc to use @typescript-eslint/parser parser

```
{
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint"]
}
```

12. Install @typescript-eslint/eslint-plugin

```
npm i @typescript-eslint/eslint-plugin --save-dev
```
