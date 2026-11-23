# Editing Workflow and Technical Delivery (Part 2)

> From YouTube Master System V5.0, sections 31 (31.15 to 31.32), 42. Original section numbers are kept, so cross-references still work. The section map is in SKILL.md.

## Contents

  - 31.15 Source-Footage Intake and Technical Audit
  - 31.16 Project Structure, Media Management, and Backup
  - 31.17 Project Setup and Timeline Configuration
  - 31.18 Media Organization and Selects Workflow
  - 31.19 The Multi-Pass Editing Process
  - 31.20 Story Clarity, Continuity, and Visual Grammar
  - 31.21 Gaming and Screen-Recording Editing Rules
  - 31.22 Comedy Construction and Timing Map
  - 31.23 Cinematic Look and Shot Treatment
  - 31.24 Dialogue Editing and Audio Repair
  - 31.25 Music and Sound-Effects Editing
  - 31.26 Color Management and Finishing
  - 31.27 Graphics, Captions, and Accessibility
  - 31.28 Titles, Transitions, and On-Screen Information
  - 31.29 Export and Delivery Specifications
  - 31.30 Export Verification and Delivery Handoff
  - 31.31 Actual Editing vs. Editing Advice
  - 31.32 Tool-Specific Editing Adaptation
- 42. APPENDIX A — EXPANDED POST-PRODUCTION WORKFLOW
  - A1. End-to-End Editing Pipeline
  - A2. Editing Decision Log
  - A3. Editorial Priorities
  - A4. Review Types

---

## 31.15 Source-Footage Intake and Technical Audit

Before editing, inspect the actual source files. Do not infer their contents from filenames, folder names, thumbnails, or the user's short description.

Create a source inventory with:

- File name and path;
- Duration;
- Resolution and aspect ratio;
- Frame rate and whether it is constant or variable;
- Video codec and container;
- Audio codec, sample rate, channel count, and bit depth when available;
- Recording device or source, if known;
- Creation date or recording order, if available;
- Corruption, missing frames, dropped frames, clipping, or sync issues;
- Whether the file contains dialogue, game audio, music, ambience, or multiple tracks;
- Rights or license information for third-party assets.

Check whether all required footage and audio files are present. Identify duplicate files, missing segments, offline media, unsupported codecs, and unusually large files.

Never overwrite or destructively alter the original source media. Work from copies, proxies, or a non-destructive project unless the user explicitly authorizes another method. Preserve a recoverable source backup before any destructive operation.

If a recording uses variable frame rate (VFR), test for audio drift, frame pacing issues, and sync instability. Convert or transcode only when required by the selected editor or delivery workflow. Preserve the source's intended timing and do not silently change the frame rate.

If footage has clipped audio, crushed highlights, blocked shadows, heavy motion blur, or missing frames, document the limitation before promising a repair.

## 31.16 Project Structure, Media Management, and Backup

Use a clean, portable project structure. Adapt names to the user's operating system and editor, but use a predictable arrangement such as:

```text
PROJECT_NAME/
  00_ADMIN/
  01_ORIGINALS_READ_ONLY/
  02_AUDIO_RECORDINGS/
  03_MUSIC_LICENSES_AND_SFX/
  04_GRAPHICS_AND_FONTS/
  05_PROXIES_AND_CACHE/
  06_EDIT_PROJECT/
  07_CAPTIONS_AND_TRANSCRIPTS/
  08_EXPORTS/
  09_DELIVERY_AND_ARCHIVE/
```

Keep original media read-only where practical. Use proxies or optimized media when the source resolution, codec, or hardware makes editing slow. Proxies must remain linked to the correct camera originals and must not replace the final-resolution export.

Use clear, versioned names such as:

- `ProjectName_Edit_v01`
- `ProjectName_RoughCut_v02`
- `ProjectName_PictureLock_v03`
- `ProjectName_Final_1080p`
- `ProjectName_Final_4K`
- `ProjectName_English.srt`

Do not use ambiguous names such as `final_final2_reallyfinal.mp4`.

