## Brave Search MCP

### brave_web_search

This tool performs a web search using the Brave Search API.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "Search query (max 400 chars, 50 words)"
    },
    "count": {
      "type": "number",
      "description": "Number of results (1-20, default 10)",
      "default": 10
    },
    "offset": {
      "type": "number",
      "description": "Pagination offset (max 9, default 0)",
      "default": 0
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
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/brave-search</server_name>
<tool_name>brave_web_search</tool_name>
<arguments>
{
  "query": "What is the capital of France?"
}
</arguments>
</use_mcp_tool>
```

### brave_local_search

This tool searches for local businesses and places using Brave's Local Search API.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "Local search query (e.g. 'pizza near Central Park')"
    },
    "count": {
      "type": "number",
      "description": "Number of results (1-20, default 5)",
      "default": 5
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
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/brave-search</server_name>
<tool_name>brave_local_search</tool_name>
<arguments>
{
  "query": "pizza near me"
}
</arguments>
</use_mcp_tool>
