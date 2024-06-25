## Step 4: Setup Prettier

### What is Prettier?

Prettier is an opinionated code formatter that enforces a consistent style by parsing your code and re-printing it with its own rules. It helps maintain a uniform code style across your project, making it easier to read and collaborate.

### Why Use Prettier?

- **Consistency**: Ensures your code adheres to a consistent style, making it easier to read and maintain.
- **Focus on Code Logic**: Frees you from worrying about code formatting, allowing you to focus on writing code logic.
- **Collaboration**: Improves collaboration by reducing diffs in pull requests and making code reviews more focused on logic than style.

### Installation Instructions

1. **Initialize Your Project**:
   - If you haven't already, initialize your Node.js project:
     ```sh
     npm init -y
     ```

2. **Install Prettier Locally**:
   - Install Prettier as a dev dependency:
     ```sh
     npm install --save-dev prettier
     ```

3. **Create a Prettier Configuration File**:
   - Create a `.prettierrc` file in the root of your project to configure Prettier:
     ```json
     {
       "semi": true,
       "singleQuote": true,
       "printWidth": 80,
       "tabWidth": 2
     }
     ```

4. **Create a Prettier Ignore File**:
   - Create a `.prettierignore` file in the root of your project to specify files and directories that Prettier should ignore:
     ```
     node_modules
     dist
     ```

### Example Project Structure

Create a basic project structure:

my-project/
├── src/
│ └── index.ts
├── .prettierrc
├── .prettierignore
├── tsconfig.json
└── package.json


### Example Files

1. **`src/index.ts`**:
```typescript
const greeting: string = 'Hello, Prettier!';
console.log(greeting);
```

2. **`package.json`**:
```json
{
  "name": "my-project",
  "version": "1.0.0",
  "main": "dist/index.js",
  "scripts": {
    "start": "ts-node src/index.ts",
    "build": "tsc",
    "format": "prettier --write \"src/**/*.ts\""
  },
  "devDependencies": {
    "typescript": "^4.0.0",
    "ts-node": "^10.0.0",
    "prettier": "^2.0.0"
  }
}
```

### Running Prettier

To format your TypeScript files using Prettier, you can use the following command:

```sh
npx prettier --write "src/**/*.ts"
```

You can also add a script to your `package.json` to run Prettier:

```json
{
  "scripts": {
    "format": "prettier --write \"src/**/*.ts\""
  }
}
```

Then, you can run Prettier using:

```sh
npm run format
```

This will format your TypeScript files based on the rules defined in your `.prettierrc` configuration file.

### Running Prettier with vscode on save

To run Prettier automatically when you save a file in Visual Studio Code, you can install the Prettier extension and add the following settings to your workspace or user settings:

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```