Keep project files, fonts, graphics, linked audio, LUTs, and other dependencies together or document their locations. If an editable project is a required deliverable, verify that it opens and that media is online on the target machine or in the agreed handoff environment.

## 31.17 Project Setup and Timeline Configuration

Before building the timeline, select project settings based on the source footage and delivery target:

- Sequence resolution;
- Frame rate;
- Aspect ratio;
- Progressive or interlaced handling;
- Color-management mode;
- Working color space;
- Audio sample rate;
- Channel layout;
- Proxy and cache settings.

For a conventional long-form YouTube master, 16:9 is the normal starting point. Do not force 16:9 when the source or creative brief requires another aspect ratio.

Match the timeline frame rate to the principal source footage and intended delivery. Do not convert 24 fps footage to 60 fps merely because 60 fps appears more advanced. Do not mix frame rates without checking motion cadence, frame duplication, frame blending, or optical-flow artifacts.

Use the source's native resolution when practical. Upscale only when there is a justified production reason; do not claim that upscaling creates genuine captured detail.

## 31.18 Media Organization and Selects Workflow

Organize footage into bins or folders according to the project:

- Main footage;
- Camera A / Camera B;
- Facecam;
- Screen recordings or gameplay;
- Voice-over;
- Production audio;
- Music;
- Sound effects;
- B-roll;
- Graphics;
- Captions;
- Exports.

Review the footage and create selects before building a detailed edit. Log useful moments with timecodes and short descriptions. Mark:

- Strong opening moments;
- Important story beats;
- Funny moments;
- Reactions;
- Useful explanations;
- Visual evidence;
- Turning points;
- Climax and payoff;
- Continuity references;
- Sections that may be removed.

When the source is long, build a string-out or selects timeline. A paper edit or beat sheet may be used to plan the narrative before fine editing.

Never invent timestamps. Timecodes must come from inspected media or a reliable transcript aligned to the actual source.

## 31.19 The Multi-Pass Editing Process

Use a staged workflow rather than trying to perfect every shot at once:

**Pass 1 — Narrative Assembly:** Put the essential events in a coherent order. Focus on meaning, cause and effect, and the viewer's understanding.

**Pass 2 — Story and Pacing Cut:** Remove repetition, dead time, weak transitions, and irrelevant material. Preserve necessary context and emotional beats.

**Pass 3 — Comedy and Performance Cut:** Refine setup, anticipation, pause, reaction, punchline, callback, and timing. Do not cut away from a strong reaction too early.

**Pass 4 — Visual Continuity Cut:** Match action, screen direction, eyelines, positions, gameplay state, props, graphics, and scene geography where applicable.

**Pass 5 — Sound Edit:** Clean dialogue, synchronize sources, shape ambience, add justified effects, and balance music.

**Pass 6 — Color and Graphics:** Match footage, apply the intended look, and add titles, labels, captions, and supporting graphics.

**Pass 7 — Fine Polish:** Refine transitions, timing, audio fades, caption positions, and small visual issues.

**Pass 8 — Picture Lock and QC:** Stop making creative changes unless a real issue is found. Export, inspect, and verify the delivered file.

A rough cut is allowed to be structurally complete but visually unfinished. A fine cut should be close to final timing and storytelling. Do not claim picture lock before the narrative and timing are stable.

## 31.20 Story Clarity, Continuity, and Visual Grammar

Each cut should preserve or intentionally change the viewer's understanding of:

- Who is present;
- Where the action takes place;
- What is happening;
- Why it matters;
- What changed since the previous shot;
- What the viewer should notice next.

Use continuity tools where appropriate:

- Match on action;
- Eyeline match;
- Screen direction;
- Establishing shots;
- Reaction shots;
- Insert shots;
- Cutaways;
- Motivated camera movement;
- Consistent geography;
- Consistent game state or interface state.

Use jump cuts intentionally. If a jump cut makes the subject, action, or timeline confusing, use a cutaway, reframing, room tone, visual bridge, or a different take where available.

Do not manufacture reactions, outcomes, or actions that did not occur in the supplied footage. Do not splice statements in a way that changes their meaning.

## 31.21 Gaming and Screen-Recording Editing Rules

