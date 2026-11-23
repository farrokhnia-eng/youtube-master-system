# YouTube Master System

A skill for Claude. It helps you plan, make, publish, and improve YouTube videos.

- **Version:** 5.0 (November 23, 2026)
- **Install in:** Claude.ai or Claude Code
- **Content:** 22 text files. The skill has no code.

## Contents

- [What is this?](#what-is-this)
- [What can you do with it?](#what-can-you-do-with-it)
- [Built-in rules](#built-in-rules)
- [Install](#install)
- [Quick start](#quick-start)
- [How to use it](#how-to-use-it)
- [Commands](#commands)
- [Examples](#examples)
- [How it works](#how-it-works)
- [Files in this repo](#files-in-this-repo)
- [Limits](#limits)
- [Credits](#credits)

## What is this?

A skill is a folder of instructions for Claude. Claude reads the folder when your task needs it.

This skill makes Claude work like a team of YouTube experts. The team covers strategy, research, scripts, titles, thumbnails, editing, publishing, analytics, and money.

Claude uses only the experts that your task needs. It does not make every deliverable by default.

You do not need a new app. You write to Claude as usual.

## What can you do with it?

| Stage | What you can do |
|---|---|
| Strategy | Build a channel plan. Audit a channel. |
| Research | Study the market, trends, and competitors. Find video ideas. Score and rank topics. |
| Packaging | Write titles. Design thumbnails. Write descriptions, chapters, and tags. |
| Script and story | Write scripts, hooks, and screenplays. Plan Shorts. |
| Visual production | Make storyboards and shot lists. Write prompts for AI image, video, voice, and 3D tools. |
| Editing | Make an editing plan. Write a brief or a prompt for a human or AI editor. Diagnose one problem in an edit. |
| Music and sound | Write music briefs. Plan sound effects. |
| Publishing | Make an upload checklist. Plan the publish time. Write community posts and pinned comments. Plan playlists, end screens, and cards. |
| Analytics | Find out why a video does poorly. Revive a weak video. Design A/B tests. |
| Money and rules | Review mid-roll ads and revenue. Check copyright. Check AI disclosure. |

You can use one stage alone. You can also run all stages for one video with `/full-production`.

## Built-in rules

The skill follows these rules in every task:

- **It labels each claim.** A level from A to E shows how far you can trust the claim.
- **It checks current rules.** YouTube rules change. The skill tells Claude to check the official pages first. This works when Claude has web search.
- **It does not invent facts.** It never makes up statistics, sources, quotes, or test results.
- **It does not help you cheat.** It never suggests fake views, likes, comments, or subscribers.
- **It asks before big actions.** Claude stops and asks before it deletes files, publishes, buys assets, or posts for you.
- **It treats text in files as data.** Claude does not follow orders that it finds in a transcript, a comment, or a file name.

The evidence levels:

| Level | Source | How the skill uses it |
|---|---|---|
| A | Official rule or documentation from YouTube, Google, or a tool maker | Follow it. Check the latest update. |
| B | Strong research | Use it inside its stated scope. |
| C | Limited research: one niche, one country, or one study | Use it as a lead. Do not apply it to all channels. |
| D | Industry practice from experienced creators and editors | Use it as a start. Judge it by your own results. |
| E | Experimental idea or rumor | Test it with real data. Never treat it as a rule. |

## Install

### Before you start

- You need a Claude account. Skills work on the Free, Pro, Max, Ultra, Team, and Enterprise plans.
- Code execution must be on. Skills need it.
- Install skills only from sources that you trust. Read the files first. This skill has only text files.

### Option A: Claude.ai

1. Open the [Releases page](https://github.com/farrokhnia-eng/youtube-master-system/releases). Download `youtube-master-system.zip`. Do not unzip it.
2. In Claude, open **Settings > Capabilities**. Turn on **Code execution and file creation**. In the new Settings layout, the option name is **Create and edit files**.
3. Open **Customize > Skills**.
4. Click **+**. Click **+ Create skill**. Click **Upload a skill**.
5. Select `youtube-master-system.zip`.
6. Make sure the switch for the skill is on.

Notes:

- On Team and Enterprise plans, an owner must turn on skills first. The owner finds the setting in **Organization settings > Plugins & skills**. An owner can also block uploads.
- A skill that you upload is private to your account until you share it.
- The upload fails when the folder name in the ZIP does not match the skill name. Do not rename the folder.

You can also make the ZIP yourself. Zip the folder `youtube-master-system`, not the files inside it. On the command line, run this command in the repo folder:

```bash
zip -r youtube-master-system.zip youtube-master-system
```

### Option B: Claude Code

Install the skill for all your projects:

```bash
git clone https://github.com/farrokhnia-eng/youtube-master-system.git
mkdir -p ~/.claude/skills
cp -r youtube-master-system/youtube-master-system ~/.claude/skills/
```

The first name is the repo. The second name is the skill folder.

Install the skill for one project only. Run this command in the project folder:

```bash
mkdir -p .claude/skills
cp -r /path/to/youtube-master-system/youtube-master-system .claude/skills/
```

On Windows, use PowerShell:

```powershell
git clone https://github.com/farrokhnia-eng/youtube-master-system.git
New-Item -ItemType Directory -Force "$HOME\.claude\skills"
Copy-Item -Recurse youtube-master-system\youtube-master-system "$HOME\.claude\skills\"
```

You do not have git? Click **Code > Download ZIP** on the repo page. Unzip it. Copy the folder `youtube-master-system` that holds `SKILL.md` into your `skills` folder.

Then type `/skills` in Claude Code. Check that `youtube-master-system` is in the list. If the `skills` folder did not exist when you started Claude Code, restart Claude Code.

**Tip:** You can upload the skill in Claude.ai and sign in to Claude Code with the same account. Claude Code can then load the skill by sync. This needs Claude Code v2.1.273 or later. It does not work when you sign in with an API key.

### Check that it works

Start a new chat. Send this message:

```text
Use the youtube-master-system skill. I run a channel about home coffee. Give me video ideas.
```

Claude should give ten different ideas and explain the three best ones. If it does not, check the switch in **Customize > Skills**. Then ask again and keep the words "Use the youtube-master-system skill".

## Quick start

1. Install the skill.
2. Open a new chat.
3. Tell Claude about your channel in a few lines.
4. Ask for a task in plain words, or start with a command.
5. Read the result. Check the evidence labels.

Example of a first message:

```text
Use the youtube-master-system skill.
My channel is about home coffee. I publish one 8-minute video each week.
My viewers are beginners. The language is English. My goal is more subscribers.
Give me video ideas.
```

## How to use it

### Three ways to ask

**1. Use plain words.** Claude picks the skill by itself when your task is about YouTube.

```text
My last video got few views. What should I check?
```

**2. Start with a command.** A command is a short name for a task. The result is the same as with plain words.

```text
/title Write titles for a video about cold brew at home.
```

**3. Name the skill.** Use this way when Claude does not use the skill.

```text
Use the youtube-master-system skill. Plan a Short about latte art.
```

In Claude Code, start with the skill name. Then add your request or a command:

```text
/youtube-master-system /title Write titles for a video about cold brew at home.
```

### Tell Claude about your channel

The skill builds a channel profile before it makes a long-term plan. Give Claude these facts one time. Claude then uses them in the whole chat.

- Channel name and link
- Main topic and side topics
- Channel language and target countries
- Who your viewers are
- Video types: Shorts, long videos, Live, series
- Video length and how often you publish
- Budget, equipment, editing software, AI tools, and team size
- Goals, competitors, and limits (legal, creative, or technical)

Claude asks only for facts that it cannot work without. If a fact is missing, it states an assumption and continues.

### Language

Claude replies in the language that you use. The skill also reacts to Persian words such as `یوتیوب`, `تامبنیل`, and `ویدیو`.

The skill assumes a U.S.-focused English video for English-speaking viewers. If your video is for other viewers, say so at the start. For example:

```text
My channel language is Persian. My viewers speak Persian.
```

Claude writes prompts for outside AI tools in English. This is because most tools work best with English. Ask for another language if you need it.

### Use your real data

For `/analytics`, `/revive`, and `/ab-test`, paste your numbers from YouTube Studio. For example, paste impressions, click-through rate (CTR), retention, and traffic sources. The skill prefers your data to generic guesses. It never invents numbers.

### Edit, plan, or write a prompt?

For editing, say what you want:

- **Make the edit.** Claude makes a real video file only when its tools can edit and export video. If they cannot, Claude says so.
- **Make an editing plan.** You get a timeline, shot choices, and edit decisions.
- **Write an editor prompt.** You get a copy-ready prompt for a named human or AI editor.
- **Diagnose one problem.** Claude checks one issue in the timeline, sound, color, subtitles, or export.

Claude never says that an MP4 or SRT file exists unless the file exists and Claude checked it.

## Commands

A command is a short name for a task. Type it at the start of your message. The skill has 30 commands.

### Strategy and audit

| Command | What it does |
|---|---|
| `/channel` | Builds a channel strategy and a growth plan. |
| `/audit` | Audits a channel. |
| `/full-production` | Runs the full workflow for one video, from idea to analytics. |

### Research and ideas

| Command | What it does |
|---|---|
| `/research` | Researches the market and the audience. |
| `/trends` | Finds trends that fit your niche. |
| `/competitors` | Studies competitor channels. |
| `/ideas` | Makes video ideas. |
| `/select-topic` | Scores and ranks topics. |

### Titles, thumbnails, and metadata

| Command | What it does |
|---|---|
| `/title` | Writes and judges titles. |
| `/thumbnail` | Designs thumbnail concepts and prompts. |
| `/description` | Writes the video description. |
| `/transcript` | Analyzes a transcript. |
| `/seo` | Improves metadata: description, chapters, tags, and file names. |

### Scripts and Shorts

| Command | What it does |
|---|---|
| `/script` | Writes a video script with a hook and a plan to keep viewers watching. |
| `/screenplay` | Develops a fiction screenplay or a cinematic story. |
| `/shorts` | Plans and writes a Short. |

### Visual production

| Command | What it does |
|---|---|
| `/storyboard` | Makes a storyboard and a shot list. |
| `/visual-prompts` | Writes prompts for AI image, video, voice, and 3D tools. |

### Editing, music, and sound

| Command | What it does |
|---|---|
| `/editing` | Makes an editing plan or a brief. Makes the edit only when Claude has the tools. |
| `/music` | Writes music briefs, lyrics, and prompts for music tools. |
| `/sound` | Plans sound effects and audio treatment. |

### Publishing and community

| Command | What it does |
|---|---|
| `/community` | Plans Community posts and polls. |
| `/pinned-comment` | Writes pinned comments and replies. |
| `/publish` | Prepares the upload package. Also covers publish time, the first hour, playlists, end screens, and cards. |

### Analytics and tests

| Command | What it does |
|---|---|
| `/analytics` | Diagnoses how a video performs. |
| `/revive` | Diagnoses a weak video and plans fixes. |
| `/ab-test` | Designs an experiment. |

### Money and rules

| Command | What it does |
|---|---|
| `/monetization` | Reviews revenue options and mid-roll ads. |
| `/copyright` | Reviews rights and licensing risks. |
| `/ai-compliance` | Reviews AI and synthetic-content disclosure. |

### Tasks without a command

Use plain words for these tasks:

- Audience psychology and how the recommendation system works.
- A prompt for any outside AI tool: image, video, voice, music, workflow, or research agent.
- A task for an agent that edits files, runs scripts, renders, or uploads.
- A check of a rule of thumb, or a source.
- A final check before delivery.

## Examples

Each example shows what you write and what you get. Replace the topic with your own.

### 1. Find video ideas

```text
/ideas My channel is about home coffee. My viewers are beginners aged 20 to 35. Give me video ideas.
```

You get ten different ideas. Each idea lists the topic, the viewer need, the core promise, the unique angle, and the risks. Claude explains the three strongest ideas.

### 2. Pick the best topic

```text
/select-topic Rank these ideas: (1) cold brew in 5 minutes, (2) 10 coffee mistakes, (3) I tried 20 grinders.
```

You get a score from 0 to 10 for each part: audience fit, demand evidence, packaging, originality, story, production, and strategy. The score helps you decide. It does not forecast views.

### 3. Write titles

```text
/title Write titles for my video "Cold brew in 5 minutes". My viewers are beginners.
```

You get twelve different titles in several styles. Claude picks the three strongest and adds three to five alternatives. It explains the promise, the viewer, the link to the thumbnail, and the risk of a wrong guess.

### 4. Design thumbnails

```text
/thumbnail Give me thumbnail ideas for "Cold brew in 5 minutes".
```

You get three different concepts. One uses a proven look from your niche. One is a new creative idea. One uses the look of your own channel. The skill asks for thumbnails that are easy to read on a phone and true to the video.

### 5. Write a script

```text
/script Write a script for an 8-minute video about 5 cold brew mistakes. The tone is friendly and funny.
```

You get a script with a hook, a clear structure, and a payoff. The skill uses story methods such as open curiosity loops and hook, promise, and payoff.

### 6. Get an editing brief

```text
/editing Write a copy-ready brief for my editor. The video is a funny, cinematic 10-minute video about cold brew.
```

You get a brief that covers story, pacing, humor, color, audio, subtitles, and technical settings. Give it to a human editor or an AI editor.

### 7. Prepare the upload

```text
/publish Prepare the upload package for my cold brew video.
```

You get a checklist for the title, description, chapters, tags, links, playlist, pinned comment, and upload settings. Claude does not upload anything without your approval.

### 8. Find out why a video does poorly

```text
/analytics My video has a high CTR but low retention. Here are my numbers from YouTube Studio: ...
```

You get five parts: observed data, a possible explanation, missing data, a proposed experiment, and a decision rule. For high CTR with low retention, the skill checks two causes. The promise and the video may not match, or the opening may be weak.

### 9. Plan an A/B test

```text
/ab-test Design a thumbnail test for my last video.
```

You get a test plan with these parts:

- a hypothesis and one variable
- a control and the test variants
- a main metric and a second metric
- notes on sample size
- an observation period and a decision

The skill tells you to use the YouTube Test & Compare tool when it is available. Check the current rules for that tool first.

### 10. Check AI disclosure

```text
/ai-compliance My video uses an AI voice and AI-made B-roll. What must I check before I publish?
```

You get a review of the YouTube rules for altered or synthetic content. The skill checks the official YouTube pages first when Claude has web search. It marks as unverified anything that it cannot check.

### 11. Run the full workflow

```text
/full-production Take my cold brew video from idea to upload package. Ask me before any big step.
```

Claude goes through eight phases: audience, topic and packaging, script, visuals, editing, music and sound, publishing, and analytics. A real project can merge phases or change their order. Claude stops and asks before big actions, such as publishing.

### More prompts to try

```text
/channel Plan a 6-month growth strategy for my cooking channel.
/audit Audit my channel. Here are my last 20 videos: ...
/research Who watches home coffee videos? What do they need?
/trends Find current trends in home coffee.
/competitors Compare my channel with these three channels: ...
/description Write a description for my cold brew video.
/transcript Here is my transcript. Find the weak parts: ...
/seo Improve the chapters and tags for this video.
/screenplay Write a short comedy screenplay about a broken grinder.
/shorts Turn my cold brew video into a Short.
/storyboard Make a shot list for the first 60 seconds.
/visual-prompts Write AI image prompts for scene 3.
/music Write a music brief for a calm intro.
/sound Plan sound effects for the cold brew steps.
/community Write a poll about my next video.
/pinned-comment Write a pinned comment for my new video.
/revive My video from last month stopped getting views. Help me find out why.
/monetization Is a mid-roll ad a good idea for my 8-minute videos?
/copyright Can I use this song in my video?
```

## How it works

1. You send a message about YouTube.
2. Claude reads the skill name and description. It decides that the skill fits your task.
3. Claude loads `SKILL.md`. This file holds the rules for every task.
4. Claude finds your task in the routing table.
5. Claude reads only the reference file for that task. This keeps the context small.
6. Claude applies the core rules, such as the evidence levels.
7. Claude checks the current YouTube rules when your task depends on them.
8. Before Claude gives you a plan or a production package, it runs the quality checklist.

When goals conflict, the skill decides in this order:

1. Law, safety, rights, and privacy.
2. Your explicit requirements and limits.
3. Accuracy and source quality.
4. Real value for the viewer.
5. Creative quality.
6. Fit with the channel.
7. Production feasibility.
8. Cost and time.
9. Style and polish.

When tactics conflict, the skill decides in this order: official requirements, your channel's reliable data, strong research, limited research, industry practice, and untested ideas.

## Files in this repo

```text
youtube-master-system/                  The repo
├── README.md                           This page
└── youtube-master-system/              The skill folder. Do not rename it.
    ├── SKILL.md                        The main rules and the routing table
    └── references/                     21 detail files. Claude reads a file only when it needs it.
```

The reference files:

| File | What it holds |
|---|---|
| `framework-core.md` | Roles, priority order, evidence levels A to E, channel profile, modes, commands, and the eight phases |
| `quality-and-outputs.md` | Final checklist, conflict table, and output templates |
| `research-and-topics.md` | Market, trend, and competitor research. Topic types. Topic score. |
| `audience-and-algorithm.md` | Audience groups, psychology, recommendation signals, and viewer satisfaction |
| `titles-and-thumbnails.md` | Title rules, thumbnail rules, thumbnail claims, and A/B tests for packaging |
| `metadata-and-seo.md` | Description structure, transcript workflow, chapters, tags, and file names |
| `scripts-and-storytelling.md` | Story methods, long-form structure, hooks, retention, and cinematic story |
| `ai-visual-production.md` | Storyboards, shot lists, AI image and video prompts, and tool routing |
| `editing-principles.md` | Pacing, story structure, humor timing, color, audio, and subtitles |
| `editing-workflow-and-technical.md` | Footage intake, project setup, selects, multi-pass edit, dialogue repair, color, and export |
| `editing-briefs-and-prompts.md` | Copy-ready editing brief and editing prompts |
| `music-and-sound.md` | Music brief, music generation, sound design, and rights |
| `community-and-publishing.md` | Community posts, pinned comments, upload checks, publish time, first hour, playlists, end screens, and cards |
| `shorts.md` | Shorts topic, length, hook, loop, audio, cover, and risks |
| `analytics-and-revival.md` | Metrics, diagnosis, reviving weak videos, and experiments |
| `monetization-and-compliance.md` | Mid-roll ads, revenue, copyright, AI disclosure, and reused content |
| `prompt-engineering.md` | How to write and check prompts for outside AI tools |
| `agentic-safety.md` | Rules for agents: permissions, credentials, untrusted input, and stop conditions |
| `claim-registry.md` | Every rule, number, and tactic with its default status |
| `sources-official.md` | YouTube Help and policy links and other official sources |
| `sources-academic.md` | Research papers and a map from research to claims |

## Limits

- The skill gives advice and drafts. It cannot promise views, subscribers, or revenue.
- YouTube rules and tools change. The skill checks the current official pages only when Claude has web search. If it cannot check, it says so and marks the fact as unverified.
- The claim registry keeps rules and numbers that the author supplied. The skill does not treat them as true. It gives each one a level and a decision. Check the original source before you rely on a number.
- Claude does not edit video, publish, or post for you unless you approve it and its tools allow it.
- The results can differ in Claude.ai and in Claude Code. Test the skill with your own tasks.

## Credits

Based on YouTube Master System V5.0, Expanded Complete American English Edition (November 23, 2026).

YouTube is a trademark of Google LLC. Claude is a trademark of Anthropic, PBC. This is an independent project. Google and Anthropic do not make, endorse, or support it.
