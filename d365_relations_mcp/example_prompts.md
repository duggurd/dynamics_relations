# Example Prompts for AI Assistants

This document provides example prompts to help AI assistants effectively use the Dynamics 365 Table Relationship Finder MCP tools.

## Introduction Prompt

```
You have access to a Dynamics 365 Table Relationship Finder through MCP tools.
This tool helps you understand how different tables in Dynamics 365 are related to each other.
You can find direct relationships between tables, paths connecting tables, and get details about specific relationships.

The following MCP tools are available:
- find_related_tables: Find all tables directly related to a specific table
- find_relationship_path: Find paths between two tables through their relationships
- get_relationship_details: Get detailed information about the direct relationship between two tables
- list_tables: List all tables in the dataset
- get_stats: Get statistics about the loaded relationships
- optimize_relationship_file: Create an optimized version of the relationships file
```

## Task Prompts

### Finding Related Tables

```
Find all tables that are directly related to the Customer table in Dynamics 365.
```

```
What tables are connected to the SalesTable? I need to understand what data is linked to sales.
```

### Finding Relationship Paths

```
I need to understand how Customer and ProductReceipt tables are connected in Dynamics 365. Can you find a relationship path between them?
```

```
Find all possible ways to connect the WorkOrder table to the SalesInvoice table, allowing up to 2 intermediate tables.
```

### Getting Relationship Details

```
What is the exact relationship between the Customer table and the SalesTable in Dynamics 365? I need to understand the fields that connect them.
```

```
Show me the details of how Opportunity and Lead tables are connected. I need the specific fields involved in this relationship.
```

### Listing Tables and Getting Statistics

```
Show me all tables available in the Dynamics 365 dataset. I want to get a complete overview.
```

```
Can you give me statistics about the relationship data? I want to understand how many tables and relationships are in the system.
```

### Complex Analysis

```
I'm trying to understand the customer sales process in Dynamics 365. Can you:
1. First show me all tables related to Customer
2. Then find how Customer connects to SalesOrder
3. And finally show how SalesOrder connects to Products
This will help me understand the full sales process flow.
```

```
I need to analyze how service operations connect to financial data in Dynamics 365:
1. Start by finding tables related to ServiceOrder
2. Then find paths between ServiceOrder and GeneralLedger
3. Show me the specific relationship details for each connection
This will help me understand the service-to-finance flow.
```

## Providing Context For Better Results

When interacting with the AI assistant and the MCP tools, it's helpful to:

1. Specify the exact table names when known
2. Indicate the depth of relationships to explore when looking for paths
3. Ask for specific details about relationships when needed
4. Build up complex analyses step-by-step

The AI assistant can handle case-insensitive table names, so you don't need to worry about case matching. 