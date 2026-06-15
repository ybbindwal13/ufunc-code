When building an MCP (Model Context Protocol) server with the Python SDK, tools are typically defined using decorators provided by the SDK. A decorator such as @server.tool() registers a Python function as a tool that can be called by an AI client. Type hints are used on function parameters and return values to describe the expected inputs and outputs. These type hints help the MCP framework automatically generate schemas, validate data, and provide better documentation for the tool.
Example:
Python
from mcp.server.fastmcp import FastMCP

mcp = FastMCP("DemoServer")

@mcp.tool()
def add_numbers(a: int, b: int) -> int:
    """Adds two numbers together."""
    return a + b
In this example, the decorator exposes the function as an MCP tool, while the type hints (int) define the expected parameter types and return type.
Before connecting tools to a real application, I would test them using the MCP Inspector. First, I would start the MCP server locally and launch the Inspector. Then I would connect the Inspector to the running server and verify that all tools are discovered correctly. Next, I would execute each tool with different inputs, including valid, invalid, and edge-case values, to confirm proper behavior and error handling. I would also check the returned data structure and ensure the tool descriptions and parameter schemas are displayed correctly. After successful testing and validation in the MCP Inspector, the tools can be safely integrated into a real application or AI workflow.
