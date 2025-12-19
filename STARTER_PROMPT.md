# AINative Builder Class - Starter Prompt

**Copy and paste this entire prompt into your AI coding assistant (Claude Code, Cursor, Copilot, Codeium, etc.) to get started building with AINative!**

---

## THE PROMPT (Copy Everything Below This Line)

---

You are my AI coding assistant for building an application using the AINative platform. I'm attending the AINative Holiday Builder Class in Santa Cruz on December 19, 2025. Help me build a simple but impressive AI-powered application.

I'm working in a code editor (VS Code, Cursor, or similar) and you're my AI coding assistant. Please help me write code, create files, and build a working application step by step.

## About AINative Platform

AINative provides three core building blocks:

### 1. AI Kit - Production-Ready AI Components
AI Kit is "The Stripe for LLM Applications" - framework-agnostic SDK with 14 NPM packages:

**Core Packages:**
- `@ainative/ai-kit-core` - Agent orchestration, tool calling, streaming
- `@ainative/ai-kit` - React components (StreamingMessage, CodeBlock, etc.)
- `@ainative/ai-kit-safety` - Security (prompt injection, PII filtering, jailbreak detection)
- `@ainative/ai-kit-cli` - Project scaffolding (`npx @ainative/ai-kit-cli create my-app`)
- `@ainative/ai-kit-zerodb` - ZeroDB integration

**Installation:**
```bash
npm install @ainative/ai-kit @ainative/ai-kit-core zod
```

### 2. Agent Swarm APIs - Intelligent Multi-Agent Workflows
Create and orchestrate AI agents that work together:

**API Base URL:** `https://api.ainative.studio`

**Key Endpoints:**
```
POST /v1/public/auth/                    # Login (get JWT token)
POST /v1/public/auth/register            # Register new account
POST /v1/public/projects                 # Create project
POST /v1/public/agent-swarms             # Create agent swarm
POST /v1/public/agent-swarms/{id}/tasks  # Execute task
```

**Agent Capabilities:** general, coding, analysis, testing, documentation, frontend, backend, database, security, devops

### 3. ZeroDB - AI-Native Database with Memory
Give your agents persistent memory with vector search:

**Key Features:**
- Vector search (semantic similarity)
- Memory storage and retrieval
- 8192 token context windows (MCP protocol)
- Event streams
- NoSQL tables
- File storage

**Key Endpoints:**
```
POST /v1/public/projects/{id}/database/memory         # Store memory
POST /v1/public/projects/{id}/database/memory/search  # Search memory
POST /v1/public/projects/{id}/database/vectors/upsert # Store vector
POST /v1/public/projects/{id}/database/vectors/search # Search vectors
POST /v1/public/projects/{id}/database/events         # Create event
POST /v1/public/projects/{id}/database/tables         # Create table
```

## My Credentials (Fill These In)

I registered at ainative.studio and got my API key from Developer Settings.

```
API_BASE_URL: https://api.ainative.studio
EMAIL: [YOUR_EMAIL]
API_KEY: [YOUR_API_KEY_FROM_DEVELOPER_SETTINGS]
PROJECT_ID: [YOUR_PROJECT_ID]
```

Note: I can use the API key directly in headers as `X-API-Key: [API_KEY]` or get a JWT token if needed.

## What I Want to Build

I want to create a simple AI-powered application that demonstrates:
1. **AI Kit** - A nice UI with streaming responses
2. **Agent APIs** - An intelligent agent that can perform tasks
3. **ZeroDB Memory** - The ability to remember and recall information

Suggested app ideas (pick one or suggest your own):
- **Personal Assistant** - Remembers preferences, past conversations, and tasks
- **Study Buddy** - Stores notes, quizzes you, recalls relevant information
- **Recipe Helper** - Saves favorite recipes, suggests based on ingredients
- **Mood Journal** - Tracks moods over time, provides insights
- **Meeting Notes** - Stores meeting summaries, recalls action items
- **Travel Planner** - Remembers preferences, stores trip ideas

