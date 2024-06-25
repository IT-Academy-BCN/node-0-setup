## Step 5: Setup Jest

### What is Jest?

Jest is a delightful JavaScript testing framework with a focus on simplicity. It works with projects using Babel, TypeScript, Node.js, React, Angular, Vue.js, and Svelte. Jest provides a great developer experience with features like powerful mocking capabilities, a simple API, and excellent performance.

### Why Use Jest?

- **Ease of Use**: Simple and easy-to-configure testing framework.
- **Fast and Reliable**: Provides fast and reliable tests with features like parallel test execution.
- **Comprehensive**: Comes with built-in assertion library, mocking capabilities, and code coverage.

### Installation Instructions

1. **Initialize Your Project**:
   - If you haven't already, initialize your Node.js project:
     ```sh
     npm init -y
     ```

2. **Install Jest Locally**:
   - Install Jest and the necessary TypeScript support as dev dependencies:
     ```sh
     npm install --save-dev jest ts-jest @types/jest
     ```

3. **Create a Jest Configuration File**:
   - Create a `jest.config.js` file in the root of your project to configure Jest:
     ```javascript
     module.exports = {
       preset: 'ts-jest',
       testEnvironment: 'node',
       testMatch: ['**/?(*.)+(spec|test).[jt]s?(x)']
     };
     ```

### Basic Setup

Your `jest.config.js` file might look something like this:

```javascript
module.exports = {
  preset: 'ts-jest',
  testEnvironment: 'node',
  testMatch: ['**/?(*.)+(spec|test).[jt]s?(x)']
};
```

### Example Project Structure

Create a basic project structure:
```plaintext
my-project/
├── src/
│   ├── index.ts
│   └── index.test.ts
├── jest.config.js
├── .prettierrc
├── .prettierignore
├── tsconfig.json
└── package.json
```

### Example Files

1. **`src/index.ts`**:
```typescript
export const sum = (a: number, b: number): number => a + b;
```

2. **`src/index.test.ts`**:
```typescript
import { sum } from './index';

describe('sum', () => {
  it('adds 1 + 2 to equal 3', () => {
    expect(sum(1, 2)).toBe(3);
  });
});
```

3. **`package.json`**:
```json
{
  "name": "my-project",
  "version": "1.0.0",
  "main": "dist/index.js",
  "scripts": {
    "start": "ts-node src/index.ts",
    "build": "tsc",
    "format": "prettier --write \"src/**/*.ts\"",
    "lint": "eslint . --ext .ts",
    "test": "jest"
  },
  "devDependencies": {
    "typescript": "^4.0.0",
    "ts-node": "^10.0.0",
    "prettier": "^2.0.0",
    "eslint": "^7.0.0",
    "@typescript-eslint/parser": "^4.0.0",
    "@typescript-eslint/eslint-plugin": "^4.0.0",
    "jest": "^27.0.0",
    "ts-jest": "^27.0.0",
    "@types/jest": "^27.0.0"
  }
}
```

### Running Jest

To run Jest tests, you can use the following command:
```sh
npm test
```

