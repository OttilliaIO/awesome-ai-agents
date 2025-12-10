# Awesome AI Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI agent frameworks, tools, and resources for building intelligent, autonomous systems.

## Contents

- [Agent Frameworks & SDKs](#agent-frameworks--sdks)
  - [Frontier Model Providers](#frontier-model-providers)
  - [Foundation Model Frameworks](#foundation-model-frameworks)
  - [General Purpose Frameworks](#general-purpose-frameworks)
- [Coding Agents](#coding-agents)
  - [IDE Integrated](#ide-integrated)
  - [CLI Tools](#cli-tools)
  - [Cloud-Based IDEs](#cloud-based-ides)
- [LLM SDKs & Integration Tools](#llm-sdks--integration-tools)
- [RAG & Knowledge Management](#rag--knowledge-management)
- [Observability & Monitoring](#observability--monitoring)
- [Multi-Model & Gateway Tools](#multi-model--gateway-tools)

---

## Agent Frameworks & SDKs

### Frontier Model Providers

These are SDKs and agent frameworks from companies that develop frontier LLMs.

| Provider | Repository | Stars | Description |
|----------|------------|-------|-------------|
| **OpenAI** | LLM SDK [openai-python](https://github.com/openai/openai-python) | ![Stars](https://img.shields.io/github/stars/openai/openai-python) | Direct API access for GPT-4, o1, o3, embeddings |
| | Agent SDK [openai-agents-python](https://github.com/openai/openai-agents-python) | ![Stars](https://img.shields.io/github/stars/openai/openai-agents-python) | Agent orchestration and workflows. [Docs](https://platform.openai.com/docs) |
| | Coding CLI [codex](https://github.com/openai/codex) | ![Stars](https://img.shields.io/github/stars/openai/codex) | Lightweight local coding agent with ChatGPT integration |
| **Anthropic** | LLM SDK [anthropic-sdk-python](https://github.com/anthropics/anthropic-sdk-python) | ![Stars](https://img.shields.io/github/stars/anthropics/anthropic-sdk-python) | Direct API access for Claude Sonnet 4, Opus 4 |
| | Agent SDK [claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) | ![Stars](https://img.shields.io/github/stars/anthropics/claude-agent-sdk-python) | Agent orchestration and tool integration. [Docs](https://docs.anthropic.com) |
| | Coding CLI [claude-code](https://github.com/anthropics/claude-code) | ![Stars](https://img.shields.io/github/stars/anthropics/claude-code) | Terminal coding agent with git workflows and plugins |
| **Google** | LLM SDK [python-genai](https://github.com/googleapis/python-genai) | ![Stars](https://img.shields.io/github/stars/googleapis/python-genai) | Direct API access for Gemini 2.0 Flash, Pro |
| | Agent SDK [adk-python](https://github.com/google/adk-python) | ![Stars](https://img.shields.io/github/stars/google/adk-python) | Agent Development Kit for building agents. [Docs](https://googleapis.github.io/python-genai/) |
| | Coding CLI [gemini-cli](https://github.com/google-gemini/gemini-cli) | ![Stars](https://img.shields.io/github/stars/google-gemini/gemini-cli) | Terminal agent with Google Search and 1M token context |

### General Purpose Frameworks

Open-source agent frameworks maintained by the community.

#### Agno
- **GitHub**: [agno-agi/agno](https://github.com/agno-agi/agno) ![Stars](https://img.shields.io/github/stars/agno-agi/agno)
- **Description**: Fast multi-agent framework, runtime and control plane
- **Key Features**:
  - Framework for building agents, teams, and workflows with memory, knowledge, and state
  - AgentOS Runtime for production deployment with FastAPI app
  - AgentOS Control Plane for testing, monitoring, and management
  - Model-agnostic with type-safe structured I/O
  - MCP and A2A protocol support
  - 100+ built-in toolkits
  - Private by design - runs entirely in your cloud
- **Website**: [agno.com](https://agno.com/)
- **License**: Apache 2.0

#### Microsoft AutoGen
- **GitHub**: [microsoft/autogen](https://github.com/microsoft/autogen) ![Stars](https://img.shields.io/github/stars/microsoft/autogen)
- **Description**: A programming framework for agentic AI supporting both Python and .NET
- **Key Features**:
  - Multi-agent conversation patterns
  - Human-in-the-loop workflows
  - Code execution and AutoGen Studio GUI
  - Built-in agent abstractions
- **Website**: [microsoft.github.io/autogen](https://microsoft.github.io/autogen/)
- **Note**: Microsoft announced a new [Agent Framework](https://github.com/microsoft/agent-framework) - AutoGen continues to be maintained


#### ByteDance Trae
- **GitHub**: [bytedance/trae-agent](https://github.com/bytedance/trae-agent) ![Stars](https://img.shields.io/github/stars/bytedance/trae-agent)
- **Description**: LLM-based agent for general purpose software engineering tasks
- **Key Features**:
  - Lakeview for concise step summarization
  - Multi-LLM support (OpenAI, Anthropic, Doubao, Azure, OpenRouter, Ollama, Gemini)
  - Rich tool ecosystem (file editing, bash, sequential thinking)
  - Interactive conversational interface
  - Trajectory recording for debugging and analysis
  - Docker mode for isolated execution environments
- **Website**: [trae.ai](https://www.trae.ai/)
- **License**: MIT
- **Research**: [arXiv:2507.23370](https://arxiv.org/abs/2507.23370)

#### AG2 (Formerly AutoGen)
- **GitHub**: [ag2ai/ag2](https://github.com/ag2ai/ag2) ![Stars](https://img.shields.io/github/stars/ag2ai/ag2)
- **Description**: Open-source AgentOS evolved from Microsoft's AutoGen
- **Key Features**:
  - Conversable agents with seamless communication
  - Orchestrating multiple agents (swarms, group chats, nested chats)
  - Tool support with external APIs
  - Human-in-the-loop capabilities
- **Website**: [ag2.ai](https://ag2.ai/)
- **License**: Apache 2.0

#### LangGraph
- **GitHub**: [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) ![Stars](https://img.shields.io/github/stars/langchain-ai/langgraph)
- **Description**: Low-level orchestration framework for building stateful, multi-agent applications
- **Key Features**:
  - Durable execution with automatic resumption
  - Human-in-the-loop workflows
  - Comprehensive memory (short-term and long-term)
  - Production-ready deployment
  - Inspired by Pregel and Apache Beam
- **Website**: [docs.langchain.com/oss/python/langgraph](https://docs.langchain.com/oss/python/langgraph/)
- **License**: MIT

#### CrewAI
- **GitHub**: [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) ![Stars](https://img.shields.io/github/stars/crewAIInc/crewAI)
- **Description**: Fast and flexible multi-agent automation framework built from scratch
- **Key Features**:
  - CrewAI Crews for autonomous multi-agent collaboration
  - CrewAI Flows for event-driven control
  - Independent of LangChain or other frameworks
  - 100,000+ certified developers
  - Enterprise-ready with Crew Control Plane
- **Website**: [crewai.com](https://crewai.com/)
- **License**: MIT

#### PydanticAI
- **GitHub**: [pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai) ![Stars](https://img.shields.io/github/stars/pydantic/pydantic-ai)
- **Description**: GenAI agent framework built by the Pydantic team
- **Key Features**:
  - Model-agnostic (supports OpenAI, Anthropic, Gemini, Ollama, etc.)
  - Type-safe with full IDE support
  - Seamless observability with Pydantic Logfire
  - Powerful evals for testing and evaluation
  - MCP, A2A, and UI integrations
  - Streamed outputs with validation
- **Website**: [ai.pydantic.dev](https://ai.pydantic.dev/)
- **License**: MIT

#### LangChain
- **GitHub**: [langchain-ai/langchain](https://github.com/langchain-ai/langchain) ![Stars](https://img.shields.io/github/stars/langchain-ai/langchain)
- **Description**: Framework for building LLM-powered agents and applications
- **Key Features**:
  - Real-time data augmentation with vast integration library
  - Model interoperability
  - Rapid prototyping with component-based architecture
  - Production-ready with monitoring and evaluation
  - Works seamlessly with LangGraph for advanced orchestration
- **Website**: [docs.langchain.com](https://docs.langchain.com/oss/python/langchain/)
- **License**: MIT

#### AutoGPT
- **GitHub**: [Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) ![Stars](https://img.shields.io/github/stars/Significant-Gravitas/AutoGPT)
- **Description**: Platform for building, deploying, and running AI agents
- **Key Features**:
  - Agent Builder with low-code interface
  - Workflow management by connecting blocks
  - Ready-to-use agents from marketplace
  - AutoGPT Server for continuous agent execution
  - Supports web browsing, code execution, file handling
- **Website**: [agpt.co](https://agpt.co/)
- **License**: MIT (core), Polyform Shield (platform)

---

## Coding Agents

AI-powered coding assistants that help with software development.

### IDE Integrated

Tools that integrate directly into your development environment.

#### GitHub Copilot
- **Website**: [github.com/features/copilot](https://github.com/features/copilot)
- **Description**: AI pair programmer that works in your editor
- **Key Features**:
  - Code completion and suggestions
  - Agent mode for autonomous coding
  - Chat and explanation features
  - Multiple LLM options (GPT-5, Claude Sonnet 4, Gemini 2.5 Pro)
  - Works in VS Code, Visual Studio, JetBrains, Neovim, and more
- **Pricing**: Free tier, $10/month Pro, $39/month Pro+

#### Cursor
- **Website**: [cursor.sh](https://cursor.sh/)
- **Description**: AI-first code editor (fork of VS Code)
- **Key Features**:
  - Built-in AI chat and code generation
  - Codebase-aware suggestions
  - Multi-file editing
  - Natural language commands

#### Antigravity
- **Description**: AI coding assistant (closed source)
- **Key Features**:
  - Integrated development environment
  - AI-powered code suggestions
  - Multi-language support

### CLI Tools

Command-line tools for AI-assisted coding.

#### OpenAI Codex
- **GitHub**: [openai/codex](https://github.com/openai/codex) ![Stars](https://img.shields.io/github/stars/openai/codex)
- **Description**: Lightweight coding agent from OpenAI that runs locally
- **Key Features**:
  - Sign in with ChatGPT (Plus, Pro, Team, Edu, Enterprise)
  - Model Context Protocol (MCP) support
  - Execpolicy for command governance
  - TypeScript SDK and GitHub Action integration
  - Sandbox & approval workflows
- **Install**: `npm i -g @openai/codex` or `brew install --cask codex`
- **License**: Apache 2.0

#### Claude Code
- **GitHub**: [anthropics/claude-code](https://github.com/anthropics/claude-code) ![Stars](https://img.shields.io/github/stars/anthropics/claude-code)
- **Description**: Agentic coding tool that lives in your terminal
- **Key Features**:
  - Understands your codebase and git workflows
  - Natural language commands
  - Plugin system for extensibility
  - Direct integration via `@claude` on GitHub
  - Handles routine tasks and code explanations
- **Install**: `curl -fsSL https://claude.ai/install.sh | bash` or `npm install -g @anthropic-ai/claude-code`
- **Website**: [code.claude.com](https://code.claude.com/docs/en/overview)

#### Gemini CLI
- **GitHub**: [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) ![Stars](https://img.shields.io/github/stars/google-gemini/gemini-cli)
- **Description**: Open-source AI agent that brings Gemini directly into your terminal
- **Key Features**:
  - Free tier: 60 req/min with 1M token context (Gemini 2.5 Pro)
  - Built-in tools: Google Search grounding, file ops, shell commands
  - MCP support for custom integrations
  - Conversation checkpointing and custom context files
  - GitHub Action integration for PR reviews and issue triage
- **Install**: `npm install -g @google/gemini-cli` or `brew install gemini-cli`
- **Website**: [geminicli.com](https://geminicli.com/)
- **License**: Apache 2.0

#### Aider
- **GitHub**: [Aider-AI/aider](https://github.com/Aider-AI/aider) ![Stars](https://img.shields.io/github/stars/Aider-AI/aider)
- **Description**: AI pair programming in your terminal
- **Key Features**:
  - Works with Claude 3.7 Sonnet, DeepSeek, GPT-4o, and many others
  - Maps your entire codebase for context
  - Supports 100+ programming languages
  - Git integration with automatic commits
  - Voice-to-code capabilities
  - Linting and testing automation
- **Website**: [aider.chat](https://aider.chat/)
- **License**: Apache 2.0

#### OpenHands (formerly OpenDevin)
- **GitHub**: [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands) ![Stars](https://img.shields.io/github/stars/OpenHands/OpenHands)
- **Description**: AI-driven development platform
- **Key Features**:
  - OpenHands SDK for building AI agents
  - OpenHands CLI for command-line usage
  - Local GUI with REST API
  - OpenHands Cloud with $10 free credit
  - Enterprise self-hosting options
- **Website**: [openhands.dev](https://openhands.dev/)
- **License**: MIT

### Cloud-Based IDEs

Web-based development environments with AI capabilities.

#### Replit
- **Website**: [replit.com](https://replit.com/)
- **Description**: Cloud-based IDE with AI code generation
- **Key Features**:
  - AI-powered code completion
  - Collaborative coding
  - Instant deployment
  - Support for 50+ languages

---

## LLM SDKs & Integration Tools

### LiteLLM
- **GitHub**: [BerriAI/litellm](https://github.com/BerriAI/litellm) ![Stars](https://img.shields.io/github/stars/BerriAI/litellm)
- **Description**: Call 100+ LLM APIs using the OpenAI format
- **Key Features**:
  - Unified interface for all major LLM providers
  - LiteLLM Proxy Server (LLM Gateway) for cost tracking and rate limiting
  - Retry/fallback logic across multiple deployments
  - 8ms P95 latency at 1k RPS
  - Supports all major providers (OpenAI, Anthropic, Google, Azure, Bedrock, etc.)
- **Website**: [docs.litellm.ai](https://docs.litellm.ai/)
- **License**: View license on GitHub

---

## RAG & Knowledge Management

### LlamaIndex
- **GitHub**: [run-llama/llama_index](https://github.com/run-llama/llama_index) ![Stars](https://img.shields.io/github/stars/run-llama/llama_index)
- **Description**: Leading framework for building LLM-powered agents over your data
- **Key Features**:
  - Data connectors for APIs, PDFs, docs, SQL, etc.
  - Advanced retrieval/query interface
  - Structured data with indices and graphs
  - Easy integration with LangChain, Flask, Docker
  - 300+ integration packages on LlamaHub
- **Website**: [developers.llamaindex.ai](https://developers.llamaindex.ai/)
- **License**: MIT

---

## Observability & Monitoring

### LangSmith
- **Website**: [langchain.com/langsmith](https://www.langchain.com/langsmith)
- **Description**: Observability and deployment platform for LLM applications
- **Key Features**:
  - Real-time tracing and debugging
  - Evals-based performance monitoring
  - Cost tracking and behavior analysis
  - LangSmith Deployment for scaling agents
  - LangGraph Studio for visual prototyping
- **Integration**: Works with LangChain and LangGraph

### Pydantic Logfire
- **Website**: [pydantic.dev/logfire](https://pydantic.dev/logfire)
- **Description**: OpenTelemetry observability platform by Pydantic
- **Key Features**:
  - Real-time debugging
  - Performance monitoring
  - Behavior and cost tracking
  - Native integration with PydanticAI
  - General-purpose OpenTelemetry platform

---

## Multi-Model & Gateway Tools

### LiteLLM Proxy
- See [LiteLLM](#litellm) in LLM SDKs section
- Acts as LLM Gateway with:
  - Cost tracking across projects
  - Rate limiting per API key
  - Load balancing
  - Authentication hooks
  - Logging integrations

---

## Additional Resources

### Communities & Learning

- **Discord Servers**:
  - [CrewAI Discord](https://discord.gg/crewai)
  - [AutoGen Discord](https://discord.gg/autogen)
  - [AG2 Discord](https://discord.gg/pAbnFJrkgZ)
  - [LlamaIndex Discord](https://discord.gg/dGcwcsnxhU)
  - [Aider Discord](https://discord.gg/Y7X7bhMQFV)
  
- **Learning Platforms**:
  - [LangChain Academy](https://academy.langchain.com/) - Free courses on LangGraph
  - [DeepLearning.AI - Multi AI Agent Systems with CrewAI](https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/)
  - [CrewAI Learning Platform](https://learn.crewai.com/) - 100,000+ certified developers

### Documentation

- [LangChain Docs](https://docs.langchain.com/)
- [LangGraph Docs](https://docs.langchain.com/oss/python/langgraph/)
- [PydanticAI Docs](https://ai.pydantic.dev/)
- [CrewAI Docs](https://docs.crewai.com/)
- [AutoGen Docs](https://microsoft.github.io/autogen/)
- [AG2 Docs](https://docs.ag2.ai/)
- [LlamaIndex Docs](https://docs.llamaindex.ai/)

### Comparisons

- **CrewAI vs LangGraph**: CrewAI demonstrates 5.76x faster execution in QA tasks
- **LangGraph**: Low-level, focused on orchestration with durable execution
- **LangChain**: Higher-level, pre-built architectures for common patterns
- **PydanticAI**: Type-safe, model-agnostic with strong Pydantic ecosystem
- **AG2**: Apache 2.0 licensed, community-driven evolution of AutoGen

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
