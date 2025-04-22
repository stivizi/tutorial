## GitHub MCP

### create_issue

This tool creates a new issue in a GitHub repository

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "owner": {
      "type": "string"
    },
    "repo": {
      "type": "string"
    },
    "title": {
      "type": "string"
    },
    "body": {
      "type": "string"
    },
    "assignees": {
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "milestone": {
      "type": "number"
    },
    "labels": {
      "type": "array",
      "items": {
        "type": "string"
      }
    }
  },
  "required": [
    "owner",
    "repo",
    "title"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/github</server_name>
<tool_name>create_issue</tool_name>
<arguments>
{
  "owner": "octocat",
  "repo": "hello-world",
  "title": "Found a bug",
  "body": "I'm having a problem with this.",
  "labels": ["bug", "help wanted"],
  "assignees": ["octocat"]
}
</arguments>
</use_mcp_tool>
```

### get_file_contents

This tool gets the contents of a file or directory from a GitHub repository

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "owner": {
      "type": "string",
      "description": "Repository owner (username or organization)"
    },
    "repo": {
      "type": "string",
      "description": "Repository name"
    },
    "path": {
      "type": "string",
      "description": "Path to the file or directory"
    },
    "branch": {
      "type": "string",
      "description": "Branch to get contents from"
    }
  },
  "required": [
    "owner",
    "repo",
    "path"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/github</server_name>
<tool_name>get_file_contents</tool_name>
<arguments>
{
  "owner": "octocat",
  "repo": "hello-world",
  "path": "README.md",
  "branch": "main"
}
</arguments>
</use_mcp_tool>
```

### create_repository

This tool creates a new GitHub repository in your account

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "Repository name"
    },
    "description": {
      "type": "string",
      "description": "Repository description"
    },
    "private": {
      "type": "boolean",
      "description": "Whether the repository should be private"
    },
    "autoInit": {
      "type": "boolean",
      "description": "Initialize with README.md"
    }
  },
  "required": [
    "name"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/modelcontextprotocol/servers/tree/main/src/github</server_name>
<tool_name>create_repository</tool_name>
<arguments>
{
  "name": "my-new-repo",
  "description": "This is a new repository",
  "private": false,
  "autoInit": true
}
</arguments>
</use_mcp_tool>
