# Dynamics 365 Table Relationship Explorer CLI and MCP

Using data from and inspired by https://github.com/ameyer505/MicrosoftDynamicsTableAssociations

The repo contains two packages

1. **Core Package** (`d365-relations-cli`): Contains the table relationship finder functionality and CLI.
2. **MCP Package** (`d365-relations-mcp`): Provides an MCP server that exposes the core functionality to AI assistants.

## Core Package

The core package provides the following functionality:

- Finding directly related tables (case-insensitive)
- Finding relationship paths between tables with configurable levels of intermediate tables
- Getting detailed relationship information
- Listing all available tables
- Retrieving statistics about the relationships
- Optimizing relationship files for reduced size and improved performance

### MCP Package

The MCP package builds on the core package and exposes its functionality as MCP tools with FastMCP:

- MCP tools that mirror the core functionality
- Simple configuration through environment variables and command-line arguments

## Installation

Both packages can be installed separately:

```bash
# or using uv
uv add d365-relations-cli
uv add d365-relations-mcpk
```

## Usage

### Core Package CLI

```bash
# Find related tables
uv run tr find-related Customer

# Find relationship paths
uv run tr find-relationship Customer SalesOrder --levels 2

# Optimize relationship file
uv run tr optimize -i tablefieldassociations.json -o tablefieldassociations_opt.json
```

### MCP Server

```bash
# Start the MCP server
uv run mcp

# optionally specify a different relationship file
uv run mcp --relationship-file tablefieldassociations_opt.json
```

## AI Assistant Integration

The MCP server integrates with AI assistants that support the MCP protocol. Example prompts are provided in the `example_prompts.md` file.

See more details on how to use in the [d365-relations-mcp package](d365-relations-mcp/README.md)