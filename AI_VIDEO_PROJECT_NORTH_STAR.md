# AI-Assisted Video Production Project — North Star

> **Purpose of this file**
>
> This document is the primary project context for AI agents working on this project.
> It describes the long-term goal, current constraints, preferred technologies, learning strategy,
> and decision-making rules.
>
> **Any AI agent making technical, creative, tooling, or workflow decisions should read this file first
> and keep its recommendations aligned with these goals.**
>
> This file is intentionally high-level. Detailed implementation plans, episode specifications,
> character bibles, tool comparisons, and task files should live in separate documents.


---

## 1. Project Owner / Operator Profile

The person who will run and evolve this workflow is an experienced software engineer with more than
five years of professional full-stack development experience.

Primary technical background:

- C#
- .NET
- Angular
- Full-stack web application development
- Software architecture and engineering workflows

The project owner also uses AI tools heavily in day-to-day software development, including:

- Claude Code
- Codex
- ChatGPT
- Claude
- Other LLM-based and agentic AI tools where useful

This background is an important project advantage.

AI agents working on this project should **not treat the project owner as a non-technical beginner**.
The owner is a beginner in animation, Blender, 3D production, cinematography, and related creative
production disciplines, but is already comfortable with:

- Programming
- Debugging
- APIs
- Automation
- Scripting
- Version control
- Structured data
- Software architecture
- Agentic workflows
- Iterative engineering
- Learning new technical tools

Therefore, the preferred approach is to use software-engineering strengths to reduce repetitive creative
production work through automation.

When choosing between:

```text
manual repetitive workflow
```

and:

```text
well-structured automated / agent-assisted workflow
```

the project should generally prefer the second option, provided that quality remains acceptable.

The owner should still learn enough Blender, animation, camera, lighting, rigging, and visual storytelling
to understand, inspect, direct, and correct AI-generated work.

The intended long-term role is:

> **Technical animation director + system builder + quality controller**

rather than:

> **Traditional manual animator doing every production step by hand**


---

## 2. Project Goal

The goal is to learn and build a repeatable workflow for creating high-quality animated videos
for social media platforms such as:

- YouTube
- YouTube Shorts
- TikTok
- Instagram / Reels
- Facebook / Reels
- Other relevant video platforms in the future

The long-term objective is to create content that can build an audience and eventually generate revenue.

The current content focus is:

**Kids cartoons / animated stories**

The project may explore other content categories later, but educational content is intentionally
out of scope for the current phase so that learning and production effort stay focused.

The project should support both **short-form** and **long-form** cartoon content eventually.

However, the project should **start with short-form videos** because they provide a faster feedback loop,
require fewer assets, reduce rendering and production cost, and make it easier to learn the full pipeline.

---

## 3. Current Experience Level

Current animation / Blender / 3D-production knowledge:

**Beginner / effectively zero.**

This is acceptable.

The project should not assume prior knowledge of:

- Blender
- 3D modeling
- Rigging
- Character animation
- Lighting
- Camera composition
- Cinematography
- Rendering
- Lip sync
- Animation principles
- Sound design
- Video editing

The learning plan should be practical rather than academic.

---

## 4. Available Learning Time

The expected sustainable learning / production time is approximately:

**1 hour per day**

The project should therefore favor:

- Short learning cycles
- Small experiments
- Reusable assets
- Automation
- Incremental progress
- Learning concepts immediately before they are needed
- Avoiding large courses or tutorials that are unrelated to the current milestone

The default learning philosophy is:

> **Learn while building.**

Do not delay production for months in order to "master Blender" first.

A better loop is:

```text
Learn a small concept
        ↓
Apply it immediately
        ↓
Produce something
        ↓
Identify the weakness
        ↓
Learn the missing concept
        ↓
Improve
        ↓
Repeat
```

---

## 5. Visual Direction

The preferred long-term direction is:

**3D animation**

The project should investigate whether a practical AI-assisted 3D workflow can be built using Blender
and AI tools.

However, 3D is **not an absolute requirement for the first prototype**.

If early experiments show that 2D or 2.5D animation provides a significantly better combination of:

- production quality,
- learning speed,
- automation,
- consistency,
- rendering speed,
- and output volume,

