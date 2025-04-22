## Qdrant MCP

### qdrant-store

This tool keeps the memory for later use, when you are asked to remember something.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "information": {
      "title": "Information",
      "type": "string"
    },
    "metadata": {
      "additionalProperties": true,
      "default": null,
      "title": "Metadata",
      "type": "object"
    }
  },
  "required": [
    "information"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/qdrant/mcp-server-qdrant</server_name>
<tool_name>qdrant-store</tool_name>
<arguments>
{
  "information": "The capital of France is Paris."
}
</arguments>
</use_mcp_tool>
```

### qdrant-find

This tool looks up memories in Qdrant.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "title": "Query",
      "type": "string"
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
<server_name>github.com/qdrant/mcp-server-qdrant</server_name>
<tool_name>qdrant-find</tool_name>
<arguments>
{
  "query": "capital of France"
}
</arguments>
</use_mcp_tool>
