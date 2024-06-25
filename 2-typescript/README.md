## Step 2: Setup TypeScript, ts-node, and tsconfig

### What is TypeScript?

TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. It offers static typing, which helps catch errors early through type checking and improves the development experience with features like autocompletion and navigation.

### What is `ts-node`?

`ts-node` is a TypeScript execution engine for Node.js. It allows you to run TypeScript code directly without pre-compiling, making it easier to work with TypeScript in a Node.js environment.

### Installation Instructions

1. **Initialize Your Project**:
   - Open your terminal, navigate to your project directory, and run the following command to initialize a new Node.js project:
     ```sh
     npm init -y
     ```

2. **Install TypeScript and ts-node Locally**:
   - Install TypeScript and `ts-node` as dev dependencies:
     ```sh
     npm install --save-dev typescript ts-node
     ```

3. **Initialize a TypeScript Project**:
   - Create a `tsconfig.json` file by running:
     ```sh
     npx tsc --init
     ```

### Basic Setup

Your `tsconfig.json` file will look something like this:

```json
{
  "compilerOptions": {
    "target": "es6",                                  /* Specify ECMAScript target version */
    "module": "commonjs",                             /* Specify module code generation */
    "strict": true,                                   /* Enable all strict type-checking options */
    "esModuleInterop": true,                          /* Enable compatibility with CommonJS and ES Modules */
    "skipLibCheck": true,                             /* Skip type checking of all declaration files */
    "outDir": "./dist",                               /* Redirect output structure to the directory */
    "rootDir": "./src"                                /* Specify the root directory of input files */
  },
  "include": ["src/**/*"]                             /* Include all .ts files in the src directory */
}
```

### Running TypeScript Code

To run TypeScript code using `ts-node`, you can create a simple TypeScript file (e.g., `index.ts`) in your `src` directory and run it using the following command:

```sh
npx ts-node src/index.ts
```

This will execute your TypeScript code directly without the need for compilation.

You have an example folder. Try to create a new one, running, and building a simple TypeScript project.