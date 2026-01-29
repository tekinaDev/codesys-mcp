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

<img width="1195" height="803" alt="Screenshot 2026-01-28 at 11 09 01 AM" src="https://github.com/user-attachments/assets/d2d16f78-a6e1-4636-8d22-e77aac856996" />

* Select `Install with NPM Package`

<img width="1195" height="803" alt="Screenshot 2026-01-28 at 11 09 13 AM" src="https://github.com/user-attachments/assets/6328432c-fa46-47f5-9e01-532ff5514b54" />

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

<img width="831" height="914" alt="Screenshot 2026-01-28 at 11 14 23 AM" src="https://github.com/user-attachments/assets/7a322c48-a7b8-491a-93fd-0d80905c9655" />

* Verify if the tools are loaded

<img width="602" height="204" alt="Screenshot 2026-01-28 at 11 18 46 AM" src="https://github.com/user-attachments/assets/1085cb73-336f-4cb8-9e15-2db4272d9c07" />

* Enable the MCP with the AI chatbot and **Enjoy coding!!**

# Results

https://github.com/user-attachments/assets/9514af74-9890-45d9-b893-43e5301f684f

<img width="1916" height="963" alt="Screenshot 2026-01-28 at 11 41 05 AM" src="https://github.com/user-attachments/assets/400a7f9d-644b-43a8-8813-3f69a91e1a7d" />

https://github.com/user-attachments/assets/d6acce4d-f373-4793-8ef4-8b3819bd1b4c


# What's next?

I will continue updating this repo with more functions and add knowledgebase for ease. 
Thank you to everyone in the community!