then a 2D / 2.5D prototype is acceptable.

The decision should be evidence-driven.

### Current default decision

Start by testing a **very small 3D production experiment**.

Example:

```text
1 simple character
1 simple environment
1 object/prop
5–15 seconds
basic camera movement
basic lighting
basic character action
voice or sound
final rendered video
```

If this workflow proves practical, continue with 3D.

If it requires excessive manual work or the visual quality is poor, compare it with a 2D / 2.5D workflow
before committing further.

---

## 6. AI-First Production Philosophy

A central goal of this project is to use **agentic AI as heavily as practical** throughout the production cycle.

Preferred AI assistants include tools such as:

- ChatGPT / Codex
- Claude / Claude Code
- AI tools that can connect to Blender or other production software
- MCP servers
- Plugins
- Connectors
- AI image-generation tools
- AI voice-generation tools
- AI-assisted 3D-generation tools

AI should reduce repetitive manual work while keeping the creator in control of quality and direction.

The target is **not**:

> "Press one button and blindly upload whatever AI generates."

The target is:

> **Build an AI-assisted animation production system where humans provide direction and quality judgment,
> while AI and software perform as much repetitive production work as possible.**

---

## 7. Desired Human vs. AI Responsibilities

### AI / automation should handle as much as possible

Examples:

- Story ideas
- Script drafts
- Dialogue drafts
- Story structure
- Shot-list generation
- Storyboards / visual references
- Character concepts
- Environment concepts
- Blender scripting
- Repetitive Blender operations
- Scene setup
- Object placement
- Camera setup
- Lighting presets
- Asset generation
- Basic model generation
- Rigging assistance
- Animation setup
- Lip-sync automation
- Voice generation
- Sound-effect planning
- Music planning
- Rendering automation
- FFmpeg/video composition
- Subtitle generation
- Technical QA
- File organization
- Metadata generation
- Pipeline debugging

### Human responsibility should focus on

- Creative direction
- Choosing ideas worth producing
- Selecting the best character/world designs
- Deciding whether animation looks natural
- Evaluating camera composition
- Evaluating lighting
- Story quality
- Pacing
- Emotional clarity
- Comedy / storytelling effectiveness
- Final quality control
- Final publishing decisions

The long-term goal is for the human role to move increasingly toward:

**Director + reviewer + decision maker**

rather than:

**Manual animator + manual editor + repetitive production worker**

---

## 8. Core Production Software

### Blender

Blender is currently the preferred main animation/rendering platform because it is:

- Free and open source
- Suitable for 3D modeling
- Suitable for rigging
- Suitable for character animation
- Suitable for lighting and camera work
- Scriptable with Python
- Compatible with automation
- Suitable for agentic workflows
- Extensible through plugins and MCP-based integrations

The project should actively investigate workflows where Claude Code, Codex, ChatGPT, or similar agents
can operate or automate Blender.

Examples include:

```text
Natural-language instruction
        ↓
AI agent
        ↓
Blender MCP / plugin / Python
        ↓
Blender scene
        ↓
render
```

Do not require the creator to manually perform an operation if it can be automated reliably.

At the same time, do not treat Blender as a black box.
The creator should gradually learn enough Blender to inspect, understand, and correct AI-generated work.

---

## 9. AI-Assisted 3D Model Generation

AI 3D-generation services are candidates for speeding up asset production.

Current tools of interest include:

### Meshy

https://www.meshy.ai/

Potential uses:

- Text-to-3D
- Image-to-3D
- Character / prop generation
- Environment assets
- Rapid prototyping

### Tripo AI

https://www.tripo3d.ai/

Potential uses:

- Text-to-3D
- Image-to-3D
- Asset generation
- Texturing
- Rigging / animation assistance
- Rapid prototyping

### Hyper3D / Rodin

https://hyper3d.ai/

Potential uses:

- Image/text-to-3D workflows
- Character and prop experimentation
- Rapid asset generation

### Subscription rule

**Do not immediately purchase a Pro subscription simply because an AI 3D generator looks impressive.**

The preferred approach is:

