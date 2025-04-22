## Firecrawl MCP

### firecrawl_scrape

This tool scrapes a single webpage with advanced options for content extraction.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "url": {
      "type": "string",
      "description": "The URL to scrape"
    },
    "formats": {
      "type": "array",
      "items": {
        "type": "string",
        "enum": [
          "markdown",
          "html",
          "rawHtml",
          "screenshot",
          "links",
          "screenshot@fullPage",
          "extract"
        ]
      },
      "description": "Content formats to extract (default: ['markdown'])"
    },
    "onlyMainContent": {
      "type": "boolean",
      "description": "Extract only the main content, filtering out navigation, footers, etc."
    },
    "includeTags": {
      "type": "array",
      "items": {
        "type": "string"
      },
      "description": "HTML tags to specifically include in extraction"
    },
    "excludeTags": {
      "type": "array",
      "items": {
        "type": "string"
      },
      "description": "HTML tags to exclude from extraction"
    },
    "waitFor": {
      "type": "number",
      "description": "Time in milliseconds to wait for dynamic content to load"
    },
    "timeout": {
      "type": "number",
      "description": "Maximum time in milliseconds to wait for the page to load"
    },
    "actions": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "type": {
            "type": "string",
            "enum": [
              "wait",
              "click",
              "screenshot",
              "write",
              "press",
              "scroll",
              "scrape",
              "executeJavascript"
            ],
            "description": "Type of action to perform"
          },
          "selector": {
            "type": "string",
            "description": "CSS selector for the target element"
          },
          "milliseconds": {
            "type": "number",
            "description": "Time to wait in milliseconds (for wait action)"
          },
          "text": {
            "type": "string",
            "description": "Text to write (for write action)"
          },
          "key": {
            "type": "string",
            "description": "Key to press (for press action)"
          },
          "direction": {
            "type": "string",
            "enum": [
              "up",
              "down"
            ],
            "description": "Scroll direction"
          },
          "script": {
            "type": "string",
            "description": "JavaScript code to execute"
          },
          "fullPage": {
            "type": "boolean",
            "description": "Take full page screenshot"
          }
        },
        "required": [
          "type"
        ]
      },
      "description": "List of actions to perform before scraping"
    },
    "extract": {
      "type": "object",
      "properties": {
        "schema": {
          "type": "object",
          "description": "Schema for structured data extraction"
        },
        "systemPrompt": {
          "type": "string",
          "description": "System prompt for LLM extraction"
        },
        "prompt": {
          "type": "string",
          "description": "User prompt for LLM extraction"
        }
      },
      "description": "Configuration for structured data extraction"
    },
    "mobile": {
      "type": "boolean",
      "description": "Use mobile viewport"
    },
    "skipTlsVerification": {
      "type": "boolean",
      "description": "Skip TLS certificate verification"
    },
    "removeBase64Images": {
      "type": "boolean",
      "description": "Remove base64 encoded images from output"
    },
    "location": {
      "type": "object",
      "properties": {
        "country": {
          "type": "string",
          "description": "Country code for geolocation"
        },
        "languages": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Language codes for content"
        }
      },
      "description": "Location settings for scraping"
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
<server_name>github.com/mendableai/firecrawl-mcp-server</server_name>
<tool_name>firecrawl_scrape</tool_name>
<arguments>
{
  "url": "example.com",
  "formats": ["markdown"]
}
</arguments>
</use_mcp_tool>
```

### firecrawl_search

This tool searches and retrieves content from web pages with optional scraping.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "Search query string"
    },
    "limit": {
      "type": "number",
      "description": "Maximum number of results to return (default: 5)"
    },
    "lang": {
      "type": "string",
      "description": "Language code for search results (default: en)"
    },
    "country": {
      "type": "string",
      "description": "Country code for search results (default: us)"
    },
    "tbs": {
      "type": "string",
      "description": "Time-based search filter"
    },
    "filter": {
      "type": "string",
      "description": "Search filter"
    },
    "location": {
      "type": "object",
      "properties": {
        "country": {
          "type": "string",
          "description": "Country code for geolocation"
        },
        "languages": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Language codes for content"
        }
      },
      "description": "Location settings for search"
    },
    "scrapeOptions": {
      "type": "object",
      "properties": {
        "formats": {
          "type": "array",
          "items": {
            "type": "string",
            "enum": [
              "markdown",
              "html",
              "rawHtml"
            ]
          },
          "description": "Content formats to extract from search results"
        },
        "onlyMainContent": {
          "type": "boolean",
          "description": "Extract only the main content from results"
        },
        "waitFor": {
          "type": "number",
          "description": "Time in milliseconds to wait for dynamic content"
        }
      },
      "description": "Options for scraping search results"
    }
  },
  "required": [
    "query"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/mendableai/firecrawl-mcp-server</server_name>
<tool_name>firecrawl_search</tool_name>
<arguments>
{
  "query": "site:example.com"
}
</arguments>
</use_mcp_tool>
