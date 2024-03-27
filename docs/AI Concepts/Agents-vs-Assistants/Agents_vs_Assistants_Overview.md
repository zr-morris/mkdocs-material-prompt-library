#  Agents & Assistants Overview

## Common Features between Agents and Assistants
- Both utilize Large Language Models (LLMs).
- Both operate based on prompts for direction.
- Both have access to files and tools.
- Both can be interacted with via UI or code.

## Agents
- **Nature**: Autonomous.
- **Scope**: Narrow.
- **Functionality**:
  - Agents can have multiple classes and tools plus a knowledge base, giving them the ability to generalize or focus given the exact prompt.
  - Used in conjunction with other agents (referred to as "crews", "swarms", etc.).
- **Agent Frameworks**:
  - CrewAI
  - Autogen
  - Langchain
- **Ideal Use Cases**:
  - Complex processes that require skills from a few specialist agents to be effective.
  - High latency activities.

## Assistants
- **Nature**: Human-assisted.
- **Scope**: Mid to narrow.
- **Functionality**:
  - Stand-alone operation.
- **Assistant Platforms**:
  - OpenAI Assistants API
  - SuperAGI
- **Ease of Building**:
  - Easy to build with access to building blocks.
- **Ideal Use Cases**:
  - Focused, narrow scope processes that only need a few skills, abilities, and knowledge sources.
  - Low latency activities.

## Examples

### CrewAI Example:
- ESG Reporting Gap Analysis.

### OpenAI Assistants Example:
- Financial Ratio Analyzer.
