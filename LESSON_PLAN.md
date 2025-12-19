# AINative Holiday Builder Class - Lesson Plan

**Event**: AINative x API Palooza 2025 Holiday Party
**Date**: Friday, December 19, 2025
**Time**: 10:00 AM - 12:00 PM (2 hours)
**Location**: D20 Pizza, 1520 Mission St, Santa Cruz, CA 95060
**Instructor**: AINative Team
**Target Audience**: Developers, founders, hackers - beginner to intermediate

---

## Course Overview

This hands-on builder class covers the core building blocks of the AINative platform. By the end of this session, attendees will understand how to quickly add AI capabilities to their applications, wire up intelligent agents with tools and workflows, and give their agents persistent memory using ZeroDB.

**What You'll Build**: A simple AI-powered application with memory that can remember previous conversations and context.

---

## Prerequisites (Attendees Should Have)

- Laptop with a modern web browser
- Basic familiarity with REST APIs (helpful but not required)
- Curiosity and willingness to learn!

**No prior AINative setup required** - we'll walk through everything together.

---

## Lesson Schedule (2 Hours)

| Time | Duration | Topic |
|------|----------|-------|
| 10:00 - 10:10 | 10 min | Welcome & Setup |
| 10:10 - 10:40 | 30 min | **Part 1: AI Kit** - Adding AI to Your App |
| 10:40 - 11:15 | 35 min | **Part 2: Agent APIs** - Tools, Actions & Workflows |
| 11:15 - 11:20 | 5 min | Coffee Break |
| 11:20 - 11:50 | 30 min | **Part 3: ZeroDB Memory** - Giving Agents Memory |
| 11:50 - 12:00 | 10 min | Q&A, Resources & Next Steps |

---

## Part 1: AI Kit - Adding AI Features to Your App (30 min)

### What is AI Kit? (5 min)

AI Kit is **"The Stripe for LLM Applications"** - a framework-agnostic SDK for building AI-powered applications quickly and reliably.

**Key Philosophy**: Enable existing frameworks (Next.js, Svelte, Vue, React) to become AI-native without replacing them.

### The 14 NPM Packages (5 min)

**Core Packages (Stable)**:
| Package | Purpose |
|---------|---------|
| `@ainative/ai-kit-core` | Framework-agnostic foundation (1,014 tests) |
| `@ainative/ai-kit` | React hooks and components (382 tests) |
| `@ainative/ai-kit-safety` | Security guardrails - prompt injection, PII, jailbreak detection (349 tests) |
| `@ainative/ai-kit-cli` | Project scaffolding tools (237 tests) |
| `@ainative/ai-kit-testing` | Testing utilities and mocks |
| `@ainative/ai-kit-observability` | Monitoring and metrics |
| `@ainative/ai-kit-tools` | Built-in agent tools |

**Framework Adapters (Beta)**:
- `@ainative/ai-kit-nextjs` - Next.js integration
- `@ainative/ai-kit-svelte` - Svelte adapter
- `@ainative/ai-kit-vue` - Vue adapter

**Advanced Features (Beta)**:
- `@ainative/ai-kit-auth` - AINative authentication
- `@ainative/ai-kit-rlhf` - RLHF data collection
- `@ainative/ai-kit-zerodb` - ZeroDB vector database integration
- `@ainative/ai-kit-design-system` - Design system utilities

### Quick Start Demo (10 min)

**Option 1: Scaffold a New Project**
```bash
# Create a new AI-powered app in seconds
npx @ainative/ai-kit-cli create my-ai-app

# Install dependencies
cd my-ai-app
npm install
```

**Option 2: Add to Existing Project**
```bash
npm install @ainative/ai-kit @ainative/ai-kit-core zod
```

### Live Coding: Build a Streaming Chat Component (10 min)

```typescript
// Basic streaming message with AI Kit React
import { StreamingMessage } from '@ainative/ai-kit';
import { useState } from 'react';

function ChatDemo() {
  const [message, setMessage] = useState('');
  const [isStreaming, setIsStreaming] = useState(false);

  return (
    <div className="chat-container">
      <StreamingMessage
        role="assistant"
        content={message}
        streamingState={isStreaming ? 'streaming' : 'complete'}
        enableMarkdown={true}
        animationType="typewriter"
        codeTheme="dracula"
        showStreamingIndicator={true}
      />
    </div>
  );
}
```

**Key Features Demonstrated**:
- Real-time streaming responses
- Token-by-token typewriter animation
- Markdown rendering with syntax highlighting
- Code copy functionality

### AI Kit Core Concepts

