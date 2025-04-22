## Markdownify MCP

### audio-to-markdown

This tool converts an audio file to markdown, including transcription if possible

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "filepath": {
      "type": "string",
      "description": "Absolute path of the audio file to convert"
    }
  },
  "required": [
    "filepath"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/zcaceres/markdownify-mcp</server_name>
<tool_name>audio-to-markdown</tool_name>
<arguments>
{
  "filepath": "/Users/steve/audio.mp3"
}
</arguments>
</use_mcp_tool>
```

### webpage-to-markdown

This tool converts a webpage to markdown

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "url": {
      "type": "string",
      "description": "URL of the webpage to convert"
    }
  },
  "required": [
    "url"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/zcaceres/markdownify-mcp</server_name>
<tool_name>webpage-to-markdown</tool_name>
<arguments>
{
  "url": "https://example.com"
}
</arguments>
</use_mcp_tool>
