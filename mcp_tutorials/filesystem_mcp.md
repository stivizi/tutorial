## Filesystem MCP

### read_file

This tool reads the complete contents of a file from the file system.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "path": {
      "type": "string"
    }
  },
  "required": [
    "path"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/filesystem</server_name>
<tool_name>read_file</tool_name>
<arguments>
{
  "path": "mcp_tutorial.md"
}
</arguments>
</use_mcp_tool>
```

### search_files

This tool recursively searches for files and directories matching a pattern.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "path": {
      "type": "string"
    },
    "pattern": {
      "type": "string"
    },
    "excludePatterns": {
      "type": "array",
      "items": {
        "type": "string"
      },
      "default": []
    }
  },
  "required": [
    "path",
    "pattern"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/filesystem</server_name>
<tool_name>search_files</tool_name>
<arguments>
{
  "path": ".",
  "pattern": "TODO"
}
</arguments>
</use_mcp_tool>
```

### write_file

This tool creates a new file or completely overwrite an existing file with new content.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "path": {
      "type": "string"
    },
    "content": {
      "type": "string"
    }
  },
  "required": [
