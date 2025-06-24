
# 🤝 Auto Approver Join Request Bot

## 📖 Overview
The **Auto Approver Join Request Bot** is a Telegram bot built with Pyrogram to automate the approval of join requests for Telegram groups and channels. It instantly approves users who request to join, saving admins time and effort. Upon approval, the bot sends a personalized welcome message to the user via private chat, including links to related channels for further engagement. The bot also provides a simple `/start` command for users to interact with it directly.

This bot is ideal for Telegram group or channel admins who want to streamline the onboarding process while promoting their community or related content.

---

## ✨ Key Features
- **Automatic Join Request Approval**: Instantly approves join requests for groups and channels.
- **Personalized Welcome Message**: Sends a custom greeting with the user’s first name in their private chat.
- **Promotional Buttons**: Includes inline buttons in the welcome message linking to other Telegram channels.
- **Start Command**: Responds to `/start` with a welcome message and buttons to add the bot to groups/channels or contact the owner.
- **Lightweight & Efficient**: Built with Pyrogram for fast and reliable performance.
- **Console Logging**: Logs the first name of users who join for basic tracking.

---

## 🔧 How It Works
1. **Setup**:
   - Add the bot to your Telegram group or channel with admin privileges.
   - Ensure it has permission to manage join requests.

2. **Join Request Handling**:
   - When a user requests to join the group/channel, the bot automatically approves them.
   - The user’s first name is logged to the console.

3. **Welcome Message**:
   - The bot sends a private message to the approved user.
   - The message includes a greeting and inline buttons linking to other Telegram channels (e.g., for free content or courses).

4. **User Interaction**:
   - Users can send `/start` in private chat to receive a welcome message.
   - The message includes buttons to add the bot to a group/channel or contact the owner.

---

## 📌 Commands
| Command   | Description                              |
|-----------|------------------------------------------|
| `/start`  | Sends a welcome message with action buttons. |

---

## 🛠️ Setup Instructions
Follow these steps to deploy the bot on your own server or local machine.

### Prerequisites
- Python 3.7+
- Pyrogram library (`pip install pyrogram`)
- Telegram API credentials:
  - **API ID** and **API Hash** from [my.telegram.org](https://my.telegram.org)
  - **Bot Token** from [BotFather](https://t.me/BotFather)

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ZenSlashBS/Auto-acceptor-
   cd Auto-acceptor-
   ```

2. **Install Dependencies**:
   ```bash
   pip install pyrogram
   ```

3. **Configure Credentials**:
   - Open the bot script (e.g., `bot.py`).
   - Replace the placeholder values for `BOT_TOKEN`, `API_ID`, and `API_HASH` with your own:
     ```python
     environ["BOT_TOKEN"] = "your-bot-token"
     environ["API_ID"] = "your-api-id"
     environ["API_HASH"] = "your-api-hash"
     ```

4. **Customize Links (Optional)**:
   - Update the inline button URLs in the welcome message to point to your desired Telegram channels or links.
   - Modify the greeting text in the `auto_approve` function if needed.

5. **Run the Bot**:
   ```bash
   python bot.py
   ```

6. **Add to Group/Channel**:
   - Add the bot to your Telegram group or channel via the “Add Me In Chat” or “Add Me In Channel” buttons.
   - Grant it admin rights to approve join requests.

---

## 📂 Code Overview
- **Framework**: Pyrogram, an async Python library for Telegram bots.
- **Key Handlers**:
  - `on_message`: Handles the `/start` command in private chats.
  - `on_chat_join_request`: Processes join requests for groups/channels.
- **Environment Variables**: Uses `os.environ` to store bot token and API credentials.
- **Inline Buttons**: Created with `InlineKeyboardButton` and `InlineKeyboardMarkup` for interactive menus.

---

## ⚠️ Limitations
- **No Persistent Storage**: Join request logs are printed to the console and not saved.
- **Single Language**: Welcome messages are in English only.
- **Manual Configuration**: API credentials and links must be hardcoded in the script.
- **No Error Handling**: Basic implementation without robust error management for failed approvals or messages.

---

## 🚀 Future Enhancements
- Add database support for logging join requests and user data.
- Implement multi-language support for welcome messages.
- Add admin commands to manage bot settings (e.g., toggle auto-approval).
- Include error handling for failed API calls or invalid links.
- Support custom welcome message templates via admin input.
- Add rate-limiting to prevent abuse.

---

## 🙋 Contributing
Contributions are welcome! To contribute:
1. Fork the repository: [https://github.com/ZenSlashBS/Auto-acceptor-](https://github.com/ZenSlashBS/Auto-acceptor-)
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

---

## 📞 Support
For help or suggestions:
- Open an issue on the GitHub repository: [https://github.com/ZenSlashBS/Auto-acceptor-](https://github.com/ZenSlashBS/Auto-acceptor-)
- Contact the owner via Telegram: [t.me/ZyncMaster](https://t.me/ZyncMaster)

---

## 🗿 About
This project is maintained by [ZenSlashBS](https://github.com/ZenSlashBS). It is not licensed, so please review the code and use it responsibly. The bot was created to simplify group/channel management on Telegram while promoting community engagement.

