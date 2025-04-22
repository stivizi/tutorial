## WhatsApp MCP

### search_contacts

This tool searches WhatsApp contacts by name or phone number.

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
  ],
  "title": "search_contactsArguments"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/lharries/whatsapp-mcp</server_name>
<tool_name>search_contacts</tool_name>
<arguments>
{
  "query": "John Doe"
}
</arguments>
</use_mcp_tool>
```

### list_messages

This tool gets WhatsApp messages matching specified criteria with optional context.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "after": {
      "anyOf": [
        {
          "type": "string"
        },
        {
          "type": "null"
        }
      ],
      "default": null,
      "title": "After"
    },
    "before": {
      "anyOf": [
        {
          "type": "string"
        },
        {
          "type": "null"
        }
      ],
      "default": null,
      "title": "Before"
    },
    "sender_phone_number": {
      "anyOf": [
        {
          "type": "string"
        },
        {
          "type": "null"
        }
      ],
      "default": null,
      "title": "Sender Phone Number"
    },
    "chat_jid": {
      "anyOf": [
        {
          "type": "string"
        },
        {
          "type": "null"
        }
      ],
      "default": null,
      "title": "Chat Jid"
    },
    "query": {
      "anyOf": [
        {
          "type": "string"
        },
        {
          "type": "null"
        }
      ],
      "default": null,
      "title": "Query"
    },
    "limit": {
      "default": 20,
      "title": "Limit",
      "type": "integer"
    },
    "page": {
      "default": 0,
      "title": "Page",
      "type": "integer"
    },
    "include_context": {
      "default": true,
      "title": "Include Context",
      "type": "boolean"
    },
    "context_before": {
      "default": 1,
      "title": "Context Before",
      "type": "integer"
    },
    "context_after": {
      "default": 1,
      "title": "Context After",
      "type": "integer"
    }
  },
  "title": "list_messagesArguments"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/lharries/whatsapp-mcp</server_name>
<tool_name>list_messages</tool_name>
<arguments>
{
  "query": "hello"
}
</arguments>
</use_mcp_tool>
```

### send_message

This tool sends a WhatsApp message to a person or group. For group chats use the JID.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "recipient": {
      "title": "Recipient",
      "type": "string"
    },
    "message": {
      "title": "Message",
      "type": "string"
    }
  },
  "required": [
    "recipient",
    "message"
  ],
  "title": "send_messageArguments"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/lharries/whatsapp-mcp</server_name>
<tool_name>send_message</tool_name>
<arguments>
{
  "recipient": "1234567890",
  "message": "Hello from MCP!"
}
</arguments>
</use_mcp_tool>