1. Test available free tiers / credits.
2. Generate the same small group of assets with multiple tools.
3. Import the results into Blender.
4. Evaluate:
   - mesh quality,
   - topology,
   - texture quality,
   - character consistency,
   - rigging suitability,
   - animation suitability,
   - export compatibility,
   - cleanup time,
   - automation/API support,
   - cost.
5. Only then choose a paid service.

A paid subscription is justified if it measurably reduces production time or improves quality.

The objective is not to collect AI subscriptions.

The objective is to build the **most efficient production pipeline**.

---

## 10. AI Image Generation

AI image generation can be used heavily even in a 3D workflow.

Possible uses:

- Character concept art
- Character reference sheets
- Front / side / back references
- Facial-expression references
- Environment concepts
- Props
- Storyboards
- Shot references
- Thumbnail concepts
- Texture concepts

Possible tools include ChatGPT image generation, Gemini / Nano Banana, or another tool that proves better
for the required task.

Generated images should be treated as production inputs / references rather than automatically becoming
the final animation.

---

## 11. Voice Generation

AI voice generation is preferred over manually recording voices during the early stages.

The system should eventually support:

```text
Script
   ↓
Character dialogue
   ↓
Voice generation
   ↓
Audio files
   ↓
Lip sync
   ↓
Animation timeline
```

Important requirements:

- Stable character voices across episodes
- Clear speech
- Appropriate emotional tone
- Reusable voice identities
- Good dialogue/music/SFX balance

Voice consistency matters more than having the most realistic voice.

---

## 12. Video Generation Without AI Video Models

The preferred long-term strategy is **not** to depend on generative AI video models for every shot.

Instead:

```text
AI
│
├── ideas
├── scripts
├── images
├── voices
├── 3D assets
└── production instructions
        ↓
Blender / animation software
        ↓
deterministic animation + rendering
        ↓
final video
```

Reasons:

- Better character consistency
- Better control
- Reusable assets
- Lower cost per future episode
- Repeatable animation
- Easier revisions
- Easier long-form production
- Stronger automation potential
- Same 3D assets may later be usable in games

AI video-generation models may still be used experimentally when they provide clear value, but they
should not become an unavoidable dependency of the production pipeline.

---

## 13. Initial Learning Areas

The creator should learn these progressively while building.

### Highest priority

1. Blender fundamentals
2. Animation fundamentals
3. Character animation
4. Keyframes, timing and spacing
5. Camera angles and composition
6. Basic lighting
7. Rigging fundamentals
8. Basic 3D asset workflow
9. Rendering

### Next priority

10. Facial animation
11. Lip sync
12. Storytelling
13. Visual storytelling
14. Sound design
15. Editing / pacing
16. Materials / texturing
17. Environment design
18. Character design

### Automation / engineering

19. Blender Python API
20. Blender MCP / agent integrations
21. Claude Code / Codex workflows
22. Reusable animation libraries
23. Asset management
24. Automated rendering
25. FFmpeg
26. Automated QA
27. Structured episode specifications

Do not attempt to learn all of these before creating the first video.

---

## 14. Content Strategy

### Phase-gate principle

Every phase is **iterative, not one-and-done**.

A generated clip does not count as a successful milestone merely because it rendered without errors.

For each phase:

```text
Create
  ↓
Watch critically
  ↓
Identify problems
  ↓
Diagnose why they happened
  ↓
Fix the workflow / prompt / asset / animation / camera / lighting
  ↓
Generate again
  ↓
Repeat until satisfied
```

It is expected that the project may create **multiple versions or multiple clips within the same phase**.

Examples of reasons to repeat a clip:

- Character motion looks robotic
- Camera angle is weak
- Lighting is poor
- Model or texture quality is inconsistent
- Rigging creates bad deformation
- Timing feels wrong
- Scene composition is unclear
- AI-generated assets need cleanup
- Automation produces unreliable results
- The final clip simply does not look good enough

Do not hide failures or rush forward just to complete a milestone.

Each failed or weak attempt should produce a useful diagnosis:

```text
What is wrong?
Why did it happen?
Was the problem creative, technical, or tooling-related?
What should change in the next attempt?
Can the fix become reusable?
```

