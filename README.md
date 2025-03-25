# MODEL CONTEXT PROTOCOL - open protocol that enables seamless integration between AI apps & agents and your tools
**https://modelcontextprotocol.io/introduction**
**https://www.youtube.com/watch?v=kQmXtrmQ5Zg&t=3s**
AAPIs - Standardize how web applications interact with the backend - Servers, Databases and Services
LSP - Standardizes how IDE's interact with language-specific tools - Code navigation, analysis and intelligence
MCP - Standardizes how AI apps interact with external systems - Prompts Tools Resources
<u>Any MCP Client</u>
CLAUDE FOR DESKTOP  |  -> DATABASE MCP SERVER      DATABASES 
Cursor              |     Query+Fetch data
Goose               |     Modify records
Windsurf            |     Handle Data Streams
Your client         |  -> CRM MCP SERVER           CRM SYSTEMS
                          Create/update contracts
                          Manage opportunities
                          Track Interactions
                       -> VERSION CONTROL MCP svr  VERSION CONTROL SOFTWARE
                          Commit changes
                          Resolve confilcts
                          Manage Branches
WITH MCP: Standardized AI Development
AI DEVOLOPERS - Connect your app to any MMCP server with 0 additional work
API DEVLOPERS -  Build an MCP server once, see adoption everywhere
END USERS - More powerful and context-rich AI Apps
ENTERPRISES - Clear separation of concerns between AI product teams

MCP Client                 MCP Server
Involkes Tools             Exposes Tools
Queries for Resource       Exposes Resources
Interpolates Prompts       Exposes Prompts

TOOLS                      RESOURCES               PROMPTS
Model-controlled           Application-controlled  User-controlled
Functions invoked by model Data exposed to the app Pre-defined templates for AI interactions
Retrieve/Search            Files                   Document Q&A
Send a message             Database Records        Transcript Summary   
Update DB records          API Responses           Output as JSON

BUILDING EFFECTIVE AGENTS WITH MCP
     IN              LLM               OUT
Query Results     Call Response     Read/Write
      |                |                |
   Retrieval         TOOLS           MEMORY

Sampling ->
Allows a server to request completions from a client, giving the user application full control over security, privacy, and cost.
CLIENT --request for inference---> SERVER   Sample Parameters: Model Prefs & Hints, Sys prompt, Temp + Max Tokens

Composability - An MCP client can be a server abd vice-vesa
USER & LLM  <---> Client Server <---> Client Server <---> Client Server

BUilding Effective Agents with MCP
Sampling + Composability - Chain agents together while making sure that the client app controls the inference
                              Client Server - Analysis Agent
                           /
APP LLM -- Client Server      Client Server - Coding Agent
                           \
                              Client Server - Research Agent

An Official MCP Registry API
A unified, hosted metadata service which 
enables: Discovery, Centralization, Verification
   REGISTRY     API
   /             |                \
registry: npm   registry: pypi    registry: npm
published: ...  version: 1.0.0    version: 1.0.0
version: 1.2.0  type: sse         type: sse
type: stdio     url: ...          url: ...

An Official MCP Registry API
An MCP server registry helps make agents self-evolving
by letting them discover and choose their own tools

                     USER
                       |
                       | "Fix the bug based on my Grafana logs"
Query Grafana          |
logs & suggest fix   AGENT
                       |
Install & invoke       |  Search for official Grafan Server
Grafana server         |
                  REGISTRY API

Long-lived vs short-lived connections
Smooth upgrade from stateless to stateful capabilities

Streaming
Stream data from server to client

Namespacing
Prevent collisions between entities of multiple servers;
create logical groups of server or tools

Elicitation
Servers proactively request contexst from users