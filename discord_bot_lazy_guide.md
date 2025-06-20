## ✅ Step 1: Choose the Easiest Language

Use **JavaScript (with Node.js)**  
It’s the most popular and has the easiest tutorials & libraries.

Alternative (if you know some Python):  
Use **Python** (with `discord.py`)

> But for the fastest start: **Go with JavaScript + discord.js**

---

## ✅ Step 2: Tools You Need (Once Only)

Install these:
1. **[Node.js](https://nodejs.org)** (get the LTS version)
2. **[Visual Studio Code](https://code.visualstudio.com)** (easy code editor)
3. **Discord account + test server** (make a new server for testing)

---

## ✅ Step 3: Quick Start Bot (Node.js)

### 1. In VS Code terminal:
```bash
mkdir my-bot
cd my-bot
npm init -y
npm install discord.js dotenv
```

### 2. Create a `.env` file (to store your bot token)
```env
DISCORD_TOKEN=your_bot_token_here
```

### 3. Create `index.js` and paste this:
```js
require('dotenv').config();
const { Client, GatewayIntentBits } = require('discord.js');

const client = new Client({ intents: [GatewayIntentBits.Guilds, GatewayIntentBits.GuildMessages, GatewayIntentBits.MessageContent] });

client.on('ready', () => {
    console.log(`Logged in as ${client.user.tag}`);
});

client.on('messageCreate', (msg) => {
    if (msg.content === '!ping') {
        msg.reply('Pong!');
    }
});

client.login(process.env.DISCORD_TOKEN);
```

---

## ✅ Step 4: Create Bot on Discord

1. Go to [Discord Developer Portal](https://discord.com/developers/applications)
2. Create App → Go to "Bot" tab → Add Bot
3. Copy Token → Paste in `.env`
4. Go to OAuth2 → URL Generator:
   - Scopes: `bot`
   - Bot Permissions: `Send Messages`, `Read Messages`
5. Copy generated URL → Paste in browser → Invite your bot to your test server

---

## ✅ Step 5: Run the Bot

In terminal:
```bash
node index.js
```

Then go to Discord and type:
```
!ping
```

Your bot should reply:
```
Pong!
```

---

## 🚀 That’s it. You now have a working bot.

---

## 🧠 Next Lazy Steps (When You Feel Like It)

- Change `!ping` to other commands (`!joke`, `!help`, etc.)
- Add command handlers
- Try using buttons, slash commands, or image embeds

---

## 🏁 Summary

| Thing         | Use This             |
|---------------|----------------------|
| Language      | JavaScript (Node.js) |
| Library       | `discord.js`         |
| IDE           | VS Code              |
| Bot Hosting   | Local (or Replit/Glitch for lazy cloud deploy) |

---

If you want, I can make you a **copy-paste template** with multiple commands and auto-reply. Want that?