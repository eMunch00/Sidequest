# MCP/JSON - JARGON & TEMPLATES:

## MCP Model Context Protocol - The Protocol:
* Client-Server Protocol, handels files back and forth between tools/skills and LMStuido. Uses JSON-RPC2.0 file syntax. Allows communication with Resources (files & folders), Tools (code) & Prompts (tepmlates).
**Manditory JSON Keys**
* The following three keys(variables) need to be present in server request/response JSON-RCP files, not requied in tool decloration JSON files.
{
  "jsonrpc": "2.0",
  "method": "tools/call",
  "id": 1
}

## JSON - Java Script Object Notation - The Format:
* highly structured file format used to structure text/data so that computers can parse it easily without it turning into a jumbled mess.
**Server Request/Response Schema**
    *JSON-RPC2.0* Remote Procedure Call, this is the schema used when sending data back and forth between server request & server response.
**Tool Decloration Schema**
    * ... this is the schema used to allow LLMs to access skills/tools via MCP servers. it reads the skills list in this JSON file then writes/sends a server request JSON file to the active skill, then recieves/interprets the server response from the MCP server.
**Characters used in JSON**
* `{ }` Curly Brackets(Braces),
    "Defines an Object. It groups a collection of ""key"": ""value"" pairs together into a single entity."
* `[ ]` Square Brackets(Brackets),"Defines an Array (or List). 
    It holds an ordered sequence of values, strings, or even other objects."
* `" "` Double Quotes,Defines a String (literal text data). 
    Numbers or booleans inside quotes become plain text.
* `:` Colon, Separates a Key (on the left) from its Value (on the right).
    "Like the Equals Sign (=) in a python variable."
* `,` Comma, Separates individual elements inside an object or an array. 
    (Never place one after the last item).

## JSON/MCP Template:
* the following is example schema structure MCP servers use to register capabilities (skills) for an LLM. While the interior payload changes depending on whether it is a resource, tool, or prompt, the top-level wrapping follows this exact structural convention:
{
  "name": "unique_identifier_name",
  "description": "Clear explanation telling the LLM exactly when and why to use this blueprint.",
  "type": "resource_or_tool_or_prompt",
  "payload_structure": {
    "uriOrSchema": "Defines either where the data lives or what inputs it expects"
  }
}

## JSON - Format Examples:
**Recources** 
* JSON Decloaratoin template that allows the LLM to pars user infrence with tool description, then injects perameters from user inference into the JSON format and sends a request to the server to search the file for info in the designated URI path..
    {
  "uri": "catalog://electrical/switchgear/eaton-magnum-ds",
  "name": "Eaton Magnum DS Catalog",
  "description": "Contains technical specifications, framing dimensions, and bus routing configurations for low-voltage power circuit breakers.",
  "mimeType": "text/plain"
    }

**Tools**
* JSON Decloration template to activate a tool that pulls info from a users prompt, injects it into the following json format then sends it to a script (skill/tool) for processing:
    {
  "name": "get_labor_units",
  "description": "Retrieves the standard NECA labor hours required to install specific electrical conduits and wire types based on environment and height.",
  "inputSchema": {
    "type": "object",
    "properties": {
      "material_type": {
        "type": "string",
        "enum": ["EMT", "RMC", "PVC", "MC_Cable"],
        "description": "The exact type of electrical conduit or cabling being installed."
      },
      "size_inches": {
        "type": "number",
        "description": "The trade size diameter of the conduit in inches, expressed as a decimal (e.g., 0.75 for 3/4 inch, 2.0 for 2 inch)."
      },
      "quantity_feet": {
        "type": "number",
        "description": "The total linear footage of the installation run."
      }
    },
    "required": ["material_type", "size_inches", "quantity_feet"]
    }
    }

**Prompts**
* JSON decloration template to format the servers resposne is the specified format, for the LLM to review in a sctructured response format.
    {
  "name": "submittal_technical_review",
  "description": "Generates a structured template for reviewing manufacturer engineering submittals against project spec sheets.",
  "arguments": [
    {
      "name": "equipment_type",
      "description": "The type of gear being reviewed (e.g., Dry-Type Transformer, UPS System, PDU).",
      "required": true
    },
    {
      "name": "spec_section",
      "description": "The CSI MasterFormat section number (e.g., 26 22 00).",
      "required": false
    }
    ]
    }
