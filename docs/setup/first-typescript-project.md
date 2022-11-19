---
sidebar_position: 1
---

# Our First Typescript Program

In this video, we will be talking about

- Creating our first typescript program
- how Typescript compiler compile ts codes into javascript
- explore more about the program's compiled output and type declaration files
  In this chapter video, we gonna be talking about

## Installing typescript globally

First, let's install typescript globally on your machine.

```bash
npm install -g typescript
```

Then, check if the installation is successfully by running

```bash
tsc -v
# Version 4.9.3
```

## Compiling typescript file

Let's create a file named `hello.ts` and write the following code

```ts title="hello.ts"
function hello(name: string) {
  console.log(`Hello ${name}`);
}
```

Then open up the terminal and you can run `tsc hello.ts` to compile the file. You will see a new file named `hello.js` is created. This is the compiled javascript file.

```js title="hello.js"
function hello(name) {
  console.log("Hello ".concat(name));
}
```

You can also specify the output file as you desire.

```bash
tsc hello.ts --outFile app.js
```

You can also enable `watch` mode to automatically compile the file when you save it.

```bash
tsc hello.ts --watch
```

## Setting up a typescript project

For this series, I will be setting up a simple typescript project with some setups and configs.

- package.json
- tsconfig.json
- src/index.ts

Start by running `npm init -y` to create a package.json file.

```json title="package.json"
{
  "name": "ts-for-dev",
  "version": "1.0.0",
  "description": "",
  "main": "index.ts",
  "scripts": {
    "dev": "tsc --watch --preserveWatchOutput"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "typescript": "^4.9.3"
  }
}
```

Then, install typescript as a dev dependency.

```bash
npm install -D typescript
```

Then, create a `tsconfig.json` file and add the following code.

```json title="tsconfig.json"
{
  "compilerOptions": {
    "outDir": "dist", // where to produce the compiled files
    "target": "ES3" // which level of JS support to target
  },
  "include": ["src"] // which files to compile
}
```

Then, create a `src` folder and create a `index.ts` file.

```ts title="src/index.ts"
function hello(name: string) {
  console.log(`Hello ${name}`);
}
```

- There is only one dependency in our package.json file, which is typescript.
- We also added a `dev` script to invoke the typescripe compiler in watch mode.

## Running the project

To run the project, you can run `npm run dev` to start the typescript compiler in watch mode.

```bash
npm run dev
```

You should see something like this in your terminal.

```bash
> [10:50:08 PM] Starting compilation in watch mode...
> [10:50:09 PM] Found 0 errors. Watching for file changes.
```

`--preserveWatchOutput` is used to preserve the output log in the terminal.
