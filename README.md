# MCP-researcher Server

Your own research assistant inside of Cline! Utilizes Perplexity's new Sonar Pro API to get docs, create up-to-date api routes, and check deprecated code while you create features with Cline. 

<a href="https://glama.ai/mcp/servers/g1i6ilg8sl"><img width="380" height="200" src="https://glama.ai/mcp/servers/g1i6ilg8sl/badge" alt="MCP-researcher Server MCP server" /></a>

## Tools

### 1. [Search](https://github.com/DaInfernalCoder/researcher-mcp/blob/main/examples/search.md)
Performs general search queries to get comprehensive information on any topic. The example shows how to use different detail levels (brief, normal, detailed) to get tailored responses.

### 2. [Get Documentation](https://github.com/DaInfernalCoder/researcher-mcp/blob/main/examples/find-apis.md)
Retrieves documentation and usage examples for specific technologies, libraries, or APIs. The example demonstrates getting comprehensive documentation for React hooks, including best practices and common pitfalls.

### 3. [Find APIs](https://github.com/DaInfernalCoder/researcher-mcp/blob/main/examples/find-apis.md)
Discovers and evaluates APIs that could be integrated into a project. The example shows finding payment processing APIs with detailed analysis of features, pricing, and integration complexity.

### 4. [Check Deprecated Code](https://github.com/DaInfernalCoder/researcher-mcp/blob/main/examples/check-deprecated-code.md)
Analyzes code for deprecated features or patterns, providing migration guidance. The example demonstrates checking React class components and lifecycle methods for modern alternatives.


## Installation

1. First install Node.js if not already installed (from nodejs.org)

2. Clone the repo

- git clone https://github.com/DaInfernalCoder/researcher-mcp perplexity-server 

- cd perplexity-server

3. Install dependencies and build:
npm install

4. Get a Perplexity API key from [https://www.perplexity.ai/settings/api](https://www.perplexity.ai/settings/api)

5. Create the MCP settings file in the appropriate location for your OS:
macOS: ~/Library/Application Support/Cursor/User/globalStorage/saoudrizwan.claude-dev/settings/cline_mcp_settings.json
Windows: %APPDATA%\Cursor\User\globalStorage\saoudrizwan.claude-dev\settings\cline_mcp_settings.json
Linux: ~/.config/Cursor/User/globalStorage/saoudrizwan.claude-dev/settings/cline_mcp_settings.json

5. To use with Claude Desktop, add the server config:

On MacOS: `~/Library/Application Support/Claude/claude_desktop_config.json`
On Windows: `%APPDATA%/Claude/claude_desktop_config.json`

6. To use with Cline, add into mcpServers: 

```json
{
  "mcpServers": {
    "perplexity-server": {
      "command": "node",
      "args": [
        "[path/to/researcher-mcp/index.js]"
      ],
      "env": {
        "PERPLEXITY_API_KEY": ""
      },
      "disabled": false,
      "autoApprove": [
        "search",
        "get_documentation",
        "find_apis",
        "check_deprecated_code"
      ]
    }
  }
}
```

7. Build the server: 
npm run build

Make sure to:
- Replace /absolute/path/to with the actual path where you cloned the repository
- Replace your-api-key-here with your Perplexity API key
- Keep the same autoApprove settings for consistent behavior

