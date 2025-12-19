# Pre-Class Email to Attendees

---

**Subject:** Get Ready for Today's Builder Class! (Quick setup guide)

---

Hi there!

We're so excited to see you TODAY at the **AINative Holiday Builder Class** at D20 Pizza in Santa Cruz!

To make sure you get the most out of our hands-on session, please complete these **setup steps before arriving**. This takes about 20-30 minutes, and we've made the instructions super beginner-friendly!

---

## What You'll Need Today

- [ ] A laptop (Mac, Windows, or Linux - any will work!)
- [ ] A code editor (IDE) installed (see Step 1)
- [ ] An AI coding assistant in your editor (see Step 2)
- [ ] An AINative account with API key (see Step 3)
- [ ] A good attitude and curiosity!

**Don't worry about:** Knowing how to program or having any prior coding experience. The AI assistant will help you write the code!

---

## Step 1: Install a Code Editor (IDE) - 10 minutes

A code editor (also called an IDE) is where you'll write and run your code. Choose ONE of these options:

### Option A: VS Code (Recommended for Beginners)

**What it is:** A free, beginner-friendly code editor made by Microsoft.

**How to install:**

1. Go to: **https://code.visualstudio.com**
2. Click the big **"Download"** button
   - It will automatically detect if you're on Mac, Windows, or Linux
3. Once downloaded, open the installer file:
   - **Mac:** Open the `.dmg` file, drag VS Code to your Applications folder
   - **Windows:** Run the `.exe` file, click "Next" through the installer
4. Open VS Code to make sure it works
5. You should see a welcome screen - you're done!

### Option B: Cursor (AI-First Editor)

**What it is:** A code editor built specifically for AI-assisted coding (based on VS Code).

**How to install:**

1. Go to: **https://cursor.sh**
2. Click **"Download"**
3. Install just like VS Code above
4. Open Cursor to make sure it works

### Option C: Windsurf by Codeium

**What it is:** Another AI-powered code editor option.

**How to install:**

1. Go to: **https://codeium.com/windsurf**
2. Click **"Download"**
3. Follow the installation steps
4. Open to verify it works

**Checkpoint:** Can you open your code editor and see a window where you could type? If yes, move to Step 2!

---

## Step 2: Install an AI Coding Assistant - 10 minutes

Now let's add an AI assistant to your code editor. This is what will help you write code during the class! Choose ONE option:

### Option A: Claude Code (Recommended)

**What it is:** Anthropic's AI coding assistant that runs in your terminal.

**How to install:**

1. Open your code editor (VS Code or Cursor)

2. Open the Terminal inside your editor:
   - **Mac:** Press `Cmd + `` ` (the key below Escape)
   - **Windows:** Press `Ctrl + `` `
   - Or go to menu: **View → Terminal**

3. You should see a command line at the bottom of your screen

4. Type this command and press Enter:
   ```
   npm install -g @anthropic-ai/claude-code
   ```

   **Don't have npm?** If you see an error, you need Node.js first:
   - Go to: **https://nodejs.org**
   - Download the **LTS** version (the green button)
   - Install it, then try the command above again

5. Once installed, type this to verify:
   ```
   claude --version
   ```
   You should see a version number!

6. To use Claude Code, you'll need an API key from Anthropic:
   - Go to: **https://console.anthropic.com**
   - Create an account
   - Go to API Keys and create one
   - When you run `claude` for the first time, it will ask for this key

### Option B: GitHub Copilot (in VS Code)

**What it is:** Microsoft/GitHub's AI coding assistant.

**How to install:**

1. Open VS Code
2. Click the **Extensions** icon on the left sidebar (looks like 4 squares)
3. Search for **"GitHub Copilot"**
4. Click **"Install"** on the GitHub Copilot extension
5. You'll need to sign in with a GitHub account
6. There's a free trial available, or it's free for students!

### Option C: Codeium (Free, in VS Code)

**What it is:** A free AI coding assistant.

**How to install:**

1. Open VS Code
2. Click the **Extensions** icon on the left sidebar
3. Search for **"Codeium"**
4. Click **"Install"**
5. Create a free account when prompted
6. You're ready to go!

### Option D: Gemini CLI (Google's AI)

**What it is:** Google's AI assistant for coding.

**How to install:**

1. Open your terminal (inside VS Code or separately)
2. Run:
   ```
   npm install -g @google/generative-ai
   ```
