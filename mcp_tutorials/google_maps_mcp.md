## Google Maps MCP

### maps_geocode

This tool converts an address into geographic coordinates

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "address": {
      "type": "string",
      "description": "The address to geocode"
    }
  },
  "required": [
    "address"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/google-maps</server_name>
<tool_name>maps_geocode</tool_name>
<arguments>
{
  "address": "1600 Amphitheatre Parkway, Mountain View, CA"
}
</arguments>
</use_mcp_tool>
```

### maps_search_places

This tool searches for places using Google Places API

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "query": {
      "type": "string",
      "description": "Search query"
    },
    "location": {
      "type": "object",
      "properties": {
        "latitude": {
          "type": "number"
        },
        "longitude": {
          "type": "number"
        }
      },
      "description": "Optional center point for the search"
    },
    "radius": {
      "type": "number",
      "description": "Search radius in meters (max 50000)"
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
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/google-maps</server_name>
<tool_name>maps_search_places</tool_name>
<arguments>
{
  "query": "restaurants",
  "location": {
    "latitude": 37.422,
    "longitude": -122.084
  },
  "radius": 1000
}
</arguments>
</use_mcp_tool>
