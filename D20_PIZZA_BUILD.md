# D20 Pizza Website - Live Build Prompt

**This is the specific app we're building together during the class!**

You can follow along with the instructor using this prompt, or use the [STARTER_PROMPT.md](./STARTER_PROMPT.md) to build something different.

---

## THE PROMPT (Copy Everything Below This Line)

---

You are my AI coding assistant. I'm at a builder class at D20 Pizza in Santa Cruz, and we're building a website for this very restaurant using the AINative platform!

## About D20 Pizza (The Client)

**D20 Pizza** is a Detroit-style pizzeria and board game café located on Santa Cruz's Westside. Here's what makes them special:

### Business Info
- **Name**: D20 Pizza
- **Address**: 1520 Mission St, Santa Cruz, CA 95060
- **Phone**: (831) 777-5331
- **Hours**: Mon-Sun 12:00 PM - 12:00 AM (hours may vary - check Instagram)
- **Instagram**: @d20pizza
- **Concept**: Detroit-style pizza + board game café

### The Name
"D20" refers to the 20-sided dice used in Dungeons & Dragons - a nod to their gaming culture!

### Menu Highlights
- **Pizza Style**: Detroit-style with slow-risen sourdough crust
- **Pizza Size**: 8" x 10" rectangular pans
- **Signature Pizzas**:
  - Cup Pepperoni (classic Detroit-style with curled pepperoni)
  - Almost Maui (Hawaiian-inspired)
  - Nana's Pesto Pesto (pesto-based)
- **Other Items**:
  - Avocado Toast on fresh sourdough ($18 - legendary!)
  - Coffee & Tea
  - Craft beverages

### Games Available
- Dungeons & Dragons (D&D)
- Magic: The Gathering
- Go (classic strategy game)
- Ticket to Ride
- Many more board games available to play or purchase!

### Events
- Board Game Designers Meetups
- Community game nights
- Private events
- Tech meetups (like this AINative class!)

### Vibe
- Casual, welcoming atmosphere
- Perfect for gamers, families, and friends
- Combination of great food and gaming culture
- Community-focused gathering space

---

## My AINative Credentials

```
API_BASE_URL: https://api.ainative.studio
API_KEY: [YOUR_API_KEY_FROM_DEVELOPER_SETTINGS]
PROJECT_ID: [YOUR_PROJECT_ID]
```

---

## What We're Building

A modern, interactive website for D20 Pizza that showcases:

1. **AI-Powered Features** (using AI Kit)
   - Chatbot that answers questions about the menu, hours, games
   - Smart menu recommendations based on preferences
   - Game night scheduler assistant

2. **Intelligent Backend** (using Agent APIs)
   - Order processing workflow
   - Event booking system
   - Customer inquiry routing

3. **Memory & Personalization** (using ZeroDB)
   - Remember customer preferences
   - Track favorite pizzas and games
   - Store event RSVPs and feedback
   - Semantic search for menu items and games

---

## Website Pages to Build

### 1. Home Page
- Hero section with D20 branding (dice theme!)
- "Order Now" and "Reserve a Table" CTAs
- Featured pizzas carousel
- Upcoming events section
- Instagram feed integration

### 2. Menu Page
- Pizza menu with photos and descriptions
- Filter by: Vegetarian, Meat Lovers, House Favorites
- AI-powered "Pizza Recommender" chat widget
- Add to order functionality

### 3. Games Library Page
- Searchable list of all available games
- Filter by: Player count, Game duration, Complexity
- "Find Your Next Game" AI assistant
- Reserve a game for your visit

### 4. Events Page
- Calendar of upcoming events
- Board Game Designers Meetups
- RSVP functionality with ZeroDB storage
- Past events gallery

### 5. Contact/About Page
- Location map
- Hours of operation
- Contact form (stored in ZeroDB)
- The D20 story

### 6. AI Chat Widget (appears on all pages)
- Floating chat button
- Answers FAQs about menu, hours, games
- Remembers conversation context using ZeroDB
- Can help with recommendations

---

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript (vanilla for simplicity)
- **UI Components**: AI Kit streaming components
- **Backend**: AINative Agent APIs
- **Database**: ZeroDB for memory and data storage
- **Styling**: Modern, playful design with dice/gaming theme

---

## Color Scheme (D20 Theme)