**Agent Definition**:
```typescript
import { Agent, AgentExecutor } from '@ainative/ai-kit-core';
import { z } from 'zod';

const agent = new Agent({
  id: 'assistant',
  name: 'My Assistant',
  systemPrompt: 'You are a helpful AI assistant.',
  llm: {
    provider: 'openai',  // or 'anthropic'
    model: 'gpt-4',
    apiKey: process.env.OPENAI_API_KEY,
  },
  tools: [], // We'll add tools in Part 2!
});

// Execute
const executor = new AgentExecutor(agent);
const result = await executor.execute('Hello!');
```

### Hands-On Exercise #1 (Attendees follow along)

1. Visit the AI Kit playground at https://ainative.studio/ai-kit
2. Try the live demo with streaming responses
3. Experiment with different animation types

---

## Part 2: AINative Agent APIs - Tools, Actions & Workflows (35 min)

### What Are Intelligent Agents? (5 min)

Agents are AI systems that can:
- **Reason** about problems
- **Use tools** to take actions
- **Orchestrate** multi-step workflows
- **Coordinate** with other agents

### Agent Swarm Architecture (10 min)

The AINative Agent Swarm is an **11-stage autonomous workflow** that coordinates multiple specialized AI agents.

**Preparation Stages (1-6)**:
1. **Project Creation** - Initialize project
2. **PRD Upload** - Upload requirements to ZeroDB storage
3. **Data Model Generation** - AI generates database schema
4. **Backlog Creation** - User stories with Fibonacci points
5. **Sprint Planning** - Timeline and velocity calculation
6. **Execution Setup** - Configure agent team

**Execution Stages (7-11)**:
7. **Launch Swarm** - Start multi-agent orchestration
8. **GitHub Repository** - Create repo with proper structure
9. **Publish Issues** - Backlog becomes GitHub Issues
10. **Feature Development** - TDD workflow (Red -> Green -> Refactor)
11. **Validation** - Tests, build verification

### Creating Your First Swarm (10 min)

**Step 1: Authentication**
```bash
# Get your JWT token
curl -X POST https://api.ainative.studio/v1/public/auth/ \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "username=your@email.com&password=yourpassword"
```

**Step 2: Create a Swarm**
```bash
curl -X POST https://api.ainative.studio/v1/public/agent-swarms \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Holiday Builder Swarm",
    "description": "Learning swarm from Santa Cruz class",
    "max_agents": 5,
    "capabilities": ["general", "coding", "analysis"]
  }'
```

**Step 3: Execute a Task**
```bash
curl -X POST https://api.ainative.studio/v1/public/agent-swarms/{SWARM_ID}/tasks \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Code Review Task",
    "description": "Review code for best practices",
    "type": "independent",
    "priority": "medium",
    "context": {
      "code": "function add(a, b) { return a + b; }"
    }
  }'
```

### Agent Capabilities (5 min)

**Core Capabilities**:
- `general` - General task execution
- `analysis` - Data analysis and insights
- `coding` - Code generation and review
- `testing` - Quality assurance
- `documentation` - Content creation

**Technology-Specific**:
- Languages: `python`, `javascript`, `typescript`, `go`
- Frameworks: `react`, `vue`, `nextjs`
- Infrastructure: `docker`, `kubernetes`, `aws`
- Databases: `postgresql`, `mongodb`, `redis`

### Defining Tools with Type Safety (5 min)

Tools are how agents interact with the world. AI Kit uses Zod for type-safe tool definitions:

```typescript
import { z } from 'zod';
import { Agent } from '@ainative/ai-kit-core';

// Define a weather tool
const weatherTool = {
  name: 'get_weather',
  description: 'Get current weather for a city',
  parameters: z.object({
    city: z.string().describe('City name'),
    units: z.enum(['celsius', 'fahrenheit']).default('celsius')
  }),
  execute: async ({ city, units }) => {
    // Call weather API
    const weather = await fetchWeather(city);
    return `Weather in ${city}: ${weather.temp}${units === 'celsius' ? 'C' : 'F'}`;
  }
};

// Add tool to agent
const agent = new Agent({
  id: 'weather-assistant',
  name: 'Weather Bot',
  systemPrompt: 'You help users check the weather.',
  tools: [weatherTool],
  llm: { provider: 'openai', model: 'gpt-4' }
});
```

### Hands-On Exercise #2

1. Visit the Agent Swarm Dashboard at https://ainative.studio/dashboard/agent-swarm
2. Create a new project
3. Watch the 11-stage workflow in action
4. Explore the real-time progress updates

---

## Coffee Break (5 min)

Grab some D20 coffee and network with fellow builders!

---

## Part 3: ZeroDB - Giving Your Agents Memory (30 min)

### The Problem: Stateless AI (3 min)

By default, AI models have **no memory** between conversations. Every request starts fresh. This creates problems:
- Agents can't remember user preferences
- Context is lost between sessions
- No learning from past interactions
- Repeated explanations needed