**Only move to the next phase when the project owner has enough confidence in the current workflow
and is personally satisfied that the output quality and repeatability are good enough to continue.**

Confidence matters more than completing a fixed number of clips.

---

### Phase A — Tiny experiments

Target:

**5–15 second videos**

Purpose:

- Learn Blender
- Test AI ↔ Blender integration
- Test 3D asset generation
- Learn basic animation
- Learn lighting and cameras
- Establish rendering workflow
- Learn how to diagnose weak results and iterate until the output is acceptable
- Build confidence before increasing duration or complexity

The first attempt is not expected to be final. Multiple 5–15 second experiments should be created
whenever needed until the project owner is satisfied with the result and understands the major causes
of previous failures.

Examples:

- Character waves
- Character walks toward an object
- Character reacts to something
- Character interacts with a simple prop
- Object transformation
- Basic camera sequence

---

### Phase B — Short-form social content

Target:

**15–60 seconds**

Platforms:

- YouTube Shorts
- TikTok
- Instagram Reels
- Facebook Reels

Goals:

- Develop a recognizable visual style
- Improve hooks
- Improve pacing
- Improve animation
- Build reusable assets
- Learn what audiences respond to
- Reduce production time per video
- Produce multiple iterations when necessary rather than accepting the first render
- Move forward only when short-form production feels sufficiently controllable and repeatable

---

### Phase C — Short episodes

Target:

**1–5 minutes**

Introduce:

- Recurring characters
- Multiple shots
- Dialogue
- Simple stories
- Reusable environments
- Reusable animation clips
- Better sound design

---

### Phase D — Longer episodes

Target eventually:

**5–15+ minutes**

Only move here after the short-form pipeline is stable **and the project owner feels confident
that quality problems can be identified, corrected, and reproduced reliably**.

Long-form content should reuse:

- characters,
- rigs,
- environments,
- props,
- animation clips,
- lighting presets,
- camera presets,
- audio assets,
- and automation code.

Do not attempt long-form animation by creating every scene from scratch.

---

## 15. Kids Cartoon Direction

The long-term cartoon workflow should use **original intellectual property**.

Create:

- Original characters
- Original names
- Original world
- Original stories
- Original visual identity
- Original dialogue
- Properly licensed/original music and SFX

Existing successful cartoons can be studied for:

- pacing,
- camera work,
- visual storytelling,
- animation principles,
- episode structure,
- comedic timing,
- and production techniques.

They should **not** be copied.

The project should avoid imitating protected characters, distinctive character designs, voices,
music, or stories.

---

## 16. Reuse Is a Core Strategy

Every useful production asset should ideally become reusable.

Example:

```text
characters/
    hero/

environments/
    forest/
    classroom/
    bedroom/

props/
    ball/
    book/
    bicycle/

animations/
    idle/
    walk/
    run/
    jump/
    wave/
    point/
    laugh/
    surprised/

cameras/
    wide/
    medium/
    close_up/

lighting/
    daylight/
    sunset/
    indoor_soft/
```

The first video may take a long time.

Future videos should become faster because the library grows.

The project should measure success partly by how much reusable capability each milestone creates.

---

## 17. Automation Architecture — Long-Term Direction

The eventual production system may resemble:

```text
Idea
  ↓
ChatGPT / Claude
  ↓
Story + Script
  ↓
Structured Episode Specification
  ↓
Shot Planner
  ↓
Asset Selection / Generation
  ↓
3D Character + Environment
  ↓
Rig / Animation Library
  ↓
Blender automation
  ↓
Camera + Lighting
  ↓
Voice + Lip Sync
  ↓
Music + SFX
  ↓
Render
  ↓
Video composition
  ↓
Automated technical QA
  ↓
Human creative QA
  ↓
Publish
```

A future episode should ideally be represented using structured data rather than a collection of
untracked prompts.

Example:

```json
{
  "episode": "example",
  "shots": [
    {
      "duration": 5,
      "environment": "forest",
      "character": "hero",
      "animation": "walk",
      "camera": "wide",
      "dialogue": null
    }
  ]
}
```

This will make the pipeline:

- reproducible,
- debuggable,
- cheaper to regenerate,
- easier for AI agents to operate,
- and easier to scale.

---

