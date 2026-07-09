# Automated Twitter Engagement Extension (Global Auto-Reply)

A smart, automated Google Chrome extension that reads your X (formerly Twitter) feed and posts human-like, context-aware replies using AI. It uses the Groq API (Llama 3) to generate natural comments and includes humanized interactions like reading delays, random skipping, and typing simulations.

## Features

- **AI-Powered Replies**: Automatically generates context-aware replies to posts using Groq's high-speed API (Llama-3.1-8b-instant).
- **Human-Like Behavior**: 
  - Simulates reading time based on the tweet's length.
  - Randomly chooses to skip some posts (25% chance) to mimic a real user's browsing habit.
  - Simulates the visual typing process.
- **Japanese-Only Mode (日本語のみ)**: A newly added feature! When toggled on, the bot will exclusively interact with and reply to Japanese posts. The replies will automatically be generated in Japanese.
- **On-Screen Status UI**: A sleek, non-intrusive status box appears on the screen, showing exactly what the bot is currently thinking, reading, or typing. It also visually highlights the active tweet it is processing.
- **Memory**: Remembers the posts it has already replied to during previous sessions to prevent duplicate comments on the same post.
- **Easy Configuration**: Simple popup menu to input your API key and toggle the bot's status and Japanese-only filter.

## Installation

Since this is an unpacked extension, you'll need to load it in Developer Mode:

1. Clone or download this repository to your local machine.
2. Open Google Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer mode** using the toggle switch in the top right corner.
4. Click the **Load unpacked** button in the top left.
5. Select the folder containing the extension files.
6. The extension is now installed! You should see the Global Auto-Reply icon in your Chrome toolbar.

## Usage

1. Click on the extension icon in your toolbar to open the popup.
2. Enter your **Groq API Key** in the provided field and click **Save Settings**. (You can get a free API key from the [Groq Console](https://console.groq.com/)).
3. Toggle the **Bot Status** switch to turn the auto-replier ON. 
4. (Optional) Toggle the **日本語のみ (JP Only)** switch if you only want it to interact with Japanese tweets.
5. Open [X (Twitter)](https://x.com/) in a new tab. 
6. Watch as the bot automatically scans the feed, selects posts, generates replies, and interacts on your behalf!

## Important Notes & Best Practices

- **Rate Limits & Bans**: Use automation on Twitter at your own risk. The random delays and skipping mechanics are designed to reduce the chances of your account being flagged, but X can still detect automated behavior. 
- **Screen Visibility**: The script scans the tweets currently visible in the DOM. Ensure your tab remains active for the most consistent behavior. 

## Technical Stack

- Vanilla JavaScript (ES6)
- Chrome Extension Manifest V3
- Groq API (OpenAI-compatible endpoints)
- CSS3 (Glassmorphism & modern UI in popup)