When the source is gameplay or a screen recording, preserve the information viewers need to understand the action:

- Relevant gameplay state;
- Player objective;
- Important HUD or interface elements;
- Map or location context;
- Score, timer, inventory, or other meaningful UI;
- Cause and effect of key actions;
- In-game audio that contributes to the experience;
- Commentary and facecam synchronization, if present.

Do not crop away essential HUD information. Zoom into a gameplay detail only when the enlarged view remains understandable. Avoid excessive overlays that obscure the game.

Loading screens, menus, respawns, queues, and repetitive gameplay may be shortened, but keep them when they create context, anticipation, a running joke, or an important transition.

Preserve the distinction between game audio, microphone audio, voice chat, and added sound effects. Control their relative levels separately when the source files permit it.

Check game soundtrack and third-party music licensing where relevant. Do not assume that every in-game track is cleared for monetized YouTube use.

## 31.22 Comedy Construction and Timing Map

When the video is intended to be funny, map comedy beats deliberately:

1. **Setup:** Give the viewer enough information to understand the situation.
2. **Expectation:** Establish what the viewer thinks will happen.
3. **Misdirection or Escalation:** Change the expectation or raise the stakes.
4. **Punchline / Payoff:** Deliver the funny event or line.
5. **Reaction:** Allow the response to register.
6. **Button or Callback:** Add a short final beat only when it strengthens the joke.

Not every joke needs all six stages. Do not explain a joke after it has landed. Do not stack multiple sound effects on a punchline unless the combination is intentionally part of the humor.

Use reaction shots and awkward pauses when they make the moment funnier. Preserve a brief silence when it is the joke. Avoid adding a meme that competes with the actual event.

For recurring jokes, maintain consistency and vary the payoff. Do not repeat the same visual gag so often that it loses impact.

## 31.23 Cinematic Look and Shot Treatment

Build the cinematic feel through the source material and the editorial treatment:

- Shot scale and shot selection;
- Foreground, midground, and background separation;
- Composition and negative space;
- Motivated movement;
- Depth and visual direction;
- Lens perspective when real camera footage supports it;
- Matching exposure and color;
- Sound perspective and ambience;
- Deliberate transitions;
- Narrative and emotional progression.

Do not add fake camera shake, artificial lens blur, heavy film grain, fake lens flares, black bars, or slow motion by default. Use these only when they support the defined aesthetic and do not damage the footage.

If the content is gameplay or screen capture, do not pretend that it was filmed with a physical cinema camera. Use cinematic composition, timing, sound, and graphics appropriate to the medium.

## 31.24 Dialogue Editing and Audio Repair

Treat audio as separate components whenever possible:

- Main dialogue or commentary;
- Voice-over;
- Facecam microphone;
- Game or system audio;
- Production ambience;
- Music;
- Sound effects;
- Room tone.

Recommended editing order:

1. Synchronize recordings;
2. Choose the cleanest source;
3. Remove avoidable handling noise and unwanted interruptions;
4. Reduce steady background noise conservatively;
5. Correct tonal problems with EQ where needed;
6. Control dynamic range with compression only when needed;
7. Use de-essing only when sibilance is distracting;
8. Add fades and room tone to avoid abrupt edits;
9. Automate or duck music under speech;
10. Check phase and mono compatibility;
11. Measure integrated loudness and true peak;
12. Listen to the final mix on headphones, speakers, and a phone where practical.

Do not apply aggressive noise reduction that creates metallic or watery artifacts. Do not use one fixed EQ or compressor preset for every voice. If multiple microphones are combined, check phase alignment and comb filtering.

Clipped or missing audio detail may be unrecoverable. Restoration can reduce the problem but cannot guarantee reconstruction of the original waveform.

## 31.25 Music and Sound-Effects Editing

Music and sound effects should follow the story, not dictate it.

For each music cue, define:

- Entry point;
- Exit point;
- Narrative function;
- Emotional direction;
- Intensity;
- Relationship to dialogue;
- Transition into the next cue.

Use music automation or sidechain-style ducking where appropriate. Avoid sudden music changes unless the change itself is a deliberate joke or narrative event.

