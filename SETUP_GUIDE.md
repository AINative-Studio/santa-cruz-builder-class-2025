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

## Step 1: Install AINative Studio IDE - 5 minutes

AINative Studio IDE is our custom code editor with AI assistance built-in. It's free and works on Mac, Windows, and Linux!

### Download AINative Studio IDE (Recommended)

**Go to:** **https://github.com/AINative-Studio/AINativeStudio-IDE/releases**

**Download the right version for your computer:**

#### For Mac:
- **Apple Silicon (M1/M2/M3):** Download `AINativeStudio-v1.1.0-macOS-arm64.dmg`
- **Intel Mac:** Download `AINativeStudio-v1.1.0-macOS-x64.dmg`
- **Not sure which?** Click the Apple logo in the top left → "About This Mac" → Look for "Chip" (M1/M2/M3 = Apple Silicon)

**To install on Mac:**
1. Open the downloaded `.dmg` file
2. Drag AINative Studio to your Applications folder
3. Open from Applications (right-click → Open the first time)

#### For Windows:
- **Most computers:** Download `AINativeStudio-v1.1.0-Windows-x64-UserInstaller.exe`
- **ARM Windows:** Download `AINativeStudio-v1.1.0-Windows-arm64-UserInstaller.exe`

**To install on Windows:**
1. Run the downloaded `.exe` file
2. Click "Next" through the installer
3. Open AINative Studio from the Start menu

#### For Linux:
- **Ubuntu/Debian:** Download `AINativeStudio-v1.1.0-Linux-x64.deb`
- **Fedora/RHEL:** Download `AINativeStudio-v1.1.0-Linux-x64.rpm`
- **Other:** Download `AINativeStudio-v1.1.0-Linux-x64.AppImage`

**To install on Linux:**
```bash
# Debian/Ubuntu
sudo dpkg -i AINativeStudio-v1.1.0-Linux-x64.deb

# Fedora/RHEL
sudo rpm -i AINativeStudio-v1.1.0-Linux-x64.rpm

# AppImage (any distro)
chmod +x AINativeStudio-v1.1.0-Linux-x64.AppImage
./AINativeStudio-v1.1.0-Linux-x64.AppImage
```

---

### Alternative IDEs (if you prefer)

If you already have a code editor you're comfortable with, that works too:

- **VS Code:** https://code.visualstudio.com
- **Cursor:** https://cursor.sh
- **Windsurf:** https://codeium.com/windsurf

**Checkpoint:** Can you open AINative Studio IDE (or your preferred editor) and see a window where you could type? If yes, move to Step 2!

---

## Step 2: AI Assistant Setup - 2 minutes

**Good news!** If you installed AINative Studio IDE, AI assistance is already built-in! You just need to configure it.

### If Using AINative Studio IDE (Recommended)

The AI assistant is already included! Here's how to activate it:

1. Open AINative Studio IDE
2. Look for the **AI Assistant** panel (usually on the right side or bottom)
3. If prompted, sign in with your AINative account (same one you'll create in Step 3)
4. You're ready to go!

**To use the AI assistant:**
- Click in the AI panel and type your question
- Or press `Cmd+Shift+A` (Mac) / `Ctrl+Shift+A` (Windows) to open AI chat
- Ask it to help you write code!

---

### If Using a Different IDE

If you chose VS Code, Cursor, or another editor, you'll need to add an AI assistant:

#### Option A: Claude Code (Terminal-based)
```bash
# Install Node.js first from nodejs.org, then run:
npm install -g @anthropic-ai/claude-code
```
- Get API key from: https://console.anthropic.com

#### Option B: GitHub Copilot (VS Code Extension)
1. Open VS Code → Extensions → Search "GitHub Copilot" → Install
2. Sign in with GitHub account (free trial available)

#### Option C: Codeium (Free VS Code Extension)
1. Open VS Code → Extensions → Search "Codeium" → Install
2. Create free account when prompted

**Checkpoint:** Can you access your AI assistant? Try asking "How do I create a new file?" If it responds, you're ready!

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

- [ ] I installed AINative Studio IDE (or another code editor)
- [ ] I can open my code editor and see where to type code
- [ ] I can access the AI assistant (built into AINative Studio IDE)
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

## "I can't install AINative Studio IDE"

**Problem:** The download or installation isn't working.

**Solutions:**
- Make sure you're downloading the right version for your computer:
  - **Mac M1/M2/M3:** Download the `arm64` version
  - **Mac Intel:** Download the `x64` version
  - **Windows:** Download the `x64-UserInstaller.exe`
- On Mac: You might need to right-click and select "Open" the first time
- On Windows: If blocked, click "More info" then "Run anyway"
- Try an alternative: VS Code (code.visualstudio.com) or Cursor (cursor.sh)

---

## "Which Mac version do I have?"

**Problem:** You're not sure if you have Apple Silicon or Intel.

**Solution:**
1. Click the **Apple logo** in the top-left corner of your screen
2. Click **"About This Mac"**
3. Look for **"Chip"** or **"Processor"**:
   - If it says **M1, M2, M3, or M4** → Download the `arm64` version
   - If it says **Intel** → Download the `x64` version

---

## "I don't know how to open a terminal"

**Problem:** You're not sure where to type commands.

**Solution in AINative Studio IDE:**
1. Open AINative Studio IDE
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
| **AINative Studio IDE** | Code editor + AI (Recommended!) | github.com/AINative-Studio/AINativeStudio-IDE/releases |
| VS Code | Alternative code editor | code.visualstudio.com |
| Cursor | Alternative AI editor | cursor.sh |

**Minimum setup:** AINative Studio IDE + AINative account with API key

**That's it!** AINative Studio IDE has everything built-in.