3. You'll need a Google Cloud account and API key
4. Follow setup at: **https://ai.google.dev**

**Checkpoint:** Can you access your AI assistant in your code editor? Try asking it a simple question like "How do I create a new file?" If it responds, you're ready!

---

## Step 3: Create Your AINative Account & API Key - 5 minutes

Now let's set up your AINative account so you can access our platform during the class.

### 3a. Register on AINative

1. Go to: **https://ainative.studio**
2. Click **"Sign Up"** or **"Get Started"** in the top right
3. Fill in your information:
   - Email address
   - Password (at least 8 characters, include a number and special character)
   - Your name
4. Click **"Create Account"**
5. Check your email and click the verification link
6. Log in to your new account

### 3b. Create Your API Key

This is the "password" that lets your app talk to AINative.

1. Once logged in, click on your **profile icon** (top right corner)
2. Go to **"Developer Settings"** or **"Settings → Developer"**
3. Find the **"API Keys"** section
4. Click **"Create New API Key"** or **"Generate API Key"**
5. Give it a name like: `Holiday Builder Class`
6. Click **"Create"**
7. **IMPORTANT:** Copy the API key immediately and save it somewhere safe!
   - It looks something like: `sk-abc123xyz789...`
   - You won't be able to see it again after you close the window!

### 3c. Create a Project (for ZeroDB)

1. While still logged in, go to the **Dashboard**
2. Click **"Create New Project"** or **"+ New Project"**
3. Name it: `Holiday Builder Project`
4. Click **"Create"**
5. Note down your **Project ID** (it looks like: `550e8400-e29b-41d4-a716-446655440000`)

**Write down these credentials - you'll need them in class!**

```
Email:      ________________________________
Password:   ________________________________
API Key:    ________________________________
Project ID: ________________________________
```

---

## Step 4: Test That Everything Works - 2 minutes

Let's make sure you're all set:

- [ ] I installed a code editor (VS Code, Cursor, or Windsurf)
- [ ] I can open my code editor and see where to type code
- [ ] I installed an AI coding assistant (Claude Code, Copilot, or Codeium)
- [ ] I can ask my AI assistant questions and get responses
- [ ] I created an account at ainative.studio
- [ ] I created an API key in Developer Settings
- [ ] I created a project and noted my Project ID
- [ ] I saved all my credentials somewhere safe

**If you got stuck anywhere, don't worry!** Just arrive a few minutes early and we'll help you get set up. Or reply to this email and we'll help you right away!

---

## What to Expect Today

**Schedule:**
- ☕ **10:00 AM** - Welcome & Setup Check
- 🧠 **10:10 AM** - Part 1: AI Kit (Adding AI to Apps)
- 🤖 **10:40 AM** - Part 2: Agent APIs (Smart Workflows)
- ☕ **11:15 AM** - Quick Coffee Break
- 💾 **11:20 AM** - Part 3: ZeroDB (Giving AI Memory)
- 🎉 **11:50 AM** - Q&A & What's Next

**After the class (12:00 PM - 4:00 PM):**
- Open coworking
- Continue building your app
- Network with fellow builders
- Grab some amazing D20 avocado toast!

---

## Quick Reference Card (Save or Print This!)

Keep this info handy during the class:

```
╔══════════════════════════════════════════════╗
║        MY AINATIVE CREDENTIALS               ║
╠══════════════════════════════════════════════╣
║                                              ║
║  Email: ________________________________     ║
║                                              ║
║  Password: ____________________________      ║
║                                              ║
║  API Key: _____________________________      ║
║           _____________________________      ║
║                                              ║
║  Project ID: __________________________      ║
║                                              ║
╠══════════════════════════════════════════════╣
║        IMPORTANT URLS                        ║
╠══════════════════════════════════════════════╣
║                                              ║
║  AINative:     ainative.studio               ║
║  ZeroDB:       zerodb.ainative.studio        ║
║  API Docs:     api.ainative.studio/docs      ║
║                                              ║
╚══════════════════════════════════════════════╝
```

---

## Questions? Need Help Right Now?

- **Reply to this email** - We'll respond quickly!
- **Check the FAQ** at ainative.studio/faq
- **Join our Discord** at discord.gg/ainative

---

## One More Thing...

During the class, we'll give you a **special starter prompt** that teaches your AI assistant everything about AINative. This means even if you've never coded before, your AI will guide you through building a real application!

Just come ready with your setup complete, and we'll handle the rest.

---

