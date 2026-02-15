# Khalil - Your AI Companion

A simple, beautiful chat interface for your personal AI assistant powered by Claude.

## 🚀 Quick Start

1. **Get an API Key**
   - Visit [Anthropic Console](https://console.anthropic.com/)
   - Sign up or log in
   - Navigate to API Keys
   - Create a new API key

2. **Open the App**
   - Simply open `khalil-chat.html` in your web browser
   - Enter your API key when prompted
   - Start chatting!

## ✨ Features

- **Beautiful, modern UI** with smooth animations
- **Conversation memory** - Khalil remembers your chat context
- **Warm personality** - Designed to be a thoughtful companion
- **Local storage** - Your API key is saved in your browser
- **Fully client-side** - No backend needed, runs entirely in browser

## 🎨 What Makes Khalil Special

Khalil is designed with a distinctive aesthetic:
- Dark, atmospheric theme with subtle gradient effects
- Crimson Pro serif font for headings (elegant, editorial feel)
- DM Sans for body text (clean, modern)
- Animated background with drifting gradients
- Smooth micro-interactions and transitions
- Pulsing logo effect

## 💡 Current Capabilities

Right now, Khalil can:
- Have natural conversations
- Remember context within the current session
- Provide advice and suggestions
- Help with planning and thinking through problems
- Be a supportive listener

## 🔮 Next Steps to Build Your Full Vision

### Phase 1: Add Persistent Memory
```javascript
// Use browser's IndexedDB to store conversations
const db = await openDB('khalil-db', 1, {
  upgrade(db) {
    db.createObjectStore('conversations');
    db.createObjectStore('memories');
  }
});
```

### Phase 2: Integrate with Your Data
**Email Integration:**
- Use Gmail API to read emails
- Summarize daily emails
- Draft responses

**Calendar Integration:**
- Google Calendar API
- Remind you of upcoming events
- Suggest scheduling

**File Access:**
- Process uploaded documents
- Remember important information

### Phase 3: Proactive Features
- **Scheduled check-ins**: "How did that meeting go?"
- **Context awareness**: Know your schedule and suggest accordingly
- **Pattern recognition**: Learn your preferences over time

### Phase 4: Multi-Platform
**Mobile App:**
- React Native version
- Push notifications
- Voice input

**Desktop App:**
- Electron wrapper
- System tray integration
- Keyboard shortcuts

## 🛠 Technical Architecture

### Current Stack
- **Frontend**: React (via CDN)
- **AI**: Claude Sonnet 4 (via Anthropic API)
- **Storage**: localStorage (for API key)

### Recommended Future Stack
- **Backend**: Node.js + Express or Python + FastAPI
- **Database**: PostgreSQL + pgvector (for semantic search)
- **AI**: Continue with Claude API
- **Memory**: Vector database for long-term memory
- **Auth**: Firebase Auth or Auth0
- **Hosting**: Vercel, Netlify, or self-hosted

## 🔒 Privacy & Security

**Current:**
- API key stored in browser localStorage
- All conversations happen directly with Anthropic
- No data sent to third parties

**For Production:**
- Never expose API keys client-side
- Use backend proxy for API calls
- Encrypt stored conversations
- Implement user authentication
- Add data retention policies

## 📝 Customization

### Change Khalil's Personality
Edit the system prompt in the code (line ~423):
```javascript
system: `You are Khalil, a warm, thoughtful AI companion...`
```

### Modify the Design
All styling is in the `<style>` section. Key variables:
```css
:root {
    --bg-primary: #0a0e16;
    --accent-primary: #4a9eff;
    --accent-secondary: #00d4aa;
    /* ... */
}
```

### Add New Features
The code is well-structured for extensions:
- `sendMessage()` - handles API communication
- `handleSubmit()` - processes user input
- Message rendering is in the JSX

## 🚧 Limitations

- **No memory between sessions** - conversations reset when you refresh
- **Client-side API key** - not secure for production
- **No file uploads** - can't analyze documents yet
- **Browser-only** - no mobile app yet
- **No integrations** - can't access email, calendar, etc.

## 📚 Resources for Next Steps

**APIs to Explore:**
- [Gmail API](https://developers.google.com/gmail/api)
- [Google Calendar API](https://developers.google.com/calendar)
- [Anthropic API Docs](https://docs.anthropic.com/)

**Frameworks:**
- [React Native](https://reactnative.dev/) - for mobile
- [Electron](https://www.electronjs.org/) - for desktop
- [FastAPI](https://fastapi.tiangolo.com/) - for backend

**Database Options:**
- [Supabase](https://supabase.com/) - PostgreSQL + Auth
- [Pinecone](https://www.pinecone.io/) - Vector database
- [Weaviate](https://weaviate.io/) - Vector search

## 💬 Usage Tips

- **Be conversational** - Khalil responds best to natural language
- **Provide context** - The more you share, the better Khalil can help
- **Use regularly** - Build a conversation history
- **Try the suggestions** - Use the starter prompts to get going

## 🎯 Ideas for Enhancement

1. **Voice input/output** - Talk to Khalil
2. **Daily summaries** - Get a recap of your day
3. **Goal tracking** - Set and track personal goals
4. **Mood tracking** - Log how you're feeling
5. **Smart notifications** - Reminders based on context
6. **Multi-user** - Different profiles for different users
7. **Export conversations** - Download your chat history
8. **Themes** - Light mode, different color schemes

## 🤝 Contributing Ideas

Want to extend Khalil? Here are some starter projects:

- Build a backend API
- Add voice input using Web Speech API
- Create a Chrome extension version
- Add markdown rendering for messages
- Implement conversation export (JSON/CSV)
- Build a settings panel
- Add conversation search

---

**Built with ❤️ using Claude Sonnet 4**

Need help? Questions? Want to share what you build? Let me know!
