# tsnode-boilerplate

**tsnode-boilerplate** is a simple boilerplate designed for TypeScript and Node.js projects. It provides you with a foundation to quickly start building your applications using TypeScript and Node.js.

## Getting Started

To get started with **tsnode-boilerplate**, follow these steps:

1. Clone this repository to your local machine or download the source code.

2. Install the necessary dependencies by running the following command:

   ```
   npm install
   ```

3. You can use the following npm scripts to build and run your project:

   - `npm run build`: This script cleans the `dist` directory and compiles your TypeScript code to JavaScript.
   - `npm run dev`: Use this script to run your application in development mode using `nodemon`, which automatically restarts your server when changes are detected.
   - `npm run serve`: This script runs your compiled application from the `dist` directory using Node.js.

## Project Structure

The structure of the project is designed to keep your code organized and maintainable:

- `src/`: This directory contains your TypeScript source code files.
  - `index.ts`: The entry point of your application. This file provides a simple way to test the project by creating a basic HTTP server and responding with a JSON message.

```typescript
import http from "http";

export const server = http.createServer((req, res) => {
  res.writeHead(200, { "Content-Type": "application/json" });
  res.end(
    JSON.stringify({
      data: "Hello world!"
    })
  );
});

server.listen(3000, () => {
  console.log("Server running on http://localhost:3000/");
});
```

## Dependencies

The following dependencies are included in this boilerplate:

- `@types/node`: TypeScript type definitions for Node.js.
- `nodemon`: A development utility that monitors for changes and restarts your server.
- `rimraf`: A cross-platform tool for removing files and directories.
- `ts-node`: TypeScript execution environment for Node.js.
- `typescript`: TypeScript programming language.

## Author

This boilerplate is created and maintained by SpicoDer.

## License

This project is licensed under the ISC License.

Feel free to customize and extend this boilerplate to suit your project's needs. Happy coding!
