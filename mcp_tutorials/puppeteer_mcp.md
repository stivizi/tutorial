## Puppeteer MCP

### puppeteer_navigate

This tool navigates to a URL

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "url": {
      "type": "string",
      "description": "URL to navigate to"
    },
    "launchOptions": {
      "type": "object",
      "description": "PuppeteerJS LaunchOptions. Default null. If changed and not null, browser restarts. Example: { headless: true, args: ['--no-sandbox'] }"
    },
    "allowDangerous": {
      "type": "boolean",
      "description": "Allow dangerous LaunchOptions that reduce security. When false, dangerous args like --no-sandbox will throw errors. Default false."
    }
  },
  "required": [
    "url"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/puppeteer</server_name>
<tool_name>puppeteer_navigate</tool_name>
<arguments>
{
  "url": "https://example.com"
}
</arguments>
</use_mcp_tool>
```

### puppeteer_screenshot

This tool takes a screenshot of the current page or a specific element

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "Name for the screenshot"
    },
    "selector": {
      "type": "string",
      "description": "CSS selector for element to screenshot"
    },
    "width": {
      "type": "number",
      "description": "Width in pixels (default: 800)"
    },
    "height": {
      "type": "number",
      "description": "Height in pixels (default: 600)"
    }
  },
  "required": [
    "name"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/puppeteer</server_name>
<tool_name>puppeteer_screenshot</tool_name>
<arguments>
{
  "name": "example",
  "selector": "h1"
}
</arguments>
</use_mcp_tool>