```css
:root {
  --primary: #E63946;      /* D20 Red */
  --secondary: #1D3557;    /* Deep Blue */
  --accent: #F4A261;       /* Golden Orange */
  --background: #F1FAEE;   /* Light Cream */
  --text: #1D3557;         /* Deep Blue */
  --success: #2A9D8F;      /* Teal */
}
```

---

## Step-by-Step Build Plan

### Phase 1: Basic Structure (10 min)
1. Create project folder structure
2. Build index.html with basic layout
3. Add CSS styling with D20 theme
4. Create navigation header

### Phase 2: Home Page Content (10 min)
1. Hero section with pizza imagery
2. Featured menu items
3. "Why D20?" section
4. Footer with contact info

### Phase 3: Connect to ZeroDB (15 min)
1. Set up API connection
2. Create a "Contact Us" form that stores messages in ZeroDB
3. Test storing and retrieving data

### Phase 4: AI Chat Widget (15 min)
1. Add floating chat button
2. Build chat interface
3. Connect to ZeroDB for conversation memory
4. Make it answer D20 Pizza questions

### Phase 5: Menu with AI Recommendations (10 min)
1. Display pizza menu
2. Add "Recommend a Pizza" feature
3. Store user preferences in ZeroDB

---

## Code Examples

### 1. Project Structure
```
d20-pizza-website/
├── index.html
├── styles.css
├── app.js
├── pages/
│   ├── menu.html
│   ├── games.html
│   └── events.html
└── assets/
    └── images/
```

### 2. Basic HTML Starter
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>D20 Pizza - Detroit Style Pizza & Board Games | Santa Cruz</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Navigation -->
  <nav class="navbar">
    <div class="logo">
      <span class="dice">🎲</span> D20 Pizza
    </div>
    <ul class="nav-links">
      <li><a href="#menu">Menu</a></li>
      <li><a href="#games">Games</a></li>
      <li><a href="#events">Events</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <a href="#order" class="btn-order">Order Now</a>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1>Roll for Delicious</h1>
      <p>Detroit-style pizza meets board game paradise</p>
      <div class="hero-buttons">
        <a href="#menu" class="btn btn-primary">View Menu</a>
        <a href="#games" class="btn btn-secondary">Browse Games</a>
      </div>
    </div>
  </section>

  <!-- Featured Pizzas -->
  <section id="menu" class="featured-pizzas">
    <h2>🍕 Fan Favorites</h2>
    <div class="pizza-grid">
      <!-- Pizzas will be added here -->
    </div>
  </section>

  <!-- AI Chat Widget -->
  <div id="chat-widget" class="chat-widget">
    <button id="chat-toggle" class="chat-toggle">
      🎲 Ask D20
    </button>
    <div id="chat-container" class="chat-container hidden">
      <div class="chat-header">
        <span>D20 Assistant</span>
        <button id="chat-close">×</button>
      </div>
      <div id="chat-messages" class="chat-messages"></div>
      <div class="chat-input-container">
        <input type="text" id="chat-input" placeholder="Ask about our menu, games, or hours...">
        <button id="chat-send">Send</button>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <div class="footer-content">
      <div class="footer-section">
        <h3>📍 Find Us</h3>
        <p>1520 Mission St<br>Santa Cruz, CA 95060</p>
      </div>
      <div class="footer-section">
        <h3>🕐 Hours</h3>
        <p>Daily: 12PM - 12AM</p>
      </div>
      <div class="footer-section">
        <h3>📱 Connect</h3>
        <p>@d20pizza</p>
        <p>(831) 777-5331</p>
      </div>
    </div>
  </footer>

  <script src="app.js"></script>
