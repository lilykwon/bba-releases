# Bba

> This repository only holds the installer and the user guide. **[Download the latest version](https://github.com/lilykwon/bba-releases/releases/latest)**
> [한국어](README.md)

**Your favorite plush, living on your Mac screen.** Turn one photo of your plush into your own desktop pet.
It wanders along the bottom of your screen, loves being petted, keeps you company while you focus, and chats with you through Claude or ChatGPT.

<p align="center"><img src="docs/demo.gif" alt="The pet walking around and answering a question" width="640"></p>

- **Make it from your plush:** pick the parts your plush has (ears, arms, legs, wings, tail) and the app writes the ChatGPT prompts and assembles the pet for you
- Hops, waddles on its legs, or floats around
- Follows your cursor with its eyes, blinks, and falls asleep after 2 minutes alone
- Click it to open a speech bubble and chat with **Claude** or **ChatGPT** (using your own account)
- Drag it anywhere. Let go and it drops down
- **Focus timer:** say "I'll focus for 30 minutes" and it puts on glasses and counts down beside you
- **Office helper:** "Start the countdown" or "Show my earnings" shows time until clock-out and what you've earned today
- **Pet it for hearts.** Drop it from too high and it gets dizzy or sulks
- **Drop a file or some text on it** to summarize, translate or proofread
- **"Meeting at 3pm"** and it reminds you on time
- Calm mode, quiet mode, four sizes, and Korean or English

<p align="center"><img src="docs/expressions.png" alt="Faces: neutral, happy, thinking, talking, surprised, pouty" width="720"></p>

---

## Contents

1. [Install](#install)
2. [Make your own character](#make-your-own-character)
3. [Connect Claude](#connect-claude) or [Connect ChatGPT](#connect-chatgpt) (optional)
4. [How to use](#how-to-use)
5. [FAQ](#faq)

---

## Install

1. Download **`Bba.dmg`** from [Releases](https://github.com/lilykwon/bba-releases/releases/latest). One file works on both Apple silicon and Intel Macs.
2. Open it and drag the **Bba** icon into your **Applications** folder.
3. Open **Bba** from Applications. Your pet drops in from the top of the screen.

> There's no Dock icon. **Right-click** the pet for the menu.

The app follows your Mac's language. To change it, right-click > **언어 / Language**.

**Connecting an AI is optional.** Petting, the focus timer and reminders ("remind me at 3pm") work right away. To chat, connect either [Claude](#connect-claude) or [ChatGPT](#connect-chatgpt).

---

## Make your own character

Right-click > **Character > Make a pet from my plush...** to open the wizard. All you need is a front photo of your plush and ChatGPT.

1. **Your plush:** name it, then pick its parts (ears, arms, legs, wings, tail) and how it moves (hop, waddle, float)
2. **Make images:** the app writes a ChatGPT prompt for each image. Click **Copy prompt** on each card and send it to ChatGPT with your photo
3. **Add images:** drag the images ChatGPT made into the boxes. Backgrounds are removed and the face sheet is cut automatically
4. **Done:** the app places the eyes, nose and limbs. Preview it and click **Finish** to swap your pet

> Your previous character is backed up automatically. Restore it any time from right-click > **Character**.

- **Rename...:** right-click > Character > Rename..., or tell your pet "your name is Mochi"
- **My characters:** every character you make or import is kept under right-click > Character > My characters. Switch any time; each keeps its own name, positions, relationship level and anniversaries. Focus records, reminders and your name are shared
- **Export character...:** saves your pet as a single `.petchar` file you can send to a friend
- **Import character...:** opens a `.petchar` file
- **Adjust positions...:** fine-tune eyes, limbs, size and motion with dots and sliders

---

## Connect Claude

Use this if you have a Claude Pro or Max subscription. Chats count toward your subscription with no extra cost.

**1. Open Terminal.** Press `Cmd + Space`, type "Terminal" and open it.

**2. Install Claude Code.** Paste this line into Terminal and press Enter.

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

> Install steps may change. If it doesn't work, see the [official Claude Code setup guide](https://docs.claude.com/en/docs/claude-code/setup).

**3. Log in.** When it's done, type:

```bash
claude
```

Log in with your Claude account in the browser. Once Terminal shows a welcome screen you're done, and you can close it.

**4. Check in the pet.** Click your pet and press **Check again**. When you see "Claude connected!", start chatting.

---

## Connect ChatGPT

Use this if you have a ChatGPT Plus, Pro, Business, Edu or Enterprise subscription.

**1. Open Terminal.** Press `Cmd + Space`, type "Terminal" and open it.

**2. Install Codex.**

```bash
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

> With Homebrew, `brew install --cask codex` also works. See the [official Codex repository](https://github.com/openai/codex) for details.

**3. Log in.**

```bash
codex
```

Choose **Sign in with ChatGPT** and log in in the browser.

**4. Check in the pet.** Click your pet and press **Check again**. "ChatGPT connected!" means you're set.

> If you installed both, switch any time from right-click > **Connection**.

<details>
<summary>Use a Claude API key instead of a subscription</summary>

Get an API key at [console.anthropic.com](https://console.anthropic.com), then right-click > **Connection > Claude API key** and paste it. The key is stored encrypted on your Mac only, and you pay per use.
</details>

---

## How to use

| Action | Result |
|---|---|
| Click | Open or close the speech bubble |
| Drag | Pick up and move (drops when you let go) |
| Right-click | Open the menu |
| Esc | Close the speech bubble |

### Focus timer

Just tell your pet: "I'm going to focus for 30 minutes", "Let's do a pomodoro". It puts on glasses and counts down beside you. You can also pick a time from right-click > **Focus timer**.

### Office helper

Tell your pet, no AI needed:

| Say | Your pet |
|---|---|
| "Start the countdown" | Shows the time until you clock out |
| "Show my earnings" | Shows what you've earned today, adding up every second |
| "Hide my salary" | Hides the amount (click the card to toggle) |
| "Turn off office" | Hides both cards |

Set your hours, lunch and annual salary in right-click > **Office helper > Settings...**. Pick your currency next to the salary. Your salary stays on your Mac and is never sent to the AI.

### Play with your pet

| Do this | Your pet |
|---|---|
| Move the mouse back and forth over its head | Smiles and floats hearts |
| Drop it from mid height or shake it | Gets dizzy |
| Drop it from very high | Sulks. **Pet it to make up** |
| Click three times quickly | Giggles, it tickles |

### Drag and drop

Drop a file or some text on your pet to **Summarize / Translate / Proofread / Ask about it**. Text files (txt, md, csv, json, code) and text dragged from the web work. PDFs, Word files and images don't yet.

### Reminders

"Remind me in 20 minutes to do laundry", "Meeting at 3pm", "Remind me tomorrow at 9am to take vitamins". See and cancel them from right-click.

### Handy

- **Call it over:** press **⌃⌥B** (Control + Option + B) and your pet comes to your cursor
- **Calm mode:** right-click > **Movement > Calm** or say "calm down". It stays near where you last put it and rests more. "Go wild" makes it lively, "act normal" goes back
- **Quiet mode:** "Be quiet" or right-click > Quiet mode. No chatter, just naps. Reminders still come. "You can talk now" ends it
- **Size:** right-click > Size, or say "shrink", "grow", "normal size"
- **Tricks:** "Jump!", "Spin", "Dance", "Good night". "Sing" works once you're best friends
- **Name:** say "Call me Lilly" and it will call you that

### AI task alerts

Right-click > **AI task alerts** to connect Claude Code or Codex. Your pet tells you when one is **waiting for your approval** (with a **Take me there** button that jumps to that Terminal, VS Code or the Claude app) and when a **task is done** (skipped if you're already looking at it). It only notifies and never approves anything for you. For Codex (0.124 or later), open `/hooks` once after connecting and trust the Bba hooks. The ChatGPT app and claude.ai chats don't expose these events yet.

### Growing closer

Petting, chatting, focusing together and just opening the app each day bring you closer: **Just met → Acquaintances → Friends → Best friends → Family**. It celebrates anniversaries (7 days, 30 days, 100 days, a year) and has a mood of the day.

---

## FAQ

<details>
<summary><b>Can I use it without an AI?</b></summary>

Yes. Reactions, the focus timer, reminders, greetings and break reminders all work without one. Chatting and summarizing dropped text need an AI connection.
</details>

<details>
<summary><b>It says I need to log in</b></summary>

Run `claude` (or `codex` for ChatGPT) in Terminal, log in, then talk to your pet again.
</details>

<details>
<summary><b>Where do my chats go?</b></summary>

The app has no server. Chats go straight to the Claude (Anthropic) or ChatGPT (OpenAI) account you logged into.
</details>

<details>
<summary><b>Can the pet touch my files or run commands?</b></summary>

No. It chats from its own empty folder. Claude runs with file and command tools turned off, and ChatGPT runs in read-only mode.
</details>

---

## License

Bba © 2026 WOX Studio. The default character "Bbagun" images may not be used or redistributed outside the app.