## 18. Important Engineering Principle

Do not let any individual AI provider become the architecture.

Bad architecture:

```text
Prompt
  ↓
Specific AI service
  ↓
final video
```

Preferred architecture:

```text
Episode specification
        ↓
Production pipeline
        ↓
replaceable providers
```

For example:

```text
3DGenerator interface
├── Meshy
├── Tripo
├── Rodin
└── future provider
```

Similarly:

```text
VoiceProvider
ImageProvider
LLMProvider
RenderEngine
```

Tools will change.

The project goals should not.

---

## 19. Manual Work Should Be Reduced, Not Eliminated Blindly

Automation is valuable when it:

- saves meaningful time,
- produces reliable results,
- improves consistency,
- allows easier iteration,
- or makes production scalable.

Do **not** automate a bad workflow just because it is technically possible.

Before automating a production step:

1. Understand what a good result looks like.
2. Create or validate at least one acceptable result.
3. Identify repeatable actions.
4. Automate those actions.
5. Keep human review where judgment still matters.

---

## 20. Quality Over Upload Volume

The project should not optimize for mass-producing low-quality AI content.

Priority order:

```text
Quality
  ↓
Consistency
  ↓
Audience value
  ↓
Repeatability
  ↓
Production speed
  ↓
Volume
```

Automation should allow **better content**, not simply more content.

---

## 21. Revenue Goal

Generating revenue is a long-term objective, but early decisions should not be based solely on immediate monetization.

Early milestones should optimize for:

- learning,
- visual quality,
- repeatability,
- audience response,
- asset reuse,
- production efficiency.

Possible future revenue channels may include:

- Platform advertising revenue
- Sponsorships
- Brand partnerships
- Licensing original characters / IP
- Games
- Digital products
- Merchandise where appropriate
- Other opportunities that emerge after an audience exists

Do not assume revenue before demonstrating that people want to watch the content.

---

## 22. Relationship to Future Game Development

3D assets should preferably be created in ways that do not unnecessarily prevent future reuse.

The creator is also interested in possible future Unity / C# game development.

Where practical, assets should therefore consider:

- reasonable topology,
- reusable rigs,
- animation clips,
- texture organization,
- exportable formats,
- sensible scale,
- modular environments.

This is **not** a requirement for the first videos, but avoiding obviously unusable assets may save work later.

A possible long-term ecosystem is:

```text
Original IP
    │
    ├── YouTube / social animation
    ├── Unity games
    └── Other interactive content
```

---

## 23. Default Tooling Direction

Current preferred / candidate stack:

| Area | Preferred / Candidate Tools |
|---|---|
| Creative planning | ChatGPT |
| Engineering / automation | Claude Code, Codex |
| Agent interoperability | MCP, plugins, connectors |
| Main animation software | Blender |
| AI image generation | ChatGPT Images, Gemini / Nano Banana, other suitable models |
| AI 3D generation | Meshy, Tripo, Hyper3D Rodin — evaluate first |
| Voice generation | Suitable TTS provider — select based on consistency and quality |
| Video/audio composition | FFmpeg |
| Automation | Python |
| Version control | Git |
| Storage | Local first; cloud when justified |
| Rendering | Blender locally first; cloud GPU only if needed |

This table represents the current direction, not permanent vendor commitments.

---

## 24. First Practical Milestone

The first serious milestone should **not** be a 10-minute cartoon.

It should be something approximately like:

### 3D Technical Proof of Concept

**Duration:** 5–15 seconds

Requirements:

- One simple original character
- One environment
- One prop
- Character imported/generated successfully
- Basic rig
- One or two basic actions
- One camera setup
- Simple lighting
- Rendered through Blender
- Optional short voice/SFX
- Final MP4 produced
- Process documented
- Identify which steps were automated vs. manual

The purpose is to answer:

> **Can an AI-assisted Blender workflow produce visually acceptable 3D animation with a reasonable amount of human effort?**

Only after answering this should the project commit strongly to the 3D production path.

---

## 25. Success Criteria for Early Experiments

Do not judge an experiment only by whether a video file was generated.

A phase may require several attempts. If the project owner is not satisfied, the correct action is to
review the result, identify the mistakes or weaknesses, change the workflow, and generate again.

