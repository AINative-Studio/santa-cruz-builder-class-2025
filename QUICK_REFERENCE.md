# AINative Holiday Builder Class - Quick Reference Handout

## Your Credentials (Fill In)
```
Email:      ________________________________
API Key:    ________________________________
            ________________________________
Project ID: ________________________________
```

*Get your API Key from: ainative.studio → Developer Settings → Create API Key*

---

## The 3 Building Blocks

| Component | What It Does | Key Feature |
|-----------|--------------|-------------|
| **AI Kit** | Add AI to your app | Streaming UI, tools, safety |
| **Agent APIs** | Smart workflows | Multi-agent coordination |
| **ZeroDB** | Give AI memory | Vector search, context recall |

---

## Important URLs

| Resource | URL |
|----------|-----|
| ZeroDB Console | `zerodb.ainative.studio` |
| API Documentation | `api.ainative.studio/docs` |
| AINative Website | `ainative.studio` |

---

## Quick API Reference

**Base URL:** `https://api.ainative.studio`

### Authentication
```
Login:    POST /v1/public/auth/
Register: POST /v1/public/auth/register
```

### ZeroDB Memory
```
Store:    POST /v1/public/projects/{id}/database/memory
Search:   POST /v1/public/projects/{id}/database/memory/search
Context:  GET  /v1/public/projects/{id}/database/memory/context
```

### Vectors
```
Upsert:   POST /v1/public/projects/{id}/database/vectors/upsert
Search:   POST /v1/public/projects/{id}/database/vectors/search
```

---

## Starter Code (Copy This!)

### Store a Memory
```javascript
fetch('https://api.ainative.studio/v1/public/projects/YOUR_PROJECT_ID/database/memory', {
  method: 'POST',
  headers: {
    'X-API-Key': 'YOUR_API_KEY',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    content: 'Your message here',
    role: 'user',
    session_id: 'my-session'
  })
});
```

### Search Memories
```javascript
fetch('https://api.ainative.studio/v1/public/projects/YOUR_PROJECT_ID/database/memory/search', {
  method: 'POST',
  headers: {
    'X-API-Key': 'YOUR_API_KEY',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    query: 'What was I talking about?',
    limit: 5
  })
});
```

---

## App Ideas to Build

- [ ] **Personal Assistant** - Remembers your preferences
- [ ] **Study Buddy** - Saves notes, quizzes you later
- [ ] **Recipe Helper** - Saves recipes, suggests meals
- [ ] **Mood Journal** - Tracks feelings over time
- [ ] **Meeting Notes** - Stores summaries, recalls action items
- [ ] **Travel Planner** - Remembers places you want to visit

---

## Need Help?

1. **Ask your AI assistant** - Paste the starter prompt!
2. **Ask the instructors** - We're here to help!
3. **Check the docs** - api.ainative.studio/docs
4. **Email us** - support@ainative.studio

---

## After the Class

**Continue building (12pm - 4pm):**
- Open coworking space
- Pair up with other builders
- Get help from instructors

**Stay connected:**
- Discord: `discord.gg/ainative`
- Twitter: `@ainativestudio`
- GitHub: `github.com/AINative-Studio`

---

## Schedule

| Time | Activity |
|------|----------|
| 10:00 | Welcome & Setup |
| 10:10 | **Part 1:** AI Kit |
| 10:40 | **Part 2:** Agent APIs |
| 11:15 | Coffee Break |
| 11:20 | **Part 3:** ZeroDB Memory |
| 11:50 | Q&A |
| 12:00+ | Open Coworking |

---

**WiFi:** _________________ | **Password:** _________________

---

*AINative x API Palooza 2025 | D20 Pizza, Santa Cruz | Dec 19, 2025*
