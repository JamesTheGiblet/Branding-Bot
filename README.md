Okay, this one is meta. I'm using my brand voice to describe a bot that helps you keep *your* brand voice consistent. If this thing becomes self-aware, we're all in trouble.

## **Project: Brand Bot**

A tool for keeping your brand voice consistent everywhere.

### **The Problem**

Keeping your tone consistent across Twitter, LinkedIn, your blog, and your emails is a pain. You end up sounding like three different people, and your message gets muddy. It's a full-time job to make sure you're always using the right keywords, tone, and style.

-----

### **The Solution**

A simple tool that learns your brand's voice and helps you write, schedule, and analyze all your content from one place. It combines a few smart APIs to act as your strategic partner, making sure you always sound like you.

-----

### **What It Does**

#### **1. Write & Refine Content**

  * **Brand Interview:** First, the bot runs you through a guided Q\&A to learn your brand's mission, values, and personality.
  * **Saves Your Profile:** It saves this profile to a local SQLite database on your machine. Your brand identity doesn't live in the cloud.
  * **Rewrites in Your Voice:** You give it rough text, and it uses the **Gemini API** to rewrite it in your specific style.
  * **Platform-Aware:** It knows the difference between a LinkedIn article and a Tweet and adjusts the format accordingly.
  * **Consistency Check:** It uses **spaCy** to scan the text and make sure your key terms and phrases are present and used correctly.

#### **2. Schedule Posts & Track Performance**

  * **Post Scheduler:** Schedule your polished content to go out to your social channels directly from the app.
  * **Content Log:** Every piece of content—from rough draft to final post—is logged in the database so you have a complete history.
  * **Performance Analytics:** It pulls basic metrics (likes, shares, etc.) for your posts so you can see what's working and what's not, without having to check ten different websites.

-----

### **Two Ways to Use It: GUI or CLI**

It’s built for everyone, from beginners to power users.

  * **GUI (Graphical User Interface):** An easy-to-use desktop app where you can manage everything visually. This is the recommended way to start.
  * **CLI (Command Line Interface):** For developers and people who live in the terminal. You can automate tasks and plug the bot's functions into your own scripts.

-----

### **The Tech Stack (No Magic Involved)**

This isn't an "invocation," it's a stack of solid, modern tools.

  * **Core AI:** **Google Gemini API** for all the heavy lifting on content generation and refinement.
  * **Orchestration:** **LangChain** to chain together prompts and actions, creating the workflow from raw text to finished post.
  * **NLP:** **spaCy** for the linguistic analysis—pulling out keywords and ensuring consistency.
  * **Language:** **Python**. It's the glue that holds everything together.
  * **Database:** **SQLite**. A simple, file-based database to store user profiles locally. No external server needed.

-----

### **How to Get Started**

**Prerequisites:**

  * Python 3.8+
  * A Google Gemini API Key
  * API keys for a social media management service (like Ayrshare)

**Installation:**

1.  **Clone the repo:**
    ```bash
    git clone https://github.com/YourUsername/praximous-brand-bot.git
    cd praximous-brand-bot
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Set up your `.env` file** with your API keys:
    ```
    GEMINI_API_KEY="YOUR_API_KEY_HERE"
    SOCIAL_MEDIA_API_KEY="YOUR_SOCIAL_MEDIA_API_KEY_HERE"
    ```

**Usage:**
Run the main script to start the brand setup interview.

```bash
python main.py
```

Follow the prompts. Once your profile is saved, you're ready to go.

-----

### **The Roadmap (What's Next)**

**Perfect is the imaginary friend of never shipped**, but here's where it's headed:

  * **Web UI:** A web-based version so you can access it from anywhere.
  * **More Integrations:** Direct plugins for WordPress, Shopify, etc.
  * **Deeper Analytics:** Sentiment analysis and better audience engagement metrics.
  * **Autonomous Mode:** Use LangChain Agents to let it create draft posts based on a topic or a URL.
  * **Team Features:** Allow multiple users to work under one brand—for agencies and larger teams.
