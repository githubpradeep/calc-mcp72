# MCP Calculator Server

    A simple Model Context Protocol (MCP) server that provides calculator functions.

    ## Overview

    This MCP server implements basic arithmetic operations as tools that can be called by Large Language Models (LLMs) through the Model Context Protocol.

    ## Features

    - Addition: Add two numbers together
    - Subtraction: Subtract one number from another
    - Multiplication: Multiply two numbers together
    - Division: Divide one number by another (with validation to prevent division by zero)

    ## Installation

    ```bash
    npm install
    ```

    ## Usage

    ### Running the server

    ```bash
    npm run dev
    ```

    This starts the MCP server in development mode with auto-restart on file changes.

    For production:

    ```bash
    npm start
    ```

    ### Testing with MCP Inspector

    You can test the server using the MCP Inspector:

    ```bash
    npx @modelcontextprotocol/inspector node src/index.js
    ```

    This will open a web interface where you can:
    - View available tools
    - Test each calculator function with custom inputs
    - See the responses from the server

    ## Available Tools

    | Tool | Parameters | Description |
    |------|------------|-------------|
    | add | a: number, b: number | Adds two numbers |
    | subtract | a: number, b: number | Subtracts b from a |
    | multiply | a: number, b: number | Multiplies two numbers |
    | divide | a: number, b: number (non-zero) | Divides a by b |

    ## Example Usage

    When connected to an LLM through MCP, the model can call these tools to perform calculations. For example:

    - To add 5 and 3, the LLM would call the `add` tool with parameters `a: 5, b: 3`
    - To divide 10 by 2, the LLM would call the `divide` tool with parameters `a: 10, b: 2`

    ## License

    MIT
