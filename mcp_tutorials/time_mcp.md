## Time MCP

### get_current_time

This tool gets current time in a specific timezones

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "timezone": {
      "type": "string",
      "description": "IANA timezone name (e.g., 'America/New_York', 'Europe/London'). Use 'America/Toronto' as local timezone if no timezone provided by the user."
    }
  },
  "required": [
    "timezone"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/time</server_name>
<tool_name>get_current_time</tool_name>
<arguments>
{
  "timezone": "America/Los_Angeles"
}
</arguments>
</use_mcp_tool>
```

### convert_time

This tool converts time between timezones

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "source_timezone": {
      "type": "string",
      "description": "Source IANA timezone name (e.g., 'America/New_York', 'Europe/London'). Use 'America/Toronto' as local timezone if no source timezone provided by the user."
    },
    "time": {
      "type": "string",
      "description": "Time to convert in 24-hour format (HH:MM)"
    },
    "target_timezone": {
      "type": "string",
      "description": "Target IANA timezone name (e.g., 'Asia/Tokyo', 'America/San_Francisco'). Use 'America/Toronto' as local timezone if no target timezone provided by the user."
    }
  },
  "required": [
    "source_timezone",
    "time",
    "target_timezone"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/time</server_name>
<tool_name>convert_time</tool_name>
<arguments>
{
  "source_timezone": "America/Los_Angeles",
  "time": "10:00",
  "target_timezone": "America/New_York"
}
</arguments>
</use_mcp_tool>