The project should not advance simply because a checklist was completed.

Evaluate:

### Visual quality

- Does it look intentional?
- Is the character consistent?
- Does the motion look acceptable?
- Is the lighting readable?
- Is the camera useful rather than random?

### Automation

- How much manual Blender work was required?
- Could the same process be repeated by an AI agent?
- Were failures easy to diagnose?

### Reusability

- Can the model be reused?
- Can the rig be reused?
- Can the animation be reused?
- Can the environment be reused?

### Time

- How much creator time was required?

### Cost

- What paid services were used?
- Did each service create enough value to justify its cost?

### Learning

- What new skill was acquired?

---

## 26. Rules for AI Agents Working on This Project

AI agents should follow these rules unless the project owner explicitly changes them.

### Rule 1 — Stay aligned with the goal

Do not turn this into a generic Blender-learning project.

The goal is:

> **AI-assisted, scalable video production for social media, focused on original kids cartoons and animated stories.**

### Rule 2 — Favor practical production

Prefer building something small over studying something large.

### Rule 3 — Prefer reuse

Do not recreate assets unnecessarily.

### Rule 4 — Prefer automation

If repetitive work can be safely and reliably automated, automate it.

### Rule 5 — Do not automate before proving quality

First establish what an acceptable result looks like.

### Rule 6 — Keep the human as creative director

Human judgment remains mandatory for quality, story, pacing, and final approval.

### Rule 7 — Avoid unnecessary subscriptions

Test before paying.

### Rule 8 — Do not lock the architecture to one vendor

Meshy, Tripo, Rodin, voice providers, LLMs, and image models should be replaceable where practical.

### Rule 9 — Start short

Do not jump to long episodes before the short production pipeline works.

### Rule 10 — Preserve original IP

Do not copy existing cartoon characters, voices, designs, music, or stories.

### Rule 11 — Keep project artifacts organized

Important decisions should be written to project files instead of existing only in chat history.

### Rule 12 — Challenge weak assumptions

If a proposed approach is expensive, difficult, low quality, or not scalable, say so and propose a better experiment.

---

## 27. Current Strategic Position

At this stage, the preferred strategy is:

```text
Learn Blender fundamentals while building
        ↓
Test Claude/Codex ↔ Blender automation
        ↓
Test AI-generated 3D assets
        ↓
Create a 5–15 second 3D animation
        ↓
Evaluate quality + effort
        ↓
If unsatisfied: diagnose → fix → generate again
        ↓
Repeat until confident
        ↓
Choose:
   ├── continue 3D
   └── test 2D/2.5D alternative
        ↓
Produce 15–60 second short content
        ↓
Build reusable asset / animation library
        ↓
Increase automation
        ↓
Produce 1–5 minute content
        ↓
Eventually attempt long-form episodes
```

---

## 28. Immediate Next Steps

Recommended immediate sequence:

1. Learn basic Blender navigation and timeline concepts.
2. Set up an AI-to-Blender workflow (Claude/agent + Blender MCP/plugin/script).
3. Create or obtain one simple original 3D character.
4. Test Meshy, Tripo and/or Rodin using free access before choosing a paid plan.
5. Import the chosen asset into Blender.
6. Test rigging.
7. Create a very simple animation.
8. Add basic camera and lighting.
9. Render a 5–15 second clip.
10. Review the entire clip critically and document problems.
11. If the result is not satisfactory, identify the root causes and create another version.
12. Repeat the 5–15 second experiment as many times as needed until the project owner has enough
    confidence in both quality and repeatability.
13. Decide whether to continue directly with 3D or run a comparable 2D/2.5D test.
14. Only after the workflow is validated and the project owner is satisfied, create the first
    15–60 second social video.

---

## 29. Final North-Star Statement

> **Build the skills and software pipeline required to create original, high-quality animated social-media content with minimal repetitive manual work. Use AI aggressively for ideation, asset creation, engineering, and automation; use Blender or similar deterministic animation software for controllable production; learn animation and directing through practical projects; start with short-form experiments; build reusable assets; and only scale into long-form kids cartoons and animated stories after the production workflow is proven.**

