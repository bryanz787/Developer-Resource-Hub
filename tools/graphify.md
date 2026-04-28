# Graphify
---
Graphify is an AI coding assistant skill which processes a codebase and transforms it into a file and graph network which visualizes dependancies and relations.


## Category
[ ] Text Generation (GPT, Claude, etc.)
[ ] Code Generation (Copilot, Cursor, etc.)
[ ] Testing/Debugging
[x] Documentation
[ ] Code Review
[x] Other: Token + Context Saver

## Link
[Link to Graphify Website](https://graphifylabs.ai/)
[Link to Graphify Repository](https://github.com/safishamsi/graphify)

## Why Recommend It?
Graphify creates a knowledge graph (queriable through `graphify query (question)`) which allows an LLM agent to find related files to explore faster and more efficiently. Many agents will default to `grep` to read files which is token intensive and consumes context space, with a knowledge graph, that step is reduced greatly.

## Cost
[x] Free
[ ] Free tier + paid options
[ ] Subscription ($X/month)
[x] Enterprise

## Compatability
[x] Claude / Claude Code
[x] Cursor
[x] Gemini / Antigravity
[x] OpenAI Codex
[x] OpenCode 
[x] Copilot CLI

## Comparison
This is similar to another tool, GitNexus, in that they both create knowledge graphs of your codebase but their aproaches differ in how they connect to your agent. Graphify relies on a graph node structure and a key findings file directly within the codebase while GitNexus acts like a MCP server.