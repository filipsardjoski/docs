# Interhuman Documentation

This repository contains the documentation for Interhuman AI.

## Prerequisites

**Node.js** (version 22 or higher) is required. We recommend using `nvm` (Node Version Manager).

### Installing Node.js

1.  **Install nvm** (if you haven't already):
    See [nvm-sh/nvm](https://github.com/nvm-sh/nvm#installing-and-updating) for installation commands.

2.  **Install/Use Node.js**:
    Run the following in the project root to install and use the version specified in `.nvmrc`:
    ```bash
    nvm install
    nvm use
    ```

## Local Development

To run the documentation locally, you need to install the Mintlify CLI.

### 1. Install Mintlify CLI

Install the CLI globally using npm:

```bash
npm i -g mintlify
```

### 2. Run Development Server

Start the local development server:

```bash
mintlify dev
```

This will start a local server, usually at `http://localhost:3000`.

### 3. Usage

Once the server is running, you can:
- Open your browser to the local URL (e.g., `http://localhost:3000`).
- Edits to the documentation files will live reload in the browser.
- Verify the content and layout before pushing changes.

### More Information

- [Mintlify Documentation](https://www.mintlify.com/docs/quickstart)