</body>
</html>
```

### 3. CSS Styling (D20 Theme)
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --primary: #E63946;
  --secondary: #1D3557;
  --accent: #F4A261;
  --background: #F1FAEE;
  --text: #1D3557;
  --success: #2A9D8F;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: var(--background);
  color: var(--text);
}

/* Navigation */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: var(--secondary);
  color: white;
  position: sticky;
  top: 0;
  z-index: 100;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.dice {
  font-size: 2rem;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: var(--accent);
}

.btn-order {
  background: var(--primary);
  color: white;
  padding: 0.5rem 1.5rem;
  border-radius: 25px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.3s;
}

.btn-order:hover {
  transform: scale(1.05);
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, var(--secondary) 0%, var(--primary) 100%);
  color: white;
  padding: 6rem 2rem;
  text-align: center;
}

.hero h1 {
  font-size: 3.5rem;
  margin-bottom: 1rem;
}

.hero p {
  font-size: 1.5rem;
  opacity: 0.9;
  margin-bottom: 2rem;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.btn {
  padding: 1rem 2rem;
  border-radius: 25px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.3s;
}

.btn-primary {
  background: var(--accent);
  color: var(--secondary);
}

.btn-secondary {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.btn:hover {
  transform: scale(1.05);
}

/* Featured Pizzas */
.featured-pizzas {
  padding: 4rem 2rem;
  text-align: center;
}

.featured-pizzas h2 {
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

.pizza-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.pizza-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s;
}

.pizza-card:hover {
  transform: translateY(-5px);
}

.pizza-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.pizza-card-content {
  padding: 1.5rem;
}

.pizza-card h3 {
  color: var(--secondary);
  margin-bottom: 0.5rem;
}

.pizza-card p {
  color: #666;
  margin-bottom: 1rem;
}

.pizza-price {
  font-size: 1.25rem;
  font-weight: bold;
  color: var(--primary);
}

/* Chat Widget */
.chat-widget {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 1000;
}

.chat-toggle {
  background: var(--primary);
  color: white;
  border: none;
  padding: 1rem 1.5rem;
  border-radius: 50px;
  font-size: 1rem;
  cursor: pointer;
  box-shadow: 0 4px 15px rgba(230, 57, 70, 0.4);
  transition: transform 0.3s;
}

.chat-toggle:hover {
  transform: scale(1.05);
}

.chat-container {
  position: absolute;
  bottom: 70px;
  right: 0;
  width: 350px;
  height: 450px;
  background: white;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.chat-container.hidden {
  display: none;
}

.chat-header {
  background: var(--secondary);
  color: white;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.chat-header button {
  background: none;
  border: none;
  color: white;
  font-size: 1.5rem;
  cursor: pointer;
}

.chat-messages {
  flex: 1;
  padding: 1rem;
  overflow-y: auto;
}

.chat-message {
  margin-bottom: 1rem;
  padding: 0.75rem 1rem;
  border-radius: 15px;
  max-width: 80%;
}

.chat-message.user {
  background: var(--primary);
  color: white;
  margin-left: auto;
}

.chat-message.assistant {
  background: #f0f0f0;
  color: var(--text);
}

.chat-input-container {
  display: flex;
  padding: 1rem;
  border-top: 1px solid #eee;
}

.chat-input-container input {
  flex: 1;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 25px;
  margin-right: 0.5rem;
}

.chat-input-container button {
  background: var(--primary);
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  cursor: pointer;
}

/* Footer */
footer {
  background: var(--secondary);
  color: white;
  padding: 3rem 2rem;
}

.footer-content {
  display: flex;
  justify-content: space-around;
  max-width: 1200px;
  margin: 0 auto;
}

.footer-section h3 {
  margin-bottom: 1rem;
}
```

