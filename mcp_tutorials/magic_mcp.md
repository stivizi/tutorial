## 21st.dev Magic MCP

### 21st_magic_component_builder

This tool is used when the user requests a new UI component—e.g., mentions /ui, /21 /21st, or asks for a button, input, dialog, table, form, banner, card, or other React component. This tool ONLY returns the text snippet for that UI component. After calling this tool, you must edit or add files to integrate the snippet into the codebase.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "message": {
      "type": "string",
      "description": "Full users message"
    },
    "searchQuery": {
      "type": "string",
      "description": "Generate a search query for 21st.dev (library for searching UI components) to find a UI component that matches the user's message. Must be a two-four words max or phrase"
    },
    "absolutePathToCurrentFile": {
      "type": "string",
      "description": "Absolute path to the current file to which we want to apply changes"
    },
    "absolutePathToProjectDirectory": {
      "type": "string",
      "description": "Absolute path to the project root directory"
    },
    "context": {
      "type": "string",
      "description": "Extract additional context about what should be done to create a ui component/page based on the user's message, search query, and conversation history, files. Don't halucinate and be on point."
    }
  },
  "required": [
    "message",
    "searchQuery",
    "absolutePathToCurrentFile",
    "absolutePathToProjectDirectory",
    "context"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>@21st-dev/magic</server_name>
<tool_name>21st_magic_component_builder</tool_name>
<arguments>
{
  "message": "create a button",
  "searchQuery": "React button",
  "absolutePathToCurrentFile": "/Users/steve/git/code/jaakko/tutorial/src/App.js",
  "absolutePathToProjectDirectory": "/Users/steve/git/code/jaakko/tutorial",
  "context": "create a simple button component"
}
</arguments>
</use_mcp_tool>
```

### logo_search

This tool searches and returns logos in specified format (JSX, TSX, SVG).

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "queries": {
      "type": "array",
      "items": {
        "type": "string"
      },
      "description": "List of company names to search for logos"
    },
    "format": {
      "type": "string",
      "enum": [
        "JSX",
        "TSX",
        "SVG"
      ],
      "description": "Output format"
    }
  },
  "required": [
    "queries",
    "format"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>@21st-dev/magic</server_name>
<tool_name>logo_search</tool_name>
<arguments>
{
  "queries": ["github"],
  "format": "JSX"
}
</arguments>
</use_mcp_tool>
