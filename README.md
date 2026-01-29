# codesys-mcp
Codesys MCP Setup for VS Code using Johannes's instructions, **https://mcpservers.org/servers/johannesPettersson80/codesys-mcp-toolkit**

A Model Context Protocol (MCP) server for CODESYS V3 programming environments. This toolkit enables seamless interaction between MCP clients and CODESYS, allowing automation of project management, POU creation, code editing, and compilation tasks via the CODESYS Scripting Engine.


# Why Codesys MCP for VS Code?

By adding this to VS Code, you can add more scripting functions and build a knowledgebase from the libraries available. This will enable vibe and spec coding using any coding agent available.

## Built Functions

**Scripting Functions**

* `open_project`
* `create_project`
* `save_project`
* `create_pou`
* `set_pou_code`
* `create_property`
* `create_method`
* `compile_project`

**MCP Resources**

* `codesys://project/status`: Check scripting status and currently open project state.
* `codesys://project/{+project_path}/structure`: Retrieve the object structure of a specified project.
* `codesys://project/{+project_path}/pou/{+pou_path}/code`: Read the declaration and implementation code for a specified POU, Method, or Property accessor.

# Installation Steps

* Open VS Code
* Hit `CTRL+SHIFT+P`
* Search for `MCP: Add Server`

[Image: Screenshot 2026-01-28 at 11.09.01 AM.png]
* Select `Install with NPM Package`

[Image: Screenshot 2026-01-28 at 11.09.13 AM.png]
* Type `@codesys/mcp-toolkit` and hit enter
    This will take you to a `mcp.json` file in VS Code Editor
* Edit the file to match these contents

```
{
    "servers": {
        "codesys_local": {
            "command": "codesys-mcp-tool",
            "args": [
                "—codesys-path", // path to your Codesys Executable`
                "...\\CODESYS\\Common\\CODESYS.exe",
                "—codesys-profile", // codesys profile info (exact match)
                "CODESYS V3.5 SP20 Patch 2",
                "—workspace", // your workspace
                "...\\codesys_ws"
            ],
            "type": "stdio"`
        }
    },
    "inputs": []
}
```

* Restart the server

[Image: Screenshot 2026-01-28 at 11.14.23 AM.png]

* Verify if the tools are loaded

[Image: Screenshot 2026-01-28 at 11.18.46 AM.png]

* Enable the MCP with the AI chatbot and **Enjoy coding!!**

# Results

[Image: Screen Recording 2026-01-28 at 11.23.31 AM.mov][Image: Screen Recording 2026-01-28 at 11.29.45 AM.mov][Image: Screenshot 2026-01-28 at 11.41.05 AM.png]

# What's next?

I will continue updating this repo with more functions and add knowledgebase for ease. 
Thank you to everyone in the community!