## Code Examples You Can Use

### 1. Authentication Options
```javascript
// Option A: Use API Key directly (simpler - recommended for this class)
const API_KEY = 'YOUR_API_KEY_FROM_DEVELOPER_SETTINGS';
const headers = {
  'X-API-Key': API_KEY,
  'Content-Type': 'application/json'
};

// Option B: Login to get JWT token (if needed)
const login = async (email, password) => {
  const response = await fetch('https://api.ainative.studio/v1/public/auth/', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=${email}&password=${password}`
  });
  const data = await response.json();
  return data.access_token;  // Use as: 'Authorization': `Bearer ${token}`
};
```

### 2. Create a Project
```javascript
const createProject = async (token, name) => {
  const response = await fetch('https://api.ainative.studio/v1/public/projects', {
    method: 'POST',
    headers: {
      'Authorization': `Bearer ${token}`,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      name: name,
      description: 'My AINative app',
      tier: 'free',
      database_enabled: true
    })
  });
  return response.json();
};
```

### 3. Store Memory
```javascript
const storeMemory = async (token, projectId, content, metadata = {}) => {
  const response = await fetch(
    `https://api.ainative.studio/v1/public/projects/${projectId}/database/memory`,
    {
      method: 'POST',
      headers: {
        'Authorization': `Bearer ${token}`,
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({
        content: content,
        role: 'user',
        session_id: 'session-' + Date.now(),
        metadata: metadata
      })
    }
  );
  return response.json();
};
```

### 4. Search Memory (Semantic Search)
```javascript
const searchMemory = async (token, projectId, query) => {
  const response = await fetch(
    `https://api.ainative.studio/v1/public/projects/${projectId}/database/memory/search`,
    {
      method: 'POST',
      headers: {
        'Authorization': `Bearer ${token}`,
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({
        query: query,
        limit: 5
      })
    }
  );
  return response.json();
};
```

### 5. React Streaming Component (AI Kit)
```jsx
import { StreamingMessage } from '@ainative/ai-kit';

function ChatMessage({ message, isStreaming }) {
  return (
    <StreamingMessage
      role="assistant"
      content={message}
      streamingState={isStreaming ? 'streaming' : 'complete'}
      enableMarkdown={true}
      animationType="typewriter"
      codeTheme="dracula"
    />
  );
}
```

### 6. Simple HTML/JavaScript Starter (No Build Tools)
```html
<!DOCTYPE html>
<html>
<head>
  <title>My AINative App</title>
  <style>
    body { font-family: Arial, sans-serif; max-width: 600px; margin: 50px auto; padding: 20px; }
    .chat-container { border: 1px solid #ddd; border-radius: 8px; padding: 20px; min-height: 300px; }
    .message { margin: 10px 0; padding: 10px; border-radius: 8px; }
    .user { background: #e3f2fd; }
    .assistant { background: #f5f5f5; }
    input { width: 100%; padding: 10px; margin-top: 10px; border: 1px solid #ddd; border-radius: 4px; }
    button { padding: 10px 20px; background: #2196F3; color: white; border: none; border-radius: 4px; cursor: pointer; margin-top: 10px; }
  </style>
</head>
<body>
  <h1>My AI Assistant</h1>
  <div class="chat-container" id="chat"></div>
  <input type="text" id="input" placeholder="Type a message...">
  <button onclick="sendMessage()">Send</button>
  <button onclick="searchMemories()">Search Memories</button>

  <script>
    const API_URL = 'https://api.ainative.studio';
    const API_KEY = 'YOUR_API_KEY';  // Get this from ainative.studio Developer Settings
    const PROJECT_ID = 'YOUR_PROJECT_ID';

    // Helper to get headers
    const getHeaders = () => ({
      'X-API-Key': API_KEY,
      'Content-Type': 'application/json'
    });

    async function storeMemory(content) {
      const response = await fetch(`${API_URL}/v1/public/projects/${PROJECT_ID}/database/memory`, {
        method: 'POST',
        headers: getHeaders(),
        body: JSON.stringify({ content, role: 'user', session_id: 'demo-session' })
      });
      return response.json();
    }

    async function searchMemory(query) {
      const response = await fetch(`${API_URL}/v1/public/projects/${PROJECT_ID}/database/memory/search`, {
        method: 'POST',
        headers: getHeaders(),
        body: JSON.stringify({ query, limit: 5 })
      });
      return response.json();
    }

    function addMessage(text, isUser) {
      const chat = document.getElementById('chat');
      const div = document.createElement('div');
      div.className = `message ${isUser ? 'user' : 'assistant'}`;
      div.textContent = text;
      chat.appendChild(div);
      chat.scrollTop = chat.scrollHeight;
    }

    async function sendMessage() {
      const input = document.getElementById('input');
      const message = input.value.trim();
      if (!message) return;

      addMessage(message, true);
      input.value = '';

      // Store in ZeroDB memory
      await storeMemory(message);
      addMessage('Memory stored! Your message has been saved.', false);
    }

    async function searchMemories() {
      const input = document.getElementById('input');
      const query = input.value.trim() || 'recent messages';

      addMessage(`Searching for: "${query}"`, true);
      const results = await searchMemory(query);

      if (results.memories && results.memories.length > 0) {
        results.memories.forEach(m => {
          addMessage(`Found: ${m.content} (similarity: ${(m.similarity_score * 100).toFixed(1)}%)`, false);
        });
      } else {
        addMessage('No memories found matching your query.', false);
      }
    }
  </script>
</body>
</html>
```

## How to Help Me

1. **Start Simple** - Help me get the basics working first
2. **Explain As You Go** - I'm learning, so explain what the code does
3. **Use AINative APIs** - Focus on the three core components above
4. **Make It Interactive** - Include user input and visible feedback
5. **Test Incrementally** - Let's test each piece before adding more

## Let's Begin!

Please help me:
1. First, understand what app I want to build (ask me if I haven't decided)
2. Set up the basic structure
3. Add AI Kit components for the UI
4. Connect to ZeroDB for memory
5. Make it work and look nice!

I'm ready to start building. What would you like to build first?

---

## END OF PROMPT

---

# Instructions for Attendees

## How to Use This Prompt

1. **Open your code editor** (VS Code, Cursor, or Windsurf)

2. **Create a new folder** for your project:
   - File → Open Folder → Create New Folder → Name it "holiday-builder-app"

3. **Open your AI assistant** in the editor:
   - **Claude Code:** Open terminal (`Ctrl+`` ` or `Cmd+`` `) and type `claude`
   - **Cursor:** The AI chat is built-in (press `Cmd+L` or `Ctrl+L`)
   - **Copilot:** Press `Ctrl+I` or `Cmd+I` for chat
   - **Codeium:** Click the Codeium icon in the sidebar

4. **Copy this entire prompt** (from "You are my AI coding assistant..." to "What would you like to build first?")

5. **Fill in your credentials** where it says `[YOUR_EMAIL]`, `[YOUR_API_KEY]`, `[YOUR_PROJECT_ID]`

6. **Paste into your AI assistant** and press Enter

7. **Tell the AI what you want to build** - Pick from the suggested apps or describe your own idea

8. **Follow along** as the AI helps you:
   - Create files in your project folder
   - Write the code for you
   - Explain what each part does

9. **Ask questions** whenever something is unclear - that's what the AI is for!

## Quick Start Commands for Your AI

Once you've pasted the prompt, try saying:
- "Let's build a personal assistant app that remembers my preferences"
- "Create a simple HTML file to get started"
- "Help me connect to ZeroDB and store my first memory"
- "Show me how to search for memories I've stored"

**Pro Tip**: Keep this prompt open in a browser tab so you can copy code examples during the class!
