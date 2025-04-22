## Supabase MCP

### list_projects

This tool lists all Supabase projects for the user.

Input Schema:

```json
{
  "type": "object",
  "properties": {},
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/supabase-community/supabase-mcp</server_name>
<tool_name>list_projects</tool_name>
<arguments>
{}
</arguments>
</use_mcp_tool>
```

### get_project

This tool gets details for a Supabase project.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "id": {
      "type": "string",
      "description": "The project ID"
    }
  },
  "required": [
    "id"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/supabase-community/supabase-mcp</server_name>
<tool_name>get_project</tool_name>
<arguments>
{
  "id": "your_project_id"
}
</arguments>
</use_mcp_tool>
```

### create_project

This tool creates a new Supabase project. Always ask the user which organization to create the project in. The project can take a few minutes to initialize - use `get_project` to check the status.

Input Schema:

```json
{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "The name of the project"
    },
    "region": {
      "type": "string",
      "enum": [
        "us-west-1",
        "us-east-1",
        "us-east-2",
        "ca-central-1",
        "eu-west-1",
        "eu-west-2",
        "eu-west-3",
        "eu-central-1",
        "eu-central-2",
        "eu-north-1",
        "ap-south-1",
        "ap-southeast-1",
        "ap-northeast-1",
        "ap-northeast-2",
        "ap-southeast-2",
        "sa-east-1"
      ],
      "description": "The region to create the project in. Defaults to the closest region."
    },
    "organization_id": {
      "type": "string"
    },
    "confirm_cost_id": {
      "type": "string",
      "description": "The cost confirmation ID. Call `confirm_cost` first."
    }
  },
  "required": [
    "name",
    "organization_id",
    "confirm_cost_id"
  ],
  "additionalProperties": false,
  "$schema": "http://json-schema.org/draft-07/schema#"
}
```

Example:

```xml
<use_mcp_tool>
<server_name>github.com/supabase-community/supabase-mcp</server_name>
<tool_name>create_project</tool_name>
<arguments>
{
  "name": "my_new_project",
  "organization_id": "your_organization_id",
  "confirm_cost_id": "your_confirm_cost_id"
}
</arguments>
</use_mcp_tool>
