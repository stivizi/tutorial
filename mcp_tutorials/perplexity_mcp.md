## Perplexity MCP

### search

This tool performs a general search query to get comprehensive information on any topic.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "The search query or question"
    },
    "detail_level": {
      "type": "string",
      "description": "Optional: Desired level of detail (brief, normal, detailed)",
      "enum": [
        "brief",
        "normal",
        "detailed"
      ]
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
<server_name>github.com/pashpashpash/perplexity-mcp</server_name>
<tool_name>search</tool_name>
<arguments>
{
  "query": "What is the capital of France?"
}
</arguments>
</use_mcp_tool>
```

### chat_perplexity

This tool maintains ongoing conversations with Perplexity AI.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "message": {
      "type": "string",
      "description": "The message to send to Perplexity AI"
    },
    "chat_id": {
      "type": "string",
      "description": "Optional: ID of an existing chat to continue. If not provided, a new chat will be created."
    }
  },
  "required": [
    "message"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/pashpashpash/perplexity-mcp</server_name>
<tool_name>chat_perplexity</tool_name>
<arguments>
{
  "message": "Hello, Perplexity!"
}
</arguments>
</use_mcp_tool>
