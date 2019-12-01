#Configuring Prettier, ESLint and AirBnb style for TypeScript in VSCode

1. Turn on the Prettier extension in VSCode
2. Install prettier npm package

```
npm install --save-dev prettier
```

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
