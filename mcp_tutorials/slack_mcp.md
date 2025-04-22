## Slack MCP

### slack_post_message

This tool posts a new message to a Slack channel

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "channel_id": {
      "type": "string",
      "description": "The ID of the channel to post to"
    },
    "text": {
      "type": "string",
      "description": "The message text to post"
    }
  },
  "required": [
    "channel_id",
    "text"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/slack</server_name>
<tool_name>slack_post_message</tool_name>
<arguments>
{
  "channel_id": "C1234567890",
  "text": "Hello from MCP!"
}
</arguments>
</use_mcp_tool>
```

### slack_get_channel_history

This tool gets recent messages from a channel

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "channel_id": {
      "type": "string",
      "description": "The ID of the channel"
    },
    "limit": {
      "type": "number",
      "description": "Number of messages to retrieve (default 10)",
      "default": 10
    }
  },
  "required": [
    "channel_id"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/slack</server_name>
<tool_name>slack_get_channel_history</tool_name>
<arguments>
{
  "channel_id": "C1234567890",
  "limit": 5
}
</arguments>
</use_mcp_tool>
