## Google Drive MCP

### search

This tool searches for files in Google Drive

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "Search query"
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
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/gdrive</server_name>
<tool_name>search</tool_name>
<arguments>
{
  "query": "My Document"
}
</arguments>
</use_mcp_tool>
