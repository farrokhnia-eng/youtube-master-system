# Storyboards, AI Visuals, and Tool Routing

> From YouTube Master System V5.0, sections 17, 45. Original section numbers are kept, so cross-references still work. The section map is in SKILL.md.

## Contents

- 17. STORYBOARDS, SHOT LISTS, AND AI VISUAL PRODUCTION
- 45. APPENDIX D — TOOL ROUTING AND MODEL ADAPTATION
  - D1. Tool Categories
  - D2. Current-Model and Feature Recency Gate
  - D3. Video-Generation Prompt Structure
  - D4. Reference Image Editing
  - D5. Voice and Music Tool Prompts
  - D6. ComfyUI and Node-Based Image Workflows
  - D7. Visual-Asset and 3D-Asset Prompts
  - D8. Voice-AI Prompt Structure
  - D9. Workflow-Automation Prompt Structure
  - D10. Research and Browser-Agent Prompt Structure

---

# 17. STORYBOARDS, SHOT LISTS, AND AI VISUAL PRODUCTION

For each scene, specify:

- Scene number;
- Shot number;
- Duration;
- Narrative purpose;
- Location;
- Characters;
- Character action;
- Shot size;
- Camera angle;
- Camera movement;
- Lens or perspective when useful;
- Lighting;
- Composition;
- Visual continuity;
- Sound effects;
- Transition;
- Generation prompt.

For each AI video prompt, define:

- Subject;
- Action;
- Environment;
- Camera;
- Lighting;
- Composition;
- Motion;
- Visual style;
- Temporal continuity;
- Audio requirements.

Identify the first frame as the visual reference for each shot when the tool workflow supports reference images. Preserve character count, wardrobe, props, location, lighting, time of day, and scene state. Carry the user's restrictions—such as no dialogue, music, lip-sync, or extra characters—through every shot.

Adapt prompts to the selected tool's actual capabilities and limitations. Never guarantee a generated result.

---

# 45. APPENDIX D — TOOL ROUTING AND MODEL ADAPTATION

## D1. Tool Categories

| Tool category | Prompting emphasis | Verify before use |
|---|---|---|
| Human editor | Editorial intent, timeline notes, references, deliverables, deadlines | NLE, codecs, project handoff |
| Non-linear editor (NLE) | Track structure, bins, timecodes, effects, color, audio, export | Current app version, feature names, supported formats |
| AI editor / autonomous editor | Objective, media access, edit scope, actual export, permissions, stop conditions | Upload limits, render capability, export options, paid features |
| General LLM | Goal, context, constraints, audience, output format, grounding | File access and whether it can actually render media |
| Video generation AI | Subject, action, setting, camera, movement, lighting, duration, continuity | Model version, reference support, duration, aspect ratio, audio controls |
| Image generation AI | Subject, pose/action, setting, style, lighting, composition, aspect ratio | Model-specific syntax and negative-prompt support |
| Reference-image editor | Keep/change boundary, reference attachment, amount of change | Image-editing mode and reference capability |
| Node-based image workflow | Separate positive and negative prompts, model/checkpoint, node inputs | Checkpoint, sampler, node graph, token limits |
| Voice AI | Voice permissions, language, accent, emotion, pacing, emphasis, pauses | Voice rights, pronunciation controls, export format |
| Music AI | Genre, mood, BPM, instrumentation, structure, vocals, license | Commercial-use terms, download/export limits, Content ID conditions |
| Research/orchestration AI | Search scope, primary sources, citations, uncertainty, final artifact | Current browsing tools and citation behavior |
| Workflow automation | Trigger, event, action, field mapping, credentials, failure handling | Connected apps, authentication, permissions |

## D2. Current-Model and Feature Recency Gate

Model names, controls, upload limits, supported media types, export formats, and pricing change frequently.

When a prompt depends on current model behavior:

1. Verify the latest model name and features in the provider's official documentation;
2. Distinguish the consumer app, desktop app, API, and agent environment;
3. Do not assume they share the same model or controls;
4. Avoid hardcoding an unverified model slug, context window, parameter, or feature;
5. If verification is unavailable, mark tool-specific details unverified and use stable, tool-agnostic instructions.

Do not copy model-version recommendations from an old reference file without checking them. The uploaded Prompt Master skill contains tool/model-specific examples; treat those as routing examples, not as permanent facts.

## D3. Video-Generation Prompt Structure

When the task is to generate footage rather than edit existing footage, use a shot-level prompt:

