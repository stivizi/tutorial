## Google Calendar MCP

### list-calendars

This tool lists all available calendars

Input Schema:

```json
{
  "type": "object",
  "properties": {},
  "required": []
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/pashpashpash/google-calendar-mcp</server_name>
<tool_name>list-calendars</tool_name>
<arguments>
{}
</arguments>
</use_mcp_tool>
```

### create-event

This tool creates a new calendar event

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "calendarId": {
      "type": "string",
      "description": "ID of the calendar to create event in"
    },
    "summary": {
      "type": "string",
      "description": "Title of the event"
    },
    "description": {
      "type": "string",
      "description": "Description of the event"
    },
    "start": {
      "type": "string",
      "description": "Start time in ISO format"
    },
    "end": {
      "type": "string",
      "description": "End time in ISO format"
    },
    "location": {
      "type": "string",
      "description": "Location of the event"
    },
    "attendees": {
      "type": "array",
      "description": "List of attendees",
      "items": {
        "type": "object",
        "properties": {
          "email": {
            "type": "string",
            "description": "Email address of the attendee"
          }
        },
        "required": [
          "email"
        ]
      }
    }
  },
  "required": [
    "calendarId",
    "summary",
    "start",
    "end"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/pashpashpash/google-calendar-mcp</server_name>
<tool_name>create-event</tool_name>
<arguments>
{
  "calendarId": "your_calendar_id",
  "summary": "Meeting with John",
  "description": "Discuss project progress",
  "start": "2024-01-01T10:00:00-07:00",
  "end": "2024-01-01T11:00:00-07:00"
}
</arguments>
</use_mcp_tool>