### What is ZeroDB? (5 min)

ZeroDB is an **AI-native database** designed specifically for intelligent applications. It provides:

**Core Features**:
- **Vector Search** - Semantic similarity search with pgvector/HNSW indexing
- **MCP Protocol** - 8192 token context windows for AI agents
- **Memory Management** - Store and retrieve conversation context
- **Event Streams** - Event-driven architecture support
- **NoSQL Tables** - Flexible data storage
- **File Storage** - Upload and manage files
- **RLHF Integration** - Collect feedback for model improvement

**69 Complete Operations** across:
- Memory (3 operations)
- Vectors (10 operations)
- Quantum compression (6 operations)
- Tables/NoSQL (8 operations)
- Files (6 operations)
- Events (5 operations)
- Projects (7 operations)
- RLHF (10 operations)
- Admin (5 operations)
- PostgreSQL (6 operations)

### Quick Setup (5 min)

**Step 1: Create Account**
```bash
curl -X POST https://api.ainative.studio/v1/public/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "email": "you@email.com",
    "password": "SecurePassword123!",
    "full_name": "Your Name"
  }'
```

**Step 2: Create a Project**
```bash
curl -X POST https://api.ainative.studio/v1/public/projects \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Holiday Builder Project",
    "description": "My first ZeroDB project",
    "tier": "free",
    "database_enabled": true
  }'
```

### Memory Operations Demo (10 min)

**Store Memory**:
```bash
curl -X POST https://api.ainative.studio/v1/public/projects/{PROJECT_ID}/database/memory \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "content": "User prefers dark mode and TypeScript",
    "role": "system",
    "session_id": "session-123",
    "metadata": {
      "category": "preferences"
    }
  }'
```

**Search Memory** (Semantic Search):
```bash
curl -X POST https://api.ainative.studio/v1/public/projects/{PROJECT_ID}/database/memory/search \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "query": "What are the user preferences?",
    "limit": 5
  }'
```

**Get Context Window**:
```bash
curl -X GET https://api.ainative.studio/v1/public/projects/{PROJECT_ID}/database/memory/context?session_id=session-123&max_tokens=4096 \
  -H "Authorization: Bearer YOUR_TOKEN"
```

### Vector Operations (5 min)

Vectors enable semantic search - finding similar items based on meaning, not just keywords.

**Store a Vector**:
```bash
curl -X POST https://api.ainative.studio/v1/public/projects/{PROJECT_ID}/database/vectors/upsert \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "namespace": "documents",
    "embedding": [0.1, 0.2, ...],  // 1536-dimensional vector
    "document": "This is my first document in ZeroDB",
    "metadata": {
      "type": "tutorial",
      "author": "developer"
    }
  }'
```

**Semantic Search**:
```bash
curl -X POST https://api.ainative.studio/v1/public/projects/{PROJECT_ID}/database/vectors/search \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "query_vector": [0.1, 0.2, ...],
    "limit": 10,
    "threshold": 0.7
  }'
```

### MCP Server Integration (2 min)

The ZeroDB MCP Server provides **69 tools** directly to Claude Desktop/Code:

```json
// ~/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "zerodb": {
      "command": "npx",
      "args": ["ainative-zerodb-mcp-server"],
      "env": {
        "ZERODB_API_URL": "https://api.ainative.studio",
        "ZERODB_PROJECT_ID": "your-project-id",
        "ZERODB_USERNAME": "your-email@example.com",
        "ZERODB_PASSWORD": "your-password"
      }
    }
  }
}
```

Then Claude can use commands like:
- "Store this as a memory"
- "Search for similar documents"
- "What context do we have from this session?"

### Hands-On Exercise #3

1. Visit https://zerodb.ainative.studio
2. Create a free account
3. Create your first project
4. Try storing and searching memories via the UI

---

## Putting It All Together: The Complete Picture (5 min)

```
+-------------------+
|     AI Kit        |  <- Quick AI features (streaming, tools, UI)
+-------------------+
         |
         v
+-------------------+
|   Agent APIs      |  <- Orchestrate intelligent workflows
+-------------------+
         |
         v
+-------------------+
|     ZeroDB        |  <- Persistent memory & vector search
+-------------------+
```

**The Flow**:
1. **AI Kit** provides the building blocks (components, tools, safety)
2. **Agent APIs** coordinate multi-agent workflows
3. **ZeroDB** gives agents memory that persists across sessions

### Example: Complete Agent with Memory

