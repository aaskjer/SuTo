<p align="center">
  <img src="Assets/example.jpg" alt="Viewers type !suggestion in Twitch, YouTube and Kick chat; each suggestion appears as an embed in a Discord channel, with the viewer's name, platform and time" width="800">
</p>

<h1 align="center">SuTo — Suggestions To</h1>

<p align="center">
  <b>Suggestions from your chat, straight into your server.</b><br>
  From Twitch, YouTube and Kick to Discord, Stoat or GameVox.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platforms-Twitch%20%7C%20YouTube%20%7C%20Kick-9146FF" alt="Platforms">
  <img src="https://img.shields.io/badge/webhooks-Discord%20%7C%20Stoat%20%7C%20GameVox-5865F2" alt="Webhooks">
  <img src="https://img.shields.io/badge/tool-streamer.bot-0b73ff" alt="Streamer.bot">
  <br>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow" alt="License: MIT"></a>
  <img src="https://img.shields.io/github/v/release/aaskjer/SuTo?label=stable" alt="Release">
  <img src="https://img.shields.io/github/downloads/aaskjer/SuTo/total" alt="Downloads">
  <img src="https://img.shields.io/github/stars/aaskjer/SuTo" alt="Stars">
</p>

<p align="center">
  <a href="https://github.com/aaskjer/SuTo/releases/latest"><b>Download</b></a> &nbsp;·&nbsp;
  <a href="Setup-Guide.md"><b>Setup Guide</b></a> &nbsp;·&nbsp;
  <a href="Import-String.md"><b>Import String</b></a> &nbsp;·&nbsp;
  <a href="https://github.com/aaskjer/SuTo/issues"><b>Report a problem</b></a>
</p>

---

## 📖 Overview

SuTo is an import for Streamer.bot. A viewer types `!suggestion Play the new farming game on Sunday` in
chat, and a moment later the idea sits in your server: who sent it, where from and when. The viewer gets a
short confirmation in chat. `!vorschlag` works the same way.

Everything is set in one window: which servers you post to, their webhooks, the look of the post and the answer
in chat.

## ✨ Highlights

- 💬 **Three chats in.** Twitch, YouTube and Kick. The action works out by itself which platform a message
  came from.
- 📬 **Three servers out.** Discord, Stoat and GameVox. Switch on one, two or all three.
- ⚙️ **A settings window.** A page per server, with a button that sends a test suggestion and says whether it
  arrived. Your settings survive every update.
- 🎨 **A tidy post.** An embed coloured per platform, with the viewer's avatar, name, platform, date and time.
  Discord shows the time in each reader's own time zone.
- 🧵 **Discord forums.** A new forum post for every suggestion, or all of them in one thread.
- 📡 **Several channels at once.** Enter more than one webhook URL, separated by commas.
- ✏️ **Your wording.** The text of the post, the colours, the footer and the chat reply are all yours to
  change.
- ✅ **Confirmed only when it arrived.** The chat reply goes out on the platform the suggestion came from, once
  per suggestion, and only when the post went through.
- 🔒 **No webhook token in your logs.** When something fails, the log says what and why, with the secret part
  of the URL masked.

<p align="center">
  <img src="Assets/screenshots/discord-dark.png" alt="The Discord page of SuTo's settings window: the server is switched on, the webhook URL shows as dots, and the test suggestion arrived" width="720">
</p>

---

## Credits

- **Author:** [aaskjer on Twitch](https://twitch.tv/aaskjer) · [aaskjer.github.io](https://aaskjer.github.io/)
- **Built for:** [Streamer.bot](https://streamer.bot) by [nate1280](https://www.patreon.com/c/nate1280/home)
- **Settings window:** [UIFramework for streamer.bot](https://github.com/aaskjer/UIFramework-Streamer.bot)
- **Thanks:** YOU ♡

Not affiliated with Streamer.bot, Twitch, YouTube, Kick, Discord, Stoat or GameVox. All names and trademarks
belong to their respective owners.