### 4. JavaScript with ZeroDB Integration
```javascript
// D20 Pizza Website - app.js
const API_URL = 'https://api.ainative.studio';
const API_KEY = 'YOUR_API_KEY';  // From ainative.studio Developer Settings
const PROJECT_ID = 'YOUR_PROJECT_ID';

// Helper for API calls
const getHeaders = () => ({
  'X-API-Key': API_KEY,
  'Content-Type': 'application/json'
});

// ============================================
// ZERODB MEMORY FUNCTIONS
// ============================================

// Store a chat message in ZeroDB memory
async function storeMessage(content, role = 'user') {
  try {
    const response = await fetch(
      `${API_URL}/v1/public/projects/${PROJECT_ID}/database/memory`,
      {
        method: 'POST',
        headers: getHeaders(),
        body: JSON.stringify({
          content: content,
          role: role,
          session_id: getSessionId(),
          metadata: {
            page: 'chat',
            timestamp: new Date().toISOString()
          }
        })
      }
    );
    return response.json();
  } catch (error) {
    console.error('Error storing message:', error);
  }
}

// Search memories for relevant context
async function searchMemories(query) {
  try {
    const response = await fetch(
      `${API_URL}/v1/public/projects/${PROJECT_ID}/database/memory/search`,
      {
        method: 'POST',
        headers: getHeaders(),
        body: JSON.stringify({
          query: query,
          limit: 5
        })
      }
    );
    return response.json();
  } catch (error) {
    console.error('Error searching memories:', error);
    return { memories: [] };
  }
}

// Store customer feedback/contact form
async function storeContactForm(name, email, message) {
  try {
    const response = await fetch(
      `${API_URL}/v1/public/projects/${PROJECT_ID}/database/memory`,
      {
        method: 'POST',
        headers: getHeaders(),
        body: JSON.stringify({
          content: `Contact from ${name} (${email}): ${message}`,
          role: 'user',
          session_id: 'contact-forms',
          metadata: {
            type: 'contact_form',
            name: name,
            email: email,
            timestamp: new Date().toISOString()
          }
        })
      }
    );
    return response.json();
  } catch (error) {
    console.error('Error storing contact form:', error);
  }
}

// ============================================
// CHAT WIDGET
// ============================================

// Get or create session ID
function getSessionId() {
  let sessionId = localStorage.getItem('d20_session_id');
  if (!sessionId) {
    sessionId = 'session-' + Date.now();
    localStorage.setItem('d20_session_id', sessionId);
  }
  return sessionId;
}

// D20 Pizza knowledge base for the chatbot
const D20_KNOWLEDGE = {
  hours: "We're open daily from 12PM to 12AM. Hours may vary - check our Instagram @d20pizza for updates!",
  location: "We're at 1520 Mission St, Santa Cruz, CA 95060. Right on the Westside!",
  phone: "You can reach us at (831) 777-5331",
  pizza_style: "We serve Detroit-style pizza with slow-risen sourdough crust. Our pies are 8x10 inches of deliciousness!",
  menu: "Our fan favorites include: Cup Pepperoni (classic!), Almost Maui (Hawaiian-style), and Nana's Pesto Pesto. We also have legendary avocado toast on sourdough for $18!",
  games: "We have tons of games! D&D, Magic: The Gathering, Go, Ticket to Ride, and many more. Games are available to play for free or purchase!",
  events: "We host Board Game Designers Meetups and other community events. Check our Instagram @d20pizza for upcoming events!",
  name: "D20 refers to the 20-sided dice used in Dungeons & Dragons. We're a pizza place AND a board game café!",
  avocado_toast: "Our avocado toast on fresh-baked sourdough is legendary! It's $18 and totally worth it.",
  reservations: "Walk-ins are welcome! For large groups or events, give us a call at (831) 777-5331."
};

// Simple chatbot response
function getChatResponse(message) {
  const lowerMessage = message.toLowerCase();

  if (lowerMessage.includes('hour') || lowerMessage.includes('open') || lowerMessage.includes('close')) {
    return D20_KNOWLEDGE.hours;
  }
  if (lowerMessage.includes('where') || lowerMessage.includes('location') || lowerMessage.includes('address')) {
    return D20_KNOWLEDGE.location;
  }
  if (lowerMessage.includes('phone') || lowerMessage.includes('call') || lowerMessage.includes('contact')) {
    return D20_KNOWLEDGE.phone;
  }
  if (lowerMessage.includes('menu') || lowerMessage.includes('pizza') || lowerMessage.includes('eat') || lowerMessage.includes('food')) {
    return D20_KNOWLEDGE.menu;
  }
  if (lowerMessage.includes('game') || lowerMessage.includes('play') || lowerMessage.includes('board')) {
    return D20_KNOWLEDGE.games;
  }
  if (lowerMessage.includes('event') || lowerMessage.includes('meetup')) {
    return D20_KNOWLEDGE.events;
  }
  if (lowerMessage.includes('d20') || lowerMessage.includes('name') || lowerMessage.includes('why')) {
    return D20_KNOWLEDGE.name;
  }
  if (lowerMessage.includes('avocado') || lowerMessage.includes('toast')) {
    return D20_KNOWLEDGE.avocado_toast;
  }
  if (lowerMessage.includes('reserv') || lowerMessage.includes('book') || lowerMessage.includes('group')) {
    return D20_KNOWLEDGE.reservations;
  }

  return "Great question! 🎲 I can help with info about our menu, hours, games, events, and more. What would you like to know about D20 Pizza?";
}

// Add message to chat UI
function addChatMessage(text, isUser) {
  const messagesContainer = document.getElementById('chat-messages');
  const messageDiv = document.createElement('div');
  messageDiv.className = `chat-message ${isUser ? 'user' : 'assistant'}`;
  messageDiv.textContent = text;
  messagesContainer.appendChild(messageDiv);
  messagesContainer.scrollTop = messagesContainer.scrollHeight;
}

// Handle sending a chat message
async function handleChatSend() {
  const input = document.getElementById('chat-input');
  const message = input.value.trim();
  if (!message) return;

  // Add user message to UI
  addChatMessage(message, true);
  input.value = '';

  // Store in ZeroDB
  await storeMessage(message, 'user');

  // Search for relevant past context
  const context = await searchMemories(message);

  // Get response
  const response = getChatResponse(message);

  // Add slight delay for natural feel
  setTimeout(async () => {
    addChatMessage(response, false);
    // Store assistant response too
    await storeMessage(response, 'assistant');
  }, 500);
}

// ============================================
// INITIALIZE
// ============================================

document.addEventListener('DOMContentLoaded', () => {
  // Chat toggle
  const chatToggle = document.getElementById('chat-toggle');
  const chatContainer = document.getElementById('chat-container');
  const chatClose = document.getElementById('chat-close');
  const chatSend = document.getElementById('chat-send');
  const chatInput = document.getElementById('chat-input');

  chatToggle?.addEventListener('click', () => {
    chatContainer.classList.toggle('hidden');
  });

  chatClose?.addEventListener('click', () => {
    chatContainer.classList.add('hidden');
  });

  chatSend?.addEventListener('click', handleChatSend);

  chatInput?.addEventListener('keypress', (e) => {
    if (e.key === 'Enter') handleChatSend();
  });

  // Add welcome message
  setTimeout(() => {
    if (document.getElementById('chat-messages')) {
      addChatMessage("Hey there! 🎲 Welcome to D20 Pizza! Ask me about our menu, games, hours, or anything else!", false);
    }
  }, 1000);

  // Load featured pizzas
  loadFeaturedPizzas();
});

// Load featured pizzas
function loadFeaturedPizzas() {
  const pizzaGrid = document.querySelector('.pizza-grid');
  if (!pizzaGrid) return;

  const pizzas = [
    {
      name: "Cup Pepperoni",
      description: "Classic Detroit-style with crispy curled pepperoni cups",
      price: "$18"
    },
    {
      name: "Almost Maui",
      description: "Hawaiian-inspired with ham, pineapple, and our signature sauce",
      price: "$19"
    },
    {
      name: "Nana's Pesto Pesto",
      description: "Fresh basil pesto with mozzarella and parmesan",
      price: "$20"
    }
  ];

  pizzas.forEach(pizza => {
    const card = document.createElement('div');
    card.className = 'pizza-card';
    card.innerHTML = `
      <div style="height: 200px; background: linear-gradient(135deg, var(--primary), var(--accent)); display: flex; align-items: center; justify-content: center;">
        <span style="font-size: 4rem;">🍕</span>
      </div>
      <div class="pizza-card-content">
        <h3>${pizza.name}</h3>
        <p>${pizza.description}</p>
        <span class="pizza-price">${pizza.price}</span>
      </div>
    `;
    pizzaGrid.appendChild(card);
  });
}
```

