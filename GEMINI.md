# v0.dev Gemini Extension

This extension enables the AI assistant to interact with v0.dev, Vercel's AI-powered design and code generation platform, using the official v0 MCP server.

## Overview

The v0 MCP server allows you to:
- Create new v0 chats for React components, designs, and more.
- Get details and code from existing v0 chats.
- Search through your past v0 chats.
- Send follow-up messages to refine existing chats.

## Available Tools

The following tools are provided by the `v0` MCP server. Always use these when the user asks to "create in v0", "ask v0", or interact with v0.dev.

### `create_chat`
Creates a new v0 chat with a specified prompt.
- **When to use:** When the user wants to start a new design or component on v0.dev.
- **Example:** "Create a v0 chat for a modern dashboard with a sidebar and dark mode support."

### `get_chat`
Retrieves the details of a specific v0 chat by its ID.
- **When to use:** To fetch the code or design state of an existing chat.
- **Example:** "Show me the details of v0 chat `abc123`."

### `search_chats`
Searches through the user's v0 chats.
- **When to use:** To find relevant previous work on v0.
- **Example:** "Find my v0 chats about React hooks or auth components."

### `send_message`
Sends a new message to an existing v0 chat.
- **When to use:** To refine an existing v0 design or ask questions about it.
- **Example:** "Send a message to v0 chat `abc123` asking to change the primary color to blue."

## Best Practices

- **Code Integration:** After creating or fetching a chat, v0 will provide code. You can then use other tools (like `write_file`) to save that code into the local project if requested.
- **Context:** If the user provides an image or complex requirements, ensure the prompt passed to `create_chat` or `send_message` is detailed and clear.
- **API Key:** The extension handles the `V0_API_KEY` automatically. If the tools fail with authentication errors, remind the user to check their API key using `gemini extensions config v0-gemini-extension`.
