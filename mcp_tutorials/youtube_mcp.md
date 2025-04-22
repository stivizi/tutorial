## YouTube MCP

### download_youtube_url

This tool downloads YouTube subtitles from a URL

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "url": {
      "type": "string",
      "description": "URL of the YouTube video"
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
<server_name>github.com/anaisbetts/mcp-youtube</server_name>
<tool_name>download_youtube_url</tool_name>
<arguments>
{
  "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
}
</arguments>
</use_mcp_tool>
