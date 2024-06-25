## Step 3: Setup ESLint

### What is ESLint?

[ESLint](https://eslint.org/) is a tool for identifying and fixing problems in your JavaScript and TypeScript code. It helps maintain code quality and consistency by enforcing a set of coding standards and highlighting potential errors and bad practices.

### Why Use ESLint?

- **Code Quality**: Ensures your code adheres to a specified set of rules, improving readability and maintainability.
- **Error Prevention**: Catches common coding errors and potential bugs before they cause problems.
- **Consistency**: Enforces a consistent coding style across your project.

### Installation Instructions

1. **Initialize Your Project**:
   - If you haven't already, initialize your Node.js project:
     ```sh
     npm init -y
     ```

2. **Install ESLint Locally**:
   - Install ESLint as a dev dependency:
     ```sh
     npm install --save-dev eslint
     ```

3. **Set Up ESLint Configuration**:
   - Create an ESLint configuration file by running:
     ```sh
     npx eslint --init
     ```

   - Follow the prompts to configure ESLint for your project. For a basic setup, you can choose the following options:
     - How would you like to use ESLint? (To check syntax, find problems, and enforce code style)
     - What type of modules does your project use? (CommonJS)
     - Which framework does your project use? (None)
     - Does your project use TypeScript? (Yes)
     - Where does your code run? (Node)
     - What format do you want your config file to be in? (JSON)

   - This will create a `.eslintrc.json` file in your project.

### Basic Setup

Your `.eslintrc.json` file might look something like this:

```json
{
  "env": {
    "node": true,
    "es2021": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": [
    "@typescript-eslint"
  ],
  "rules": {
    "indent": ["error", 2],
    "quotes": ["error", "single"],
    "semi": ["error", "always"]
  }
}
```

### Running ESLint

To run ESLint on your TypeScript files, you can use the following command:

```sh
npx eslint src/**/*.ts
```

This will analyze your TypeScript files and report any errors or warnings based on the rules defined in your ESLint configuration.

There may be errors or warnings reported by ESLint. You can fix them manually or use ESLint's autofix feature to automatically correct some issues.

There may be also missconfiguration, please try to fix them and run the command again.

### Running ESLint with vscode on save

To run ESLint automatically when you save a file in Visual Studio Code, you can install the ESLint extension and add the following settings to your workspace or user settings:

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```