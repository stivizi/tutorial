## Ollama MCP

### run

This tool runs a model

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "Name of the model"
    },
    "prompt": {
      "type": "string",
      "description": "Prompt to send to the model"
    },
    "timeout": {
      "type": "number",
      "description": "Timeout in milliseconds (default: 60000)",
      "minimum": 1000
    }
  },
  "required": [
    "name",
    "prompt"
  ]
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/NightTrek/Ollama-mcp</server_name>
<tool_name>run</tool_name>
<arguments>
{
  "name": "llama2",
  "prompt": "What is the capital of France?"
}
</arguments>
</use_mcp_tool>
```

### list

This tool lists models

Input Schema:

```json
{
  "type": "object",
  "properties": {}
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/NightTrek/Ollama-mcp</server_name>
<tool_name>list</tool_name>
<arguments>
{}
</arguments>
</use_mcp_tool>