See you in a few minutes at **D20 Pizza** (1520 Mission St, Santa Cruz)!

Can't wait to build something amazing with you.

Happy holidays!

**The AINative Team**

P.S. - D20 has amazing coffee and their avocado toast on sourdough is legendary. Just saying!

---

# Event Details Quick Reference

- **Date:** Friday, December 19, 2025
- **Time:** 10:00 AM - 12:00 PM (class), 12:00 PM - 4:00 PM (open coworking)
- **Location:** D20 Pizza, 1520 Mission St, Santa Cruz, CA 95060
- **Cost:** FREE!
- **What to bring:** Laptop (with setup complete), charger, curiosity

---

# Troubleshooting Guide (For Non-Technical Attendees)

## "I can't install VS Code"

**Problem:** The download or installation isn't working.

**Solutions:**
- Make sure you're downloading the right version for your computer (Mac/Windows/Linux)
- On Mac: You might need to right-click and select "Open" the first time
- On Windows: If blocked, click "More info" then "Run anyway"
- Try using Cursor instead: cursor.sh

---

## "npm command not found"

**Problem:** When you try to install Claude Code, it says npm isn't recognized.

**Solution:**
1. You need to install Node.js first
2. Go to: https://nodejs.org
3. Download the **LTS** version (left button, usually green)
4. Install it (just click Next through everything)
5. **Close and reopen** your terminal/VS Code
6. Try the npm command again

---

## "I don't know how to open a terminal"

**Problem:** You're not sure where to type commands.

**Solution:**
1. Open VS Code (or your code editor)
2. Look at the top menu bar
3. Click **View** → **Terminal**
4. A panel should appear at the bottom
5. That's where you type commands!

**Keyboard shortcut:**
- Mac: `Cmd + `` ` (backtick key, below Escape)
- Windows: `Ctrl + `` `

---

## "I can't find Developer Settings"

**Problem:** You're logged into AINative but can't find where to create an API key.

**Solution:**
1. Look in the top-right corner for your profile icon or name
2. Click it to open a dropdown menu
3. Look for "Settings", "Developer Settings", or "Account"
4. Inside settings, look for "API Keys" or "Developer" tab
5. If still stuck, try going directly to: ainative.studio/settings/developer

---

## "My API key disappeared"

**Problem:** You created an API key but didn't copy it, and now you can't see it.

**Solution:**
- API keys are only shown once for security
- You'll need to create a new one
- Delete the old one (if you can see its name) and create fresh
- This time, **immediately** copy and save it!

---

## "I don't have a laptop"

**Problem:** You don't have a laptop to bring.

**Solutions:**
- That's okay! You can still attend and learn
- Pair up with someone who has a laptop
- Take notes and try it at home later
- Let us know ahead of time and we might be able to help arrange something

---

## "I've never coded before - will I be lost?"

**Problem:** You're worried you won't be able to follow along.

**Answer:** Not at all! Here's why:
- The AI coding assistant does most of the work
- You'll mainly be describing what you want in plain English
- We explain everything step-by-step
- The instructors will help anyone who gets stuck
- Many attendees have zero coding experience!

Just come with curiosity and we'll take care of the rest.

---

## "My AI assistant isn't responding"

**Problem:** You installed an AI assistant but it's not working.

**Solutions:**
- **Claude Code:** Make sure you entered your Anthropic API key
- **GitHub Copilot:** Make sure you're signed into GitHub
- **Codeium:** Make sure you created and verified your account
- Try restarting your code editor
- Check your internet connection

---

## "I'm getting errors I don't understand"

**Problem:** Something went wrong and you don't know what to do.

**Solution:**
- Take a screenshot of the error
- Don't stress - errors are normal!
- Reply to this email with the screenshot
- Or just arrive and we'll fix it together at the venue

---

**Still have questions? Reply to this email anytime - we're here to help!**

---

# Software Summary (Everything You Need)

| Software | Purpose | Download Link |
|----------|---------|---------------|
| VS Code | Code editor | code.visualstudio.com |
| Cursor | AI code editor | cursor.sh |
| Node.js | Runs JavaScript | nodejs.org |
| Claude Code | AI assistant | `npm install -g @anthropic-ai/claude-code` |
| GitHub Copilot | AI assistant | VS Code Extensions |
| Codeium | AI assistant (free) | VS Code Extensions |

**Minimum setup:** VS Code + Node.js + one AI assistant + AINative account with API key
