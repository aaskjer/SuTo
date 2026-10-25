<p align="center"><img src="Assets/example.jpg" alt="Viewers type !suggestion in Twitch, YouTube and Kick chat; each suggestion appears as an embed in a Discord channel, with the viewer's name, platform and time" width="800"></p>

<p align="center"><b>SuTo — Suggestions To ...</b><br>Gather suggestions from your Twitch, YouTube or Kick chat in your Discord, Stoat or GameVox server. A Streamer.bot import.</p>

<p align="center">
  <img alt="Supported platforms: Twitch, YouTube, Kick" src="https://img.shields.io/badge/supported_platform-Twitch%2C_YouTube%2C_Kick-white">
  <img alt="Posts to: Discord, Stoat, GameVox" src="https://img.shields.io/badge/posts_to-Discord%2C_Stoat%2C_GameVox-5865f2">
  <img alt="tool: streamer.bot" src="https://img.shields.io/badge/tool-streamer.bot-0b73ff">
  <a href="https://opensource.org/licenses/MIT"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow"></a>
</p>
<p align="center">
  <img alt="Latest stable release" src="https://img.shields.io/github/v/release/aaskjer/SuTo?label=stable">
  <img alt="Total downloads" src="https://img.shields.io/github/downloads/aaskjer/SuTo/total">
  <img alt="GitHub stars" src="https://img.shields.io/github/stars/aaskjer/SuTo">
</p>

<p align="center"><b><a href="Manual.md">Manual</a></b> · <b><a href="Import-String.md">Import string</a></b> · <b><a href="https://github.com/aaskjer/SuTo/releases/latest">Download</a></b> · <b><a href="https://github.com/aaskjer/SuTo/issues">Report a problem</a></b></p>

---

# Overview

A viewer types `!suggestion Play the new farming game on Sunday` in chat. A moment later the idea sits in your server, with who sent it, where from and when, and the viewer gets a short confirmation in chat.

- **Three chats in:** Twitch, YouTube and Kick. The action works out by itself which platform a message came from.
- **Three servers out:** one action each for **Discord**, **Stoat** and **GameVox**. Turn on one, two or all three.
- **Two commands:** `!suggestion` and `!vorschlag`.
- **A tidy post:** the suggestion in an embed, coloured per platform, with the viewer's avatar, name, platform and the date and time underneath.
- **Discord forums:** a new forum post for every suggestion, or all of them in one thread.
- **Several channels at once:** put more than one webhook URL in, separated by commas.
- **Your wording:** the text of the post, the colours, the footer and the chat reply are all yours to change.
- **No webhook token in your logs:** if something goes wrong, the log says what and why, with the secret part of the URL masked.

---

# Install

1. Download **`SuggestionsTo.sb`** from the [latest release](https://github.com/aaskjer/SuTo/releases/latest), or copy the string from [Import-String.md](Import-String.md).
2. In Streamer.bot (1.0 or newer) click **Import** and drag the file in, or paste the string. Confirm the prompts.
3. Under **Settings → Commands**, group **[SuTo] Suggestions To**, enable the command for each server you post to:

   | Command | Posts to |
   |---|---|
   | `[SuTo] Suggestion to Discord` | Discord |
   | `[SuTo] Suggestion to Stoat` | Stoat |
   | `[SuTo] Suggestion to GameVox` | GameVox |

   All three answer to `!suggestion` and `!vorschlag`. With more than one enabled, a suggestion goes to every server, and the chat confirmation comes once per server.
4. Open the action (**[SuTo] ... Discord**, **... Stoat** or **... GameVox**) and replace the placeholder in the **Webhook: Send to Channel** group with your webhook URL:

   | Server | Argument | Where the URL comes from |
   |---|---|---|
   | Discord | `discordWebhookUrl` | Channel settings → Integrations → Webhooks → New Webhook → Copy Webhook URL |
   | Stoat | `stoatSuggestionWebhook` | The channel's webhook settings; the URL looks like `https://api.stoat.chat/webhooks/{id}/{token}` |
   | GameVox | `gameVoxWebhookUrl` | [GameVox Developer Portal](https://developers.gamevox.com/docs/webhooks) → your application → Webhooks → New Webhook. The URL is shown only once. |

That is it. Type `!suggestion test` in your chat to try it.

Everything else (text, colours, footer, time format, Discord forums) is optional and explained in the **[Manual](Manual.md)**.

---

# What lands where

| | Discord | Stoat | GameVox |
|---|---|---|---|
| Suggestion text | Embed, with Markdown | Embed, with Markdown | Embed, plain text (GameVox shows no Markdown) |
| Colour per platform | ✅ | ✅ | ✅ |
| Viewer's avatar | Twitch, Kick; YouTube when Streamer.bot passes one | Twitch, Kick | Twitch, Kick; YouTube when Streamer.bot passes one |
| Name and platform | Footer | Under the text | Footer |
| Date and time | Discord's own timestamp, in each reader's time zone | Your PC's time, in your format | Your PC's time, in your format |
| Forum posts and threads | ✅ | — | — |

The chat confirmation (`@user has made a suggestion!`) is sent on the platform the suggestion came from, and only when the post went through.

---

# Good to know

- **Webhooks are secrets.** Anyone with the URL can post to that channel. Do not show the action on stream, and create a new webhook if one leaks.
- **GameVox webhooks only reach cloud-hosted GameVox servers.** A self-hosted server answers with "not found".
- **Do not edit the "No Touchy!" group.** It looks up Kick avatars and runs the code.
- **Something not posting?** Streamer.bot's log (**Logs** tab) has a line starting with `[SuTo/Discord]`, `[SuTo/Stoat]` or `[SuTo/GameVox]` that says why. The [Manual](Manual.md#when-nothing-arrives) lists the usual ones.

---

Made by [aaskjer](https://www.twitch.tv/aaskjer) · [More Streamer.bot extensions](https://aaskjer.github.io) · [MIT License](LICENSE)

Not affiliated with Streamer.bot, Twitch, YouTube, Kick, Discord, Stoat or GameVox. All names and trademarks belong to their respective owners.