```text
Shot ID:
Duration:
Subject:
Action:
Setting:
Composition:
Shot size / angle:
Camera movement:
Lighting:
Color and visual style:
Continuity anchors:
Audio requirements:
Reference image(s):
Negative constraints:
Output format:
```

Do not use a video-generation prompt when the user wants a real source-video edit. Do not substitute newly generated footage for supplied footage unless the user requests it.

## D4. Reference Image Editing

For an existing image, describe only the intended change and explicitly identify what must remain unchanged:

```text
Reference image: [attached]
Keep unchanged: [identity, pose, clothing, layout, background, lighting, etc.]
Change only: [specific requested change]
Change amount: [subtle / moderate / substantial]
Maintain: [style, perspective, color, continuity]
Avoid: [unwanted changes]
```

Tell the user to attach the reference image to the target tool when the tool requires it. Do not describe a full new scene when the task is only to edit an existing image.

## D5. Voice and Music Tool Prompts

For voice generation, specify language, accent, voice authorization, emotion, pacing, emphasis, pronunciation, pause placement, and output type. Do not ask the model to imitate a living person's voice without authorization or to recreate an identifiable voice deceptively.

For music generation, separate the creative brief from lyrics, arrangement, and output settings. State whether the track must be instrumental or include vocals. Include commercial-use and attribution requirements where relevant. Do not assume a generated track is automatically copyright-safe.

## D6. ComfyUI and Node-Based Image Workflows

When a YouTube production task requires ComfyUI or another node-based image workflow, do not treat it as a single prompt box. Confirm the checkpoint/model and the workflow's supported conditioning method when those details affect the result.

When the workflow accepts separate positive and negative text conditioning, provide two clearly separated blocks:

```text
POSITIVE PROMPT:
[Subject, action, setting, style, lighting, composition, camera perspective, color direction, and required visual details.]

NEGATIVE PROMPT:
[Unwanted objects, visual defects, anatomy issues, text, logos, watermarks, blur, or other prohibited elements.]

MODEL / CHECKPOINT: [verified model]
WORKFLOW: [workflow or node graph]
OUTPUT SIZE: [width × height]
OTHER SETTINGS: [only settings verified for this workflow]
```

Do not copy generic sampler, CFG, step-count, or resolution values from an old prompt library as universal settings. These are checkpoint- and workflow-dependent. Verify the model documentation and current node graph.

## D7. Visual-Asset and 3D-Asset Prompts

For image or 3D asset generation used in a video, define:

- Asset purpose in the edit;
- Subject and distinctive features;
- Style (photorealistic, stylized, low-poly, etc.);
- Primary materials and textures;
- Lighting and composition;
- Background requirements;
- Aspect ratio or geometry constraints;
- Required view or pose;
- Intended use (thumbnail, overlay, B-roll, 3D scene, game asset, or animation);
- Required export format.

For a 3D character intended for rigging, specify the required pose (A-pose or T-pose) only when the target tool supports it and the downstream rigging workflow needs it. For 3D assets, state the target platform and format (for example, GLB/FBX for real-time use or STL for printing) only when relevant.

## D8. Voice-AI Prompt Structure

When generating narration or dialogue, specify:

- Authorized voice or approved synthetic voice;
- Language and locale;
- Accent target (for example, natural American English, without exaggerated slang);
- Age impression only when relevant and appropriate;
- Emotion;
- Energy;
- Pacing and speech rate;
- Pronunciation of names and technical terms;
- Words to emphasize;
- Pause locations;
- Delivery style;
- Output format and sample rate.

Use SSML or tool-specific emphasis/pause markers only when supported. Distinguish voice-over from subtitles and dubbing. Do not clone or imitate an identifiable person's voice without appropriate authorization.

## D9. Workflow-Automation Prompt Structure

When building an automation for content production, define:

```text
Trigger application:
Trigger event:
Input data:
Validation / filtering:
Action application:
Action:
Field mapping:
Authentication assumptions:
Error handling:
Retry limits:
Logging:
Human approval points:
Output / completion signal:
```

For multi-step automation, state what data passes from one step to the next. Never include API keys, access tokens, passwords, or connection secrets in the prompt. Assume approved authentication is configured outside the prompt.

## D10. Research and Browser-Agent Prompt Structure

For research agents, specify whether the task is search, comparison, extraction, fact-checking, or synthesis. Require primary sources, publication dates, exact URLs, and explicit uncertainty labels. For browser agents that can act on accounts or publish content, state whether the task is research-only or action-authorized. Require approval before submitting, purchasing, publishing, deleting, or sending anything externally.

---
