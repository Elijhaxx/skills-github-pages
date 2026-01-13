---
title: Developer Asta
date: 2026-01-12
---

# Investigating the Effects of LSP–MCP Integration on Code Comprehension

## Abstract
This project presents an agent that integrates **Language Server Protocol (LSP)** outputs with a **Model Context Protocol (MCP)**–guided reasoning process to diagnose, explain, and refactor code. LSP provides structured program insights such as syntax trees, symbols, types, and diagnostics, while MCP orchestrates the LLM’s step-by-step reasoning and tool usage. The goal is to evaluate whether combining precise program structure with guided model reasoning can produce deeper code understanding and clearer explanations than traditional static analysis and heavier agent frameworks.

## Introduction
Static analyzers detect surface-level issues but often miss deeper intent and structural relationships. Large Language Models (LLMs) reason well but lack access to exact program structure. This project bridges that gap by routing LSP-derived structural context through a lightweight MCP server, enabling the model to reason with accurate code semantics. The work also explores MCP as a simpler, protocol-level alternative to larger agent frameworks such as LangChain or LangGraph.

## Objectives
1. Integrate LSP and MCP for structured code understanding  
2. Detect issues and generate clear explanations  
3. Suggest refactors and code improvements  
4. Provide an interactive TUI for real-time exploration  
5. Evaluate clarity, accuracy, and efficiency against baselines  
6. Demonstrate lightweight agent design using MCP  

## System Architecture
### Modules
- **Interactive TUI**
  - Feature selection (analyze, explain, fix)
  - Displays explanations, diffs, suggestions
- **LSP Integration Layer**
  - Wraps language server
  - Extracts AST, symbols, types, diagnostics
- **MCP Orchestration Layer**
  - Plans reasoning steps
  - Coordinates LLM and tools
- **LLM Reasoning Engine**
  - Explains issues
  - Proposes fixes
  - Suggests next actions
- **Action Engine**
  - Applies or simulates changes
  - Generates diffs
  - Re-validates with LSP
- **Evaluation & Logging**
  - Captures traces
  - Compares against static analyzers
  - Measures performance

## Workflow
1. User uploads a repository or pastes code via TUI  
2. User selects a feature: Analyze, Explain, or Fix  
3. Code is ingested and analyzed by LSP  
4. Structured context is normalized  
5. MCP plans tasks based on user intent  
6. LLM performs guided reasoning  
7. Actions are executed and validated  
8. Results are displayed and refined interactively  

## Plan of Action
- **Phase 1:** LSP integration, MCP flow, basic TUI  
- **Phase 2:** Core reasoning and issue explanation  
- **Phase 3:** Refactoring, diffs, live feedback  
- **Phase 4:** Evaluation, benchmarking, final demo  

## Conclusion
By combining LSP’s precise structural insights with MCP-guided reasoning, this project investigates a lightweight yet powerful approach to code understanding. The system aims to deliver clearer explanations, more meaningful refactors, and a simpler alternative to heavyweight agent frameworks—making it well-suited for interactive developer tools.
