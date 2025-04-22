## Playwright MCP

### playwright_navigate

This tool navigates to a URL

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "url": {
      "type": "string",
      "description": "URL to navigate to the website specified"
    },
    "browserType": {
      "type": "string",
      "description": "Browser type to use (chromium, firefox, webkit). Defaults to chromium",
      "enum": [
        "chromium",
        "firefox",
        "webkit"
      ]
    },
    "width": {
      "type": "number",
      "description": "Viewport width in pixels (default: 1280)"
    },
    "height": {
      "type": "number",
      "description": "Viewport height in pixels (default: 720)"
    },
    "timeout": {
      "type": "number",
      "description": "Navigation timeout in milliseconds"
    },
    "waitUntil": {
      "type": "string",
      "description": "Navigation wait condition"
    },
    "headless": {
      "type": "boolean",
      "description": "Run browser in headless mode (default: false)"
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
<server_name>github.com/executeautomation/mcp-playwright</server_name>
<tool_name>playwright_navigate</tool_name>
<arguments>
{
  "url": "https://example.com"
}
</arguments>
</use_mcp_tool>
```

### playwright_screenshot

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
    },
    "storeBase64": {
      "type": "boolean",
      "description": "Store screenshot in base64 format (default: true)"
    },
    "fullPage": {
      "type": "boolean",
      "description": "Store screenshot of the entire page (default: false)"
    },
    "savePng": {
      "type": "boolean",
      "description": "Save screenshot as PNG file (default: false)"
    },
    "downloadsDir": {
      "type": "string",
      "description": "Custom downloads directory path (default: user's Downloads folder)"
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
<server_name>github.com/executeautomation/mcp-playwright</server_name>
<tool_name>playwright_screenshot</tool_name>
<arguments>
{
  "name": "example",
  "selector": "h1"
}
</arguments>
</use_mcp_tool>