Sound-effect categories may include:

- Foley;
- UI and interface sounds;
- Whooshes;
- Impacts;
- Risers;
- Hits;
- Transitions;
- Ambience;
- Game-specific effects;
- Comedic stingers.

Do not use a sound effect merely because a transition exists. Respect source perspective, distance, room size, and scene continuity.

Maintain a music and SFX cue sheet with source, license, and intended use for third-party assets.

## 31.26 Color Management and Finishing

Before grading, identify whether the source and target are SDR or HDR and determine the correct color-management path.

For ordinary SDR web delivery, use the appropriate Rec.709 / BT.709 workflow and metadata. For HDR, retain an HDR workflow only when the footage, project, monitoring, and delivery all support it. Do not convert HDR to SDR with a blind LUT or tag SDR footage as HDR.

Use waveform, RGB parade, vectorscope, and reference viewing where available. Do not rely only on a single uncalibrated monitor or a visual preset.

Finishing priorities:

- Consistent exposure;
- Neutral white balance where intended;
- Natural skin tones;
- Controlled highlights;
- Retained shadow detail;
- Consistent saturation;
- Shot-to-shot matching;
- Correct color-space tags and export metadata.

Avoid over-sharpening, chroma noise, crushed blacks, clipped highlights, banding, posterization, and unnecessary denoising.

## 31.27 Graphics, Captions, and Accessibility

Every graphic should have a clear role: identify, explain, emphasize, compare, or guide attention.

Keep typography consistent with the channel's identity. Use readable type sizes, adequate contrast, clear hierarchy, and consistent placement. Do not cover faces, subtitles, important gameplay UI, or information the viewer needs.

Distinguish these outputs:

- **Closed captions / subtitle file:** A separate timed text track, such as SRT;
- **Burned-in subtitles:** Text permanently embedded in the video;
- **Emphasis captions:** Selective words or short phrases used as visual design;
- **Transcript:** Full text record of spoken content;
- **Translated subtitles:** A localized timed text version, not a dub.

For SRT delivery, use valid sequential cue numbers, `HH:MM:SS,mmm --> HH:MM:SS,mmm` timestamps, UTF-8 text, and a verified final-video timebase. Keep lines concise and normally no more than two lines where practical. Check punctuation, speaker labels, line breaks, timing, and readability.

For English localization, translate meaning and tone rather than word-for-word phrasing. Preserve important jokes, proper nouns, names, and factual details. Do not invent speech that is not audible.

## 31.28 Titles, Transitions, and On-Screen Information

Use opening titles, lower thirds, labels, chapter cards, and end-screen graphics only when they improve orientation or branding.

Use transitions that match the visual and narrative relationship between shots:

- Straight cut;
- J-cut;
- L-cut;
- Match cut;
- Dissolve;
- Wipe;
- Whip pan;
- Dip to color;
- Sound bridge.

A straight cut is often the cleanest choice. Do not use a transition pack simply to make the edit appear elaborate.

Leave safe visual space and sufficient timing for YouTube end-screen elements when the end screen is part of the plan. Do not cover essential content with end-screen placeholders.

## 31.29 Export and Delivery Specifications

Choose export settings from the actual source and current platform guidance. Do not invent a universal bitrate or force upscaling.

A standard YouTube long-form master commonly uses:

- Container: MP4;
- Video: H.264;
- Scan: progressive;
- Frame rate: match the recorded/source frame rate;
- Aspect ratio: usually 16:9 for standard landscape content;
- SDR color space: BT.709;
- Audio: AAC-LC or another currently supported recommended codec;
- Audio sample rate: 48 kHz;
- Audio layout: stereo unless the project requires another supported layout.

Use YouTube's current upload guide for recommended bitrate ranges. The following values are the SDR/HDR upload recommendations shown in the official guide reviewed for this version. Recheck the live page before export because guidance can change.

### Recommended Video Bitrates (Reference Table)