---

## How to Help Me Build This

1. **Start with the basics** - Create the folder structure and index.html
2. **Add styling** - Make it look like a real D20 Pizza website
3. **Connect ZeroDB** - Set up the chat widget with memory
4. **Add interactivity** - Make the chat actually work
5. **Polish** - Add animations, responsive design, final touches

Let's start building! Create the initial project structure for me.

---

## END OF PROMPT

---

# Instructions for Instructors

## Teaching Flow

1. **Intro (2 min)**: "We're building a real website for D20 Pizza - the place we're sitting in right now!"

2. **Project Setup (5 min)**: Create folder, open in VS Code, create initial files

3. **HTML Structure (10 min)**: Build the basic page layout, explain each section

4. **CSS Styling (10 min)**: Add the D20 theme, make it look professional

5. **ZeroDB Connection (15 min)**:
   - Explain what ZeroDB does
   - Show how to store chat messages
   - Demonstrate searching memories

6. **Chat Widget (15 min)**:
   - Build the UI
   - Add the chatbot logic
   - Connect to ZeroDB for memory

7. **Testing & Polish (5 min)**:
   - Test the chat
   - Show memories being stored
   - Make small improvements

## Key Teaching Points

- **AI Kit**: We're using simple HTML/CSS/JS but AI Kit provides the same patterns for React
- **ZeroDB**: Every chat message is stored and searchable - this is how agents "remember"
- **Real-world application**: This could be a real website for D20 Pizza!

## Backup Plan

If attendees get stuck:
1. Share the complete code files
2. Have them just modify the `D20_KNOWLEDGE` object to customize responses
3. Focus on the ZeroDB concepts even if the code doesn't work perfectly
