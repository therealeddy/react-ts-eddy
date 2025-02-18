<h1 align="center">
 <img src="docs/logo.png" height="90" alt="react-typescript-eddy" />
</h1>

<br>

<div align="center">

[![version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/therealeddy/react-typescript-eddy/releases)<space><space>
[![documentation](https://img.shields.io/badge/documentation-yes-brightgreen.svg)](#overview)

</div>

<br><br>

## Overview

Advanced template for React TypeScript.

- **[Structure](#structure)**
- **[Dependencies](#dependencies)**
- **[Husky](#husky)**
- **[ESLint](#eslint)**
- **[Author](#author)**
- **[License](#license)**
- **[Show your support](#show-your-support)**


<br><br>

## Structure

- ```@types``` - Application types
- ```components``` - Application components
- ```config``` - Configuration files
- ```hooks``` - Custom hooks
- ```images``` - Application Images
- ```layouts``` - Auth and Default layouts
- ```pages``` - Application pages
- ```routes``` - Route configuration
- ```services``` - API configuration
- ```store``` - Redux and Redux Saga configuration
- ```styles``` - Global styles and application themes
- ```utils``` - Useful files
- ```validators``` - Yup Validation
- ```App.js``` - Global imports
- ```index.tsx``` - Render application

<br><br>

## Dependencies
  
Remember to execute the command ```yarn upgrade``` to update with dependencies.

**Normal:**

- axios
- history
- immer
- json-server
- react
- react-dom
- react-redux
- react-router-dom
- react-scripts
- react-toastify
- reactotron-react-js
- reactotron-redux
- reactotron-redux-saga
- redux
- redux-devtools-extension
- redux-persist
- redux-saga
- styled-components
- web-vitals
- yup

**Dev Dependencies:**

- @types/*
- typescript
- babel-plugin-root-import
- customize-cra
- react-app-rewired

<br><br>

## Husky

For standardization of commits for GitHub within a project, using the library **[Husky](https://github.com/typicode/husky)**, together with libraries **[commitizen](https://github.com/commitizen/cz-cli)**, **[lint-staged](https://github.com/okonet/lint-staged)**, **[@commitlint/config-conventional](https://www.npmjs.com/package/@commitlint/config-conventional)** and **[@commitlint/cli](https://www.npmjs.com/package/@commitlint/cli)**.

Add the Hunsky library in development.

```sh
yarn add husky -D
```

Also add the following libraries below, under development.

```sh
yarn add commitizen lint-staged @commitlint/config-conventional @commitlint/cli -D
```

Paste the excerpt below into your file ```package.json```.

```json
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged",
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS",
      "prepare-commit-msg": "exec < /dev/tty && git cz --hook || true"
    }
  },
  "lint-staged": {
    "*.{ts,tsx}": [
      "prettier --config prettier.config.js --write",
      "eslint --fix --ignore-pattern '!.eslintrc.json'",
      "git add -u"
    ]
  },
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
}
```

Create a file called ```commitlint.config.js``` at the root of the project and paste the code below.

```javascript
module.exports = { extends: ['@commitlint/config-conventional'] };
```

After these settings, just type ```git add .``` and ```git commit``` on your terminal and Husky will take action.

Below are listed possible questions that Husky will ask.

1. Select the type of change that you're committing: (Use arrow keys)
- ```feat```:         A new feature
- ```fix```:          A bug fix
- ```docs```:         Documentation only changes
- ```style```:        Changes that do not affect the meaning of the code (white-space, for matting, missing semi-colons, etc)
- ```refactor```:     A code change that neither fixes a bug nor adds a feature
- ```perf```:         A code change that improves performance
- ```test```:         Adding missing tests or correcting existing tests
- ```build```:        Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- ```ci```:           Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- ```chore```:        Other changes that don't modify src or test files
- ```revert```:       Reverts a previous commit

2. What is the scope of this change (e.g. component or file name): (press enter to skip)
3. Write a short, imperative tense description of the change (max 66 chars):
4. Provide a longer description of the change: (press enter to skip)
5. Are there any breaking changes? (y/N)
	- A BREAKING CHANGE commit requires a body. Please enter a longer description of the commit itself:
	- Describe the breaking changes:
6. Does this change affect any open issues? (y/N)
	- Add issue references (e.g. "fix #123", "re #123".):

<br><br>

## ESLint

For better standardization of codes within the project, we use the **[ESLint](https://eslint.org/)** and **[Prettier](https://prettier.io/)** libraries.

Follow the installation instructions on the link below: <br>
**[Eslint, Prettier and EditorConfig](https://www.notion.so/Padr-es-de-projeto-com-ESLint-Prettier-e-EditorConfig-0b57b47a24724c859c0cf226aa0cc3a7)**

<br><br>

## Author

👤 **[Eduardo Mauricio](https://github.com/therealeddy)**

## License

MIT © **[React TypeScript](LICENSE)**

## Show your support

Give a ⭐️ if this project helped you!
