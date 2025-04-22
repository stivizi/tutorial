## Apify Actors MCP

### search-actor

This tool discovers available Actors or MCP-Servers in Apify Store using full text search using keywords.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "limit": {
      "type": "integer",
      "minimum": 1,
      "maximum": 100,
      "default": 10,
      "description": "The maximum number of Actors to return. Default value is 10."
    },
    "offset": {
      "type": "integer",
      "minimum": 0,
      "default": 0,
      "description": "The number of elements that should be skipped at the start. Default value is 0."
    },
    "search": {
      "type": "string",
      "default": "",
      "description": "String of key words to search Actors by. Searches the title, name, description, username, and readme of an Actor.Only key word search is supported, no advanced search.Always prefer simple keywords over complex queries."
    },
    "category": {
      "type": "string",
      "default": "",
      "description": "Filters the results by the specified category."
    }
  },
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/apify/actors-mcp-server</server_name>
<tool_name>search-actor</tool_name>
<arguments>
{
  "search": "web scraper"
}
</arguments>
</use_mcp_tool>
```

### get-tool-details

This tool gets documentation, readme, input schema and other details about an Actor.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "actorName": {
      "type": "string",
      "description": "Retrieve input, readme, and other details for Actor ID or Actor full name. Actor name is always composed from `username/name`"
    },
    "limit": {
      "type": "integer",
      "default": 5000,
      "description": "Truncate the README to this limit. Default value is 5000."
    }
  },
  "required": [
    "actorName"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/apify/actors-mcp-server</server_name>
<tool_name>get-tool-details</tool_name>
<arguments>
{
  "actorName": "apify/web-scraper"
}
</arguments>
</use_mcp_tool>