```typescript
import { Agent, AgentExecutor } from '@ainative/ai-kit-core';
import { ZeroDBClient } from '@ainative/ai-kit-zerodb';

// Initialize ZeroDB client
const zerodb = new ZeroDBClient({
  projectId: 'your-project-id',
  apiKey: 'your-api-key'
});

// Create memory-enabled agent
const agent = new Agent({
  id: 'memory-assistant',
  name: 'Assistant with Memory',
  systemPrompt: 'You are a helpful assistant that remembers conversations.',
  llm: { provider: 'openai', model: 'gpt-4' },
  tools: [
    {
      name: 'remember',
      description: 'Store important information for later',
      parameters: z.object({
        content: z.string(),
        category: z.string()
      }),
      execute: async ({ content, category }) => {
        await zerodb.storeMemory({ content, metadata: { category } });
        return 'Stored in memory!';
      }
    },
    {
      name: 'recall',
      description: 'Search memory for relevant information',
      parameters: z.object({ query: z.string() }),
      execute: async ({ query }) => {
        const results = await zerodb.searchMemory({ query, limit: 5 });
        return results.map(r => r.content).join('\n');
      }
    }
  ]
});

// Now the agent can remember and recall!
const executor = new AgentExecutor(agent);
await executor.execute('Remember that I prefer morning meetings');
// Later...
await executor.execute('When do I prefer meetings?'); // Will recall the preference!
```

---

## Q&A and Resources (10 min)

### Key Takeaways

1. **AI Kit** = Quick way to add AI features (14 packages, 2000+ tests)
2. **Agent APIs** = Coordinate intelligent multi-agent workflows
3. **ZeroDB** = Give your agents persistent memory

### Resources

**Websites**:
- AINative Studio: https://www.ainative.studio
- ZeroDB Console: https://zerodb.ainative.studio
- API Docs: https://api.ainative.studio/docs

**GitHub**:
- AINative Studio: https://github.com/AINative-Studio
- AI Kit: https://github.com/AINative-Studio/ai-kit

**Documentation**:
- AI Kit Guide: https://ainative.studio/ai-kit
- Agent Swarm: https://ainative.studio/agent-swarm
- ZeroDB Developer Guide: https://docs.ainative.studio/zerodb

**Community**:
- Discord: https://discord.gg/ainative
- Twitter: @ainativestudio
- Email: hello@ainative.studio

### What's Next?

After this class (12:00 PM - 4:00 PM):
- **Open coworking** in the space
- **Pair programming** with other builders
- **Side project hacking** - try implementing what you learned!
- **Founder chats** and holiday networking

### Special Offer for Attendees

Use code **SANTACRUZ2025** for:
- Extended free tier on ZeroDB
- Priority access to new AI Kit features
- Direct Slack channel with the AINative team

---

## Appendix A: Quick Reference Card

### AI Kit Commands
```bash
# Create new project
npx @ainative/ai-kit-cli create my-app

# Install packages
npm install @ainative/ai-kit @ainative/ai-kit-core zod
```

### ZeroDB Endpoints Cheatsheet
```
# Memory
POST /projects/{id}/database/memory          # Store memory
POST /projects/{id}/database/memory/search   # Search memory
GET  /projects/{id}/database/memory/context  # Get context

# Vectors
POST /projects/{id}/database/vectors/upsert  # Store vector
POST /projects/{id}/database/vectors/search  # Search vectors

# Events
POST /projects/{id}/database/events          # Create event
GET  /projects/{id}/database/events          # List events
```

### Agent Swarm API
```
POST /v1/public/agent-swarms                 # Create swarm
POST /v1/public/agent-swarms/{id}/tasks      # Execute task
GET  /v1/public/agent-swarms/{id}/github     # GitHub status
```

---

## Appendix B: Troubleshooting

### Common Issues

**"Authentication failed"**
- Check your email/password
- Make sure you've verified your email
- Try refreshing your JWT token

**"Project not found"**
- Verify your PROJECT_ID is correct
- Make sure the project is active
- Check you have access to the project

**"Vector dimension mismatch"**
- ZeroDB expects 1536-dimensional vectors (OpenAI embedding size)
- If using different embedding models, check the dimensions

### Getting Help

- API Docs: https://api.ainative.studio/docs
- GitHub Issues: https://github.com/AINative-Studio/core/issues
- Email: support@ainative.studio
- Discord: Real-time help from the community

---

## Appendix C: Advanced Topics (For Self-Study)

### 1. Quantum Vector Compression
ZeroDB supports quantum-enhanced compression (60-96% compression without quality loss)

### 2. Multi-Agent Coordination
Build complex workflows with multiple specialized agents working together

### 3. RLHF Data Collection
Collect human feedback to improve your agents over time

### 4. Event-Driven Architecture
Use ZeroDB events for real-time applications

### 5. PostgreSQL Operations
Direct SQL access for advanced queries

---

**Happy Building! See you at D20 Pizza!**

*This lesson plan was created for the AINative x API Palooza 2025 Holiday Party*
*Santa Cruz, CA - December 19, 2025*
