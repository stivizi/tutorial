## Memory MCP

### create_entities

This tool creates multiple new entities in the knowledge graph

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "entities": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "name": {
            "type": "string",
            "description": "The name of the entity"
          },
          "entityType": {
            "type": "string",
            "description": "The type of the entity"
          },
          "observations": {
            "type": "array",
            "items": {
              "type": "string"
            },
            "description": "An array of observation contents associated with the entity"
          }
        },
        "required": [
          "name",
          "entityType",
          "observations"
        ]
      }
    }
  },
  "required": [
    "entities"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/memory</server_name>
<tool_name>create_entities</tool_name>
<arguments>
{
  "entities": [
    {
      "name": "Paris",
      "entityType": "City",
      "observations": ["Capital of France"]
    }
  ]
}
</arguments>
</use_mcp_tool>
```

### search_nodes

This tool searches for nodes in the knowledge graph based on a query

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "The search query to match against entity names, types, and observation content"
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
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/memory</server_name>
<tool_name>search_nodes</tool_name>
<arguments>
{
  "query": "Paris"
}
</arguments>
</use_mcp_tool>