| Resolution | SDR: Standard Frame Rate (24/25/30 fps) | SDR: High Frame Rate (48/50/60 fps) | HDR: Standard Frame Rate (24/25/30 fps) | HDR: High Frame Rate (48/50/60 fps) |
|---|---:|---:|---:|---:|
| 8K | 80–160 Mbps | 120–240 Mbps | 100–200 Mbps | 150–300 Mbps |
| 2160p (4K) | 35–45 Mbps | 53–68 Mbps | 44–56 Mbps | 66–85 Mbps |
| 1440p | 16 Mbps | 24 Mbps | 20 Mbps | 30 Mbps |
| 1080p | 8 Mbps | 12 Mbps | 10 Mbps | 15 Mbps |
| 720p | 5 Mbps | 7.5 Mbps | 6.5 Mbps | 9.5 Mbps |
| 480p | 2.5 Mbps | Not specified in the current table | Not supported | Not supported |
| 360p | 1 Mbps | 1.5 Mbps | Not supported | Not supported |

These are recommended upload bitrates, not mandatory minimums or guarantees of quality. Select the rate based on the actual source, frame rate, codec, motion complexity, and desired file size. Avoid unnecessary multiple re-encodes. Use a high-quality mezzanine master during post-production when needed, then create the delivery encode.

### Audio Upload Reference

The official upload guide lists recommended audio bitrates of 128 kbps for mono, 384 kbps for stereo, and 512 kbps for 5.1 audio. Use AAC-LC or another currently supported recommended codec and a 48 kHz sample rate where appropriate. The upload guide's table is a platform encoding recommendation; it is not a loudness target.

### Additional Encoding Notes

For a conventional H.264 MP4 delivery, use progressive scan, appropriate H.264 profile/settings, variable bitrate encoding, and fast-start metadata when supported by the export workflow. Follow the current official guide for detailed container, codec, GOP, and color metadata settings. Match the upload frame rate to the recorded source frame rate. For SDR, use correct BT.709 color metadata. Do not set HDR tags unless the project is actually mastered as HDR.

Do not use 60 fps if the source was recorded at 30 fps unless there is a justified conversion process. Do not change the source cadence casually.

### Deliverable Types

Specify exactly which outputs are required:

1. Final rendered MP4;
2. Editable project file;
3. Complete SRT subtitle file;
4. Transcript;
5. Separate translated SRT;
6. Audio-only master or stems;
7. Thumbnail or graphic assets;
8. Source and license manifest;
9. Separate vertical Shorts, only when requested;
10. Project archive with linked assets, only when requested.

Do not create extra versions that the user did not request.

## 31.30 Export Verification and Delivery Handoff

A successful export is not verified merely because the editor displays a progress bar at 100%.

Verify the actual exported files:

- File exists and is not zero bytes;
- File opens in a standard media player;
- Duration matches the intended edit;
- Resolution and frame rate are correct;
- Audio is present and synchronized;
- No accidental black frames or missing sections;
- No unintended silence or audio dropouts;
- No clipping or severe distortion;
- Captions match the exported cut;
- The final seconds and end screen are correct;
- The exported file plays through to the end.

Where practical, watch the entire export once. If full playback review is not possible, inspect the beginning, middle, end, all transitions, and known high-risk points and disclose the incomplete QC.

The handoff should state:

- Files delivered;
- Format and technical settings;
- Runtime;
- Subtitle languages;
- Project-file status;
- Assets or fonts that must accompany the project;
- License information available;
- Known limitations;
- QC checks completed and not completed.

## 31.31 Actual Editing vs. Editing Advice

Identify which outcome the user wants:

A. **Execute the edit:** Produce the actual final video file from supplied footage, if the available tool can perform and export it.

B. **Create an editing plan:** Analyze footage and provide a timeline, shot selections, and edit decisions, without claiming to export a video.

C. **Write an editor prompt:** Produce a copy-ready prompt for a named AI editor or human editor.

D. **Troubleshoot an existing edit:** Diagnose a specific problem in the timeline, sound, color, subtitles, or export.

If the user asks for an actual edited video and the tool supports editing/export, do not return only a plan or checklist. Perform the edit and deliver the rendered file.

If the tool cannot render or export, state that limitation clearly. Do not disguise an editing plan as a finished video. Do not claim that an MP4 or SRT was produced unless the file exists and has been checked.

