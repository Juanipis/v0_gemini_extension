# v0.dev Gemini CLI Extension

An extension for the [Gemini CLI](https://geminicli.com) that integrates [v0.dev](https://v0.dev) using the official Model Context Protocol (MCP) server.

## Features

- **v0.dev Integration:** Directly interact with v0's AI design and code generation capabilities from your CLI.
- **Secure API Key Management:** Safely stores your `V0_API_KEY` in the system keychain.
- **Tool Access:** Enables Gemini to create, get, search, and message v0 chats on your behalf.

## Installation

```bash
gemini extensions install https://github.com/juanipis/v0-gemini-extension
```

*Note: Replace the URL with your actual repository URL.*

During installation, you will be prompted to provide your **v0 API Key**. You can find your API key in your [v0.dev account settings](https://v0.dev/settings).

## Configuration

To update your v0 API Key at any time:

```bash
gemini extensions config v0-gemini-extension
```

## Usage

Once installed, you can ask Gemini to perform v0-related tasks:

- "Start a new v0 chat for a React auth component."
- "Show me the details of my v0 chat with ID `abc123`."
- "Search my v0 history for 'dashboard'."
- "Refine the v0 chat `abc123` to use Tailwind v4."

## Requirements

- [Node.js](https://nodejs.org/) installed on your machine.
- [Gemini CLI](https://geminicli.com) installed.
- A valid [v0.dev API Key](https://v0.dev/settings).

## License

MIT
