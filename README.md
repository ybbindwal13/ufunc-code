Tools in the Python MCP SDK are defined using decorators such as @mcp.tool(). The decorator registers a function as an MCP tool, while Python type hints define the expected input parameters and return types. The SDK uses these type hints to automatically generate schemas and validate data.
Example:
Python
@mcp.tool()
def add_numbers(a: int, b: int) -> int:
    return a + b
To test tools, I would start the MCP Inspector using:
Bash
mcp dev mcp_server.py
After the Inspector opens, I would click Connect to initialize the server. Then I would verify that the tools are listed correctly, execute them with different inputs, test error handling and edge cases, and confirm that outputs match expectations. The Inspector maintains server state between tool calls, allowing me to test stateful workflows before connecting the server to a real application.