## 31.32 Tool-Specific Editing Adaptation

Do not assume every AI editor has the same capabilities. Before writing a tool-specific prompt, identify:

- Exact tool and interface (web app, desktop app, API, plugin, or agent);
- Current model or editing mode, if relevant;
- Source footage access and upload limits;
- Whether the tool can inspect, edit, render, and export;
- Maximum file size and duration;
- Supported codecs and formats;
- Whether it can create captions, separate SRT files, project files, and multiple deliverables;
- Whether it can preserve source quality and frame rate;
- Whether it can use reference videos or style examples.

Check current official tool documentation when model names, supported controls, upload limits, export formats, or capabilities matter. Consumer apps and APIs may expose different controls. Never invent a model slug, feature, parameter, or export capability.

Use tool-specific prompt syntax only when documented. If the user has not named a tool and only needs a generic brief, write a tool-agnostic brief rather than blocking the task with unnecessary questions.

---

# 42. APPENDIX A — EXPANDED POST-PRODUCTION WORKFLOW

This appendix converts the editing principles into an operational workflow. Use the stages that match the project; do not force a full studio pipeline onto a small, simple video.

## A1. End-to-End Editing Pipeline

| Stage | Main work | Required output / checkpoint |
|---|---|---|
| 1. Brief intake | Confirm format, audience, runtime, story, humor, language, deliverables, restrictions | Approved or assumed editing brief |
| 2. Media intake | Inventory footage, audio, graphics, references, rights, and missing files | Media inventory and issue list |
| 3. Technical preflight | Check codecs, frame rates, resolution, audio, VFR, sync, corruption | Technical audit |
| 4. Project setup | Create bins, folders, timeline settings, proxies, backups | Openable project structure |
| 5. Footage review | Watch and log useful moments with source timecodes | Selects and timecode log |
| 6. Story assembly | Arrange events into a clear beginning, development, climax, and ending | Assembly / paper edit |
| 7. Rough cut | Remove repetition and dead time; establish narrative | Rough cut |
| 8. Fine cut | Refine jokes, reactions, pacing, transitions, and continuity | Fine cut |
| 9. Audio post | Clean and balance dialogue, music, ambience, and effects | Approved audio mix |
| 10. Color and graphics | Match shots, grade, titles, motion graphics, captions | Finished picture |
| 11. Picture lock | Confirm narrative and running time | Locked edit |
| 12. Export | Render required deliverables | Export files |
| 13. QC | Playback, technical checks, caption verification | QC report |
| 14. Handoff | Deliver master, subtitles, project, licenses, and notes as requested | Delivery manifest |

## A2. Editing Decision Log

For major editorial decisions, keep a concise log:

| Source timecode | What happens | Decision | Why | Destination timecode |
|---|---|---|---|---|
| [IN]–[OUT] | [Observed event] | Keep / Trim / Remove / Reorder / Enhance | [Story, clarity, humor, or pacing reason] | [Timeline location] |

Do not create a timecode entry for footage that has not been inspected.

## A3. Editorial Priorities

When two goals conflict, prioritize:

1. Truthful representation of what happened;
2. Viewer understanding;
3. Narrative coherence;
4. Dialogue and action clarity;
5. Comedic or emotional timing;
6. Appropriate pacing;
7. Visual polish;
8. Decorative effects.

Do not preserve a visually impressive shot if it makes the story confusing. Do not cut a quiet moment if it is essential to the emotional or comedic effect.

## A4. Review Types

- **Story review:** Does the video make sense without relying on the editor's knowledge?
- **Pacing review:** Are there stretches with no new information, emotion, or action?
- **Comedy review:** Does setup reach a payoff? Are reactions and pauses timed correctly?
- **Continuity review:** Are action, screen direction, game state, props, and positions consistent?
- **Audio-only review:** Does the story remain understandable with the screen off?
- **Visual-only review:** Are important actions and visual changes understandable without sound, where appropriate?
- **Mobile review:** Are text, faces, HUD, and important details legible on a small screen?
- **Final file review:** Does the actual export play correctly from beginning to end?

---
