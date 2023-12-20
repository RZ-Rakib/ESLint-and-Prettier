## Prettier & ESLint

---

**1. Prettier set up to workspace**

- Create a " _.prettierrc.json_ " file.
- Implement some rules to this file from [prettier.io](https://prettier.io/)
- The following rules are particularly pertinent to the context provided below.

```c
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true,
  "bracketSameLine": true,
  "arrowParens": "always"
}
```

**<u>N.B:</u>** For use prettier as a default formatter, select prettier as a default formatter, and after that, prettir's default rules will be applicable for all files in the VS code.

---

**2.Combined use Prettier and ESLint to workplace**

- `npm init -y`
- `npm install eslint --save -dev`
- `npm init @eslint/config`

---

After initialized, basic folders should be setup like these formats.

- _.vscode/settings.json_

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": false,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ]
}
```

- _Package.json_

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": false,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ]
}
```

- .eslintrc.json

```json
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": "airbnb-base",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "rules": {
    "no-alert": 0,
    "no-console": 2,
    "no-unused-vars": 1,
    "camelcase": 2,
    "no-var": 2,
    "no-empty": 2,
    "no-unreachable": 0,
    "eqeqeq": 2,
    "max-lines": ["error", 3],
    "semi": ["error", "always"],
    "quotes": ["error", "single"]
  }
}
// rules
//  "key": "value => off/0, warning/1, error/2"
```

- .prettierrc.json \*\*for html, CSS and another file if needed.

```c
{
  "trailingComma": "es5",
  "semi": true,
  "tabWidth": 2,
  "singleQuote": true,
  "bracketSameLine": true,
  "arrowParens": "always"
}
```
