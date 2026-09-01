# Practical Study Plan — AI-Assisted Blender 15-Second 3D Clip

> **Project companion document**
>
> Read `AI_VIDEO_PROJECT_NORTH_STAR.md` first.
>
> This file converts the project direction into a practical learning path.
> It is deliberately **not a weekly schedule**.
>
> The learning method is:
>
> **learn a small concept → use it immediately → inspect the result → fix problems → automate what is repeatable**
>
> The first major learning target is a **finished 15-second 3D animated clip** created with Blender,
> AI-generated/AI-assisted assets, Claude Code, and Blender automation/MCP where practical.

---

# 1. Goal of This Study Plan

The purpose of this plan is **not** to become a Blender expert before producing anything.

The purpose is to learn only the Blender, animation, camera, lighting, asset, rendering, and AI-automation
skills required to produce one small but complete animated clip.

The final learning milestone is:

## 15-Second 3D Technical Story Clip

Target characteristics:

- 15 seconds
- 3D
- One simple original stylized character
- One simple environment
- One prop
- Basic character movement
- One simple interaction or reaction
- 2–3 camera shots
- Basic lighting
- Basic sound / SFX
- Optional short narrator line
- No character lip-sync required yet
- Rendered in Blender
- Final MP4 produced
- AI / Claude assists as much of the workflow as practical
- Every major problem and fix is documented

The clip does **not** have to be YouTube-ready commercial content.

It needs to prove that the workflow works and that the project owner understands enough of each stage
to diagnose weak results.

---

# 2. Why the First Clip Should Stay Simple

Do not introduce these into the first 15-second milestone unless absolutely necessary:

- Multiple speaking characters
- Complex facial animation
- Lip sync
- Hair simulation
- Cloth simulation
- Complex physics
- Detailed environments
- Photorealism
- Complex human anatomy
- Long dialogue
- Large camera rigs
- Advanced compositing

These features create additional failure points before the core workflow has been proven.

The first clip should test this chain:

```text
Idea
 ↓
Asset
 ↓
Blender
 ↓
Rig / motion
 ↓
Animation
 ↓
Camera
 ↓
Lighting
 ↓
Render
 ↓
Audio
 ↓
Review
 ↓
Revision
 ↓
Final MP4
```

---

# 3. Suggested First Clip Concept

Use a deliberately simple micro-story.

Example:

## "The Curious Toy"

```text
0–5 sec
Wide shot:
A small stylized character walks into a simple colorful clearing.

5–10 sec
Medium shot:
The character notices a colorful toy/object and reacts.

10–15 sec
Closer shot:
The character approaches or interacts with the object,
then performs a simple happy reaction.
```

The exact story may change.

The important constraints are:

- one character,
- one prop,
- one location,
- one readable action,
- one readable reaction.

The first clip should be simple enough that poor quality can be diagnosed clearly.

---

# 4. Working Rule: Manual Once, Automate Next

For each major Blender concept:

1. Perform or inspect the operation manually at least once.
2. Understand what changed in the scene.
3. Repeat it through Claude Code / Blender MCP / Python where practical.
4. Compare the automated result with the manual result.
5. Keep automation only when it is reliable.

Example:

```text
Manually add a light once
        ↓
Understand position / energy / type
        ↓
Ask Claude to create it
        ↓
Inspect result
        ↓
Refine prompt / automation
```

The goal is **not** to manually master every Blender workflow.

The goal is to understand enough to direct and debug the automation.

---

# 5. Step 0 — Create the Git Repository

Before learning Blender, create the project repository.

Suggested structure:

```text
ai-animation-lab/
│
├── README.md
├── AI_VIDEO_PROJECT_NORTH_STAR.md
├── STUDY_PLAN_15S_BLENDER_AI.md
│
├── docs/
│   ├── decisions/
│   ├── experiments/
│   └── retrospectives/
│
├── assets/
│   ├── characters/
│   ├── environments/
│   ├── props/
│   ├── textures/
│   └── audio/
│
├── blender/
│   ├── scenes/
│   ├── assets/
│   ├── scripts/
│   └── renders/
│
├── episode-specs/
│
├── output/
│
└── tools/
```

Add generated renders and very large assets to `.gitignore` when appropriate.

For large binary assets, do not blindly commit everything to normal Git history.

### Learn now

- Nothing new if already comfortable with Git.

### Deliverable

Repository exists and contains:

- `AI_VIDEO_PROJECT_NORTH_STAR.md`
- this study plan

---

# 6. Step 1 — Learn Only the Blender Interface Needed to Survive

Open Blender 5.2 and learn these concepts directly in the application:

- 3D Viewport
- Outliner
- Properties panel
- Timeline
- Object Mode
- Edit Mode
- Move
- Rotate
- Scale
- Select / delete
- Add object
- Save `.blend`
- Undo / redo
- View from different angles
- Frame selected object

Do not start learning advanced modeling.

### Practical exercise

Create a scene containing:

- cube,
- sphere,
- plane.

Move them to three different positions.

Rename them in the Outliner.

Save the project as:

```text
blender/scenes/001-interface-basics.blend
```

### What must be understood before moving on

You should be able to answer:

- What is an object?
- What is a mesh?
- Where can I see all objects in the scene?
- How do I move an object?
- How do I save the scene?

### AI usage

Low.

Do this mostly yourself once.

Ask ChatGPT/Claude questions when something is unclear.

---

# 7. Step 2 — Build a Primitive Scene Manually

Create a tiny environment from Blender primitives.

Example:

```text
Plane      → ground
Cube       → simple block / pedestal
Sphere     → prop
Sun/Area   → light
Camera     → camera
```

Do not worry about artistic quality.

### Learn now

- Object transforms
- World coordinates
- Local vs global transforms at a basic level
- Object origin at a basic level
- Basic materials
- Assigning simple colors

### Practical exercise

Make a simple colorful scene that looks intentional in the viewport.

### Deliverable

```text
blender/scenes/002-primitive-scene.blend
```

### Success condition

You can open the file later and understand roughly how the scene was assembled.

---

# 8. Step 3 — Learn Keyframes by Animating One Object

Before character animation, animate something trivial.

Use the sphere or cube.

Example:

```text
Frame 1   → object on left
Frame 36  → object in center
Frame 72  → object on right
```

Then experiment with:

- location keyframes,
- rotation keyframes,
- scale keyframes.

### Learn now

- Timeline
- Current frame
- Keyframes
- Playback
- Interpolation
- Dope Sheet basics
- Graph Editor basics
- Ease-in / ease-out
- Timing and spacing at a basic level

### Practical exercise

Create a 3-second animation of a ball:

- enters,
- bounces or moves,
- stops.

Do not use physics yet.

Keyframe it.

### Deliverable

```text
blender/scenes/003-keyframe-basics.blend
```

and a low-quality preview render.

### Important lesson

If movement looks robotic, do not immediately ask AI to fix it.

First inspect:

- keyframe timing,
- spacing,
- interpolation.

This is the beginning of animation judgment.

---

# 9. Step 4 — Learn Camera Basics by Creating Three Shots

Use the simple primitive scene.

Create or reposition a camera to understand:

- wide shot,
- medium shot,
- close shot.

### Learn now

- Camera position
- Camera rotation
- Basic focal length concept
- Framing
- Subject placement
- Camera keyframes
- When a cut is better than an unnecessary camera move

### Practical exercise

Create three very short views of the same object:

```text
Shot A → wide
Shot B → medium
Shot C → close
```

Do not make the camera movement complicated.

### Deliverable

A 3–5 second test showing clear shot changes or a simple camera move.

### Human responsibility

You must decide:

> Does the shot make the subject easy to understand?

That judgment should not be delegated completely to AI.

---

# 10. Step 5 — Learn Basic Lighting Through Comparison

Do not study professional lighting theory yet.

Create the same primitive scene using a few simple arrangements.

Test:

- one light,
- two lights,
- daylight-like setup,
- softer vs harder lighting.

### Learn now

- Sun light
- Area light
- Light intensity / energy
- Light position
- Shadow readability
- World/background lighting
- Basic three-point-lighting concept

### Practical exercise

Render the same camera frame with 2–3 lighting variations.

Save comparisons under:

```text
blender/renders/lighting-tests/
```

### Question to answer

Which setup makes the character/object easiest to read?

Do not choose merely because the scene is brighter.

---

# 11. Step 6 — Perform Your First Blender Render

Before introducing MCP, prove that Blender itself can produce output correctly.

### Learn now

- Render engine selection
- Output resolution
- Frame rate
- Output path
- Image render vs animation render
- Basic output format
- Preview quality vs final quality

For the first project, use a fast real-time rendering approach such as **EEVEE** unless there is a
specific reason to use a heavier renderer.

Suggested learning settings:

```text
24 fps
720p preview renders
```

At 24 fps:

```text
15 seconds = 360 frames
```

Do not render 360 final-quality frames yet.

### Deliverable

A short primitive animation rendered successfully from Blender.

---

# 12. Step 7 — Install and Understand Blender MCP

Now introduce agentic control.

The currently relevant community project is BlenderMCP, which connects Blender to LLM clients through
the Model Context Protocol.

Reference:

https://github.com/MCPBlender/blender-mcp

Because Blender, Claude Code, and community MCP servers change over time, follow the project's **current**
installation instructions rather than copying an old setup guide into this repository.

### Important compatibility rule

The project owner currently uses Blender 5.2.

Before installing:

1. Read the current BlenderMCP README / release notes.
2. Check open issues for Blender 5.x / 5.2 compatibility.
3. Back up important `.blend` files.
4. Test MCP in a disposable Blender scene first.

Do not downgrade Blender automatically unless a real compatibility problem is demonstrated.

### Learn now

Understand conceptually:

```text
Claude Code
    ↓ MCP
Blender MCP server/add-on
    ↓
Blender Python/API
    ↓
Scene operations
```

You do **not** need to learn MCP protocol internals deeply.

### Deliverable

Claude Code can communicate with Blender through the chosen MCP setup.

---

# 13. Step 8 — Blender MCP Smoke Test

Do not immediately ask Claude to create an entire animation.

Give it tiny, verifiable tasks.

Example sequence:

1. Inspect the current scene.
2. Add a cube.
3. Rename it.
4. Move it.
5. Add a material.
6. Add a light.
7. Add a camera.
8. Save a copy of the file.

After every operation, visually inspect Blender.

### Learn now

How to write prompts containing:

```text
Goal
Constraints
Existing scene state
Exact requested change
What must not change
How to verify completion
```

Example mindset:

> Modify only the camera. Do not change the character, materials, lighting or existing object positions.

### Deliverable

```text
blender/scenes/004-mcp-smoke-test.blend
```

### Failure rule

If Claude makes an unexpected change:

- do not just retry the exact same vague prompt,
- identify why the instruction was ambiguous,
- make the instruction more explicit,
- document the failure if it teaches something reusable.

---

# 14. Step 9 — Test AI 3D Asset Generation

Do not subscribe to a Pro service yet.

Candidate tools currently include:

- Meshy
- Tripo
- Hyper3D / Rodin

Useful starting URLs:

- https://www.meshy.ai/
- https://www.tripo3d.ai/
- https://hyper3d.ai/

Use free access / credits first where available.

### Character-design rule

For the first clip, choose a character that is:

- original,
- stylized,
- simple,
- easy to rig,
- clearly separated arms/legs,
- not wearing complicated clothing,
- not covered in hair/fur simulation,
- not photorealistic.

A simple humanoid/cartoon creature is preferable to a realistic person.

### Preferred input strategy

Where possible, create or generate a strong **2D character reference image first** and then test
image-to-3D.

This generally gives more visual control than repeatedly asking text-to-3D for a character.

### Generate the same concept in more than one tool

Do not compare completely different characters.

Use approximately the same:

- reference image,
- style,
- pose,
- requirements.

### Evaluate

For every model, inspect:

- silhouette,
- proportions,
- texture quality,
- mesh artifacts,
- separate limbs,
- hands/feet,
- topology,
- ability to import into Blender,
- scale,
- rigging suitability,
- deformation quality,
- export formats,
- cleanup required.

### Deliverable

Create:

```text
docs/experiments/3d-generator-comparison.md
```

Record:

```text
Tool:
Input:
Output:
Good:
Bad:
Blender import:
Rigging:
Cleanup required:
Would use again:
```

### Subscription decision

Do **not** buy a subscription yet unless one tool clearly saves meaningful time and produces
substantially better Blender-ready assets.

---

# 15. Step 10 — Import the Selected Character into Blender

Import one chosen model.

### Learn now

- Importing GLB / FBX or the selected format
- Object hierarchy
- Materials/textures
- Scale
- Rotation
- Applying transforms at a basic level
- Origins
- Basic normal/mesh inspection
- How to identify obviously broken geometry

### Use Claude/MCP

Ask Claude to:

- inspect object names,
- describe hierarchy,
- identify obvious scene/mesh issues,
- normalize naming,
- organize collections,
- help fix simple issues.

### Human responsibility

Rotate around the model yourself.

Look closely.

Do not accept the asset because it looks good from one camera angle.

### Deliverable

```text
blender/assets/character-v001.blend
```

---

# 16. Step 11 — Get the Character Rigged

Prefer an automated path for the first experiment.

Possible paths include:

```text
AI 3D service auto-rig
        ↓
export rigged model
        ↓
Blender
```

or:

```text
model
 ↓
Blender armature / auto-weight workflow
 ↓
agent assistance
```

For example, Meshy currently documents auto-rigging and animation workflows for generated/uploaded
characters. Other providers may offer similar capabilities.

Reference:

https://help.meshy.ai/en/articles/16231707-how-to-create-3d-animation-with-auto-rigging

### Learn now

Only the concepts:

- Skeleton / armature
- Bone
- Skinning
- Weight
- Pose Mode
- Animation clip/action
- Why joints deform badly

Do not attempt to become an expert rigger.

### Practical test

The character should perform at least:

- idle,
- simple walk or equivalent movement,
- one simple reaction/gesture.

### Human review

Check:

- shoulders,
- elbows,
- hips,
- knees,
- hands,
- feet.

If the mesh collapses badly, fix/regenerate before proceeding.

### Deliverable

```text
blender/assets/character-rigged-v001.blend
```

---

# 17. Step 12 — Build a Tiny Reusable Environment

Do not generate a giant forest/city/room.

Create a simple environment with:

- ground,
- background elements,
- one or two decorative assets,
- the interaction prop.

Use:

- Blender primitives,
- free/owned assets where appropriate,
- AI-generated 3D props if useful,
- Claude/MCP for placement.

### Learn now

- Collections
- Asset organization
- Scene scale
- Composition
- Keeping backgrounds visually simple

### Deliverable

```text
blender/assets/environment-v001.blend
```

---

# 18. Step 13 — Write the 15-Second Shot Specification

Before animating the final clip, define the shots as data.

Example:

```yaml
duration_seconds: 15
fps: 24

shots:
  - id: shot_001
    start: 0
    end: 5
    camera: wide
    action: character enters environment

  - id: shot_002
    start: 5
    end: 10
    camera: medium
    action: character notices prop and reacts

  - id: shot_003
    start: 10
    end: 15
    camera: close_or_medium
    action: character approaches/interacts and celebrates
```

Save it as:

```text
episode-specs/clip-001.yaml
```

### Use ChatGPT / Claude

AI can help:

- tighten the micro-story,
- plan timing,
- suggest camera framing,
- translate story actions into Blender actions.

### Human responsibility

You approve whether the action is actually understandable within 15 seconds.

---

# 19. Step 14 — Block the Entire Clip Before Polishing

This step is critical.

Do not polish Shot 1 for hours while Shots 2 and 3 do not exist.

Create a rough version of all 15 seconds.

Use:

- rough poses,
- basic animation clips,
- simple cameras,
- temporary lighting,
- no expensive final rendering.

### Learn now

- Blocking
- Key poses
- Action readability
- Shot timing
- Transitions
- Screen direction at a basic level

### Use Claude/MCP

Let Claude help:

- place the character,
- insert/reuse actions,
- set camera positions,
- create shot timing,
- build scene structure.

### Deliverable

A **15-second viewport/playblast/low-quality preview** where the complete story can be understood.

### Gate

Do not polish until the whole 15-second idea works in rough form.

---

# 20. Step 15 — Learn Animation Principles Through the Actual Problems

Now inspect the blocking.

Do not study all animation theory in advance.

Only learn the principles needed to fix visible problems.

Common problem → concept:

```text
Movement starts instantly        → anticipation / ease-in
Movement stops mechanically      → ease-out / follow-through
Character looks weightless       → timing / spacing / weight shift
Pose is hard to understand       → staging / silhouette
Movement feels stiff             → arcs / overlap
Reaction feels weak              → exaggeration / anticipation
```

### Use AI correctly

Bad request:

> Make it better.

Better request:

> The stop at frame 118 feels mechanical. Inspect the keyframes and suggest changes to spacing,
> body lean and follow-through without changing the shot duration.

### Human responsibility

You decide whether the revised movement actually feels better.

---

# 21. Step 16 — Polish Camera Work

Watch the clip with **no sound**.

Ask:

- Is it always clear where I should look?
- Does each shot have a purpose?
- Is the character large enough on screen?
- Are cuts confusing?
- Is the camera moving for a reason?

### Keep the camera simple

For the first clip, prefer:

- locked camera,
- slow push,
- simple pan,
- simple cut.

Avoid complex cinematic motion merely because Blender can do it.

### Deliverable

Camera timing is considered acceptable before final lighting/render work.

---

# 22. Step 17 — Polish Lighting and Materials

Return to the lighting knowledge from the earlier test.

Build one clear stylized lighting setup.

Priorities:

1. Character readability
2. Mood
3. Separation from background
4. Consistency across shots
5. Render efficiency

Do not chase photorealism.

### Use Claude/MCP

Claude can:

- create lighting rigs,
- reproduce lighting across shots,
- alter energy/position,
- inspect materials,
- help create reusable presets.

### Human responsibility

Choose the version that looks best.

---

# 23. Step 18 — Add Basic Audio

Keep audio simple.

Possible first-clip audio:

- footsteps,
- small discovery/reaction SFX,
- object interaction sound,
- light music/ambience.

Optional:

- one short narrator/TTS line.

Do not require character lip-sync yet.

### Learn now

- Audio timeline
- Dialogue/SFX/music balance
- Fade in/out
- Avoiding clipping
- Making sure the final rendered/exported video actually contains audible audio

Audio may be assembled with:

- Blender Video Sequencer,
- FFmpeg,
- or a simple scripted pipeline.

### Deliverable

Preview contains audible, intentional audio.

---

# 24. Step 19 — Render a Fast Full Preview

Before final rendering, produce the entire 15 seconds using fast settings.

Suggested philosophy:

```text
720p
fast render
full 15 seconds
```

Watch the rendered file outside Blender.

Do not rely only on viewport playback.

### Review checklist

#### Story

- Can the action be understood without explanation?
- Does anything feel rushed?
- Does anything feel too slow?

#### Character

- Model remains consistent
- No major deformation
- Feet do not obviously slide unless intentional
- Character does not intersect objects badly
- Movement feels reasonably intentional

#### Camera

- Subject stays framed
- Cuts make sense
- No accidental camera jumps

#### Lighting

- Character is readable
- No unexpectedly dark shots
- No distracting lighting changes

#### Asset quality

- No missing textures
- No broken materials
- No obvious geometry artifacts

#### Audio

- Audio exists
- SFX occur at appropriate moments
- Music/SFX are not painfully loud
- No unexpected silence caused by export mistakes

---

# 25. Step 20 — Diagnose, Fix, and Render Again

This is **part of the study plan**, not a failure of the study plan.

Expect:

```text
Preview v001
    ↓
problems
    ↓
fix
    ↓
Preview v002
    ↓
new / remaining problems
    ↓
fix
    ↓
Preview v003
```

Do not move forward merely because one render exists.

Create:

```text
docs/experiments/clip-001-review.md
```

For each issue record:

```text
Timestamp / frame:
Problem:
Likely cause:
Fix attempted:
Result:
Reusable lesson:
```

### Important efficiency rule

Regenerate only the broken shot/asset whenever possible.

Do not rebuild the entire project for a small error.

---

# 26. Step 21 — Final 15-Second Render

Only after the preview is satisfactory:

- set final resolution,
- verify output format,
- verify frame range,
- verify audio,
- verify render engine,
- render the final clip.

Suggested target:

```text
1920 × 1080
24 fps
15 seconds
```

The exact final codec/encoding can be handled by Blender/FFmpeg based on the pipeline chosen.

### Deliverable

```text
output/clip-001-final.mp4
```

Keep the final `.blend` file too.

---

# 27. Step 22 — Watch the Final File Like a Viewer

Do not review only inside Blender.

Watch the MP4:

- full screen,
- with sound,
- from beginning to end,
- without stopping the first time.

Then watch it again critically.

Ask:

> Would I personally be comfortable showing this to someone as evidence that the pipeline works?

If **no**, return to the relevant step.

There is no penalty for producing:

```text
v002
v003
v004
```

The project advances when confidence is earned.

---

# 28. Step 23 — Measure What Was Manual vs Automated

After the clip is complete, create:

```text
docs/retrospectives/clip-001-retrospective.md
```

Record every production stage.

Example:

| Stage | Manual | Claude/MCP | AI service | Notes |
|---|---:|---:|---:|---|
| Story | 20% | 80% | 0% | |
| Character concept | 20% | 30% | 50% | |
| 3D generation | 10% | 10% | 80% | |
| Blender setup | 30% | 70% | 0% | |
| Rigging | | | | |
| Animation | | | | |
| Camera | | | | |
| Lighting | | | | |
| Rendering | | | | |
| Audio | | | | |
| QA | | | | |

The exact percentages are subjective.

The purpose is to discover where manual effort is still concentrated.

---

# 29. Step 24 — Decide What to Automate Next

Now use the retrospective to choose automation work.

Good automation targets are operations that were:

- repetitive,
- slow,
- predictable,
- easy to verify.

Examples:

- scene initialization,
- folder/output setup,
- render settings,
- camera presets,
- lighting presets,
- asset importing,
- object naming,
- clip concatenation,
- audio assembly,
- technical QA.

Bad early automation targets:

- subjective acting quality,
- final creative judgment,
- automatically accepting generated assets,
- automatically uploading unreviewed content.

---

# 30. Step 25 — 3D Confidence Gate

Only after one or more satisfactory 15-second experiments, answer:

### Quality

- Can I produce a visually acceptable 3D clip?
- Can I tell why a bad animation looks bad?
- Can I fix common issues with AI assistance?

### Tooling

- Is Blender comfortable enough to inspect?
- Is Blender MCP reliable enough to save time?
- Can Claude Code operate the workflow without constantly damaging unrelated scene elements?

### Assets

- Can AI-generated 3D models become usable Blender assets?
- Does one provider clearly outperform the others?
- Is a paid subscription now justified?

### Effort

- How much manual work did 15 seconds require?
- Which tasks will become cheaper through reuse?

### Confidence

- Do I feel ready to create another 15-second clip without starting from zero?

If the answer is broadly **yes**, continue with 3D.

If the answer is **no**, do not blindly push into 30–60 second 3D content.

Diagnose the bottleneck.

If necessary, run a comparable **2D/2.5D experiment** and compare:

- visual quality,
- effort,
- controllability,
- automation,
- production time.

The visual format should be chosen based on evidence rather than attachment to a tool.

---

# 31. What to Study Only After This 15-Second Milestone

Do not make these prerequisites for the first clip.

Learn them later as needed:

- Advanced modeling
- Manual retopology
- Advanced rigging
- Weight-painting mastery
- Facial rigs
- Phoneme/viseme lip sync
- Multi-character interaction
- Advanced cinematography
- Advanced lighting
- Character cloth/hair
- Geometry Nodes
- Advanced compositing
- Physics simulation
- Motion capture
- Long-form editing
- Render farms
- Cloud rendering
- Full asset-management systems

---

# 32. Skills You Should Have After Completing This Plan

You should **not** expect to be an expert animator.

You should be able to:

### Blender

- Navigate Blender without feeling lost
- Inspect a scene
- Move/rotate/scale objects
- Understand object hierarchy
- Inspect materials
- Understand the timeline
- Inspect keyframes
- Position a camera
- Adjust lights
- Configure a basic render
- Import a 3D asset
- Inspect a rig
- Render a clip

### Animation

- Understand what a keyframe is
- Recognize basic timing/spacing problems
- Recognize obviously robotic motion
- Understand blocking
- Understand why anticipation/easing/follow-through matter

### AI / Automation

- Connect Claude Code to Blender through an MCP workflow
- Give narrow, testable scene instructions
- Inspect AI-created Blender changes
- Detect when the agent changed something it should not have
- Iterate on prompts/instructions
- Decide which operations should become automated

### Asset Pipeline

- Generate/test a 3D asset with AI tools
- Import it into Blender
- Evaluate whether it is actually usable
- Reject an attractive-but-broken model
- Understand basic rigging requirements

### Directing

- Distinguish wide/medium/close shots
- Recognize bad framing
- Judge basic lighting readability
- Decide whether a 15-second action communicates clearly

---

# 33. Claude Code / Blender MCP Prompting Pattern

Prefer structured tasks.

Example:

```text
GOAL:
Create the wide establishing shot for clip-001.

CURRENT STATE:
- Character already exists in collection CHARACTERS.
- Environment exists in ENVIRONMENT.
- Prop exists and must not move.
- Existing materials must not be changed.

TASK:
- Position the character at the left edge of the playable area.
- Create a camera for a readable wide shot.
- Add only the keyframes required for the character to walk toward center.
- Duration: frames 1–120 at 24 fps.

CONSTRAINTS:
- Do not modify mesh geometry.
- Do not replace materials.
- Do not delete existing objects.
- Do not change render settings.

VERIFY:
- Report which objects/actions/keyframes were created or changed.
```

This is much better than:

> Make the first scene look cinematic.

Use broad creative prompts with ChatGPT/Claude during planning.

Use narrow engineering prompts when modifying Blender.

---

# 34. Experiment Log Template

For every important experiment:

```markdown
# Experiment: <name>

## Goal

## Input / Prompt

## Tool / Version

## What happened

## What worked

## What failed

## Root cause

## Fix

## Result after fix

## Reusable lesson

## Keep / reject
```

The repository should become a memory system for future AI agents.

Do not let valuable lessons remain only in chat history.

---

# 35. Suggested Definition of Done for the 15-Second Milestone

The milestone is complete only when all of these are true:

- [ ] A complete 15-second MP4 exists.
- [ ] The clip uses an original 3D character.
- [ ] The character is rigged or otherwise meaningfully animated.
- [ ] The clip has a simple readable beginning/action/reaction.
- [ ] At least two intentional camera compositions are used.
- [ ] Lighting is intentional and readable.
- [ ] Audio is present if included in the final creative plan.
- [ ] No major missing textures/materials.
- [ ] No severe rig deformation.
- [ ] No accidental camera jumps.
- [ ] The clip has been watched outside Blender.
- [ ] Problems from earlier iterations are documented.
- [ ] At least one repeated Blender operation has been performed through Claude/MCP.
- [ ] The project owner understands enough to explain how the scene was produced.
- [ ] The project owner is personally satisfied enough to move to the next experiment.
- [ ] A retrospective identifies the next automation priorities.

---

# 36. Current Tool Notes — September 2026

These notes are intentionally small because tool capabilities will change.

## Blender

Blender 5.2 is an LTS release and is a good base for the learning project.

Official release page:

https://www.blender.org/releases/5-2/

## Blender MCP

Community BlenderMCP project:

https://github.com/MCPBlender/blender-mcp

Treat it as a fast-moving dependency.
Always check current documentation and compatibility before setup changes.

## Meshy

Meshy currently provides workflows around:

- Text/Image to 3D
- Texturing
- Auto rigging
- Animation
- Export to Blender-compatible workflows

References:

https://www.meshy.ai/

https://help.meshy.ai/en/articles/16231707-how-to-create-3d-animation-with-auto-rigging

## Tripo

Candidate AI 3D provider:

https://www.tripo3d.ai/

## Hyper3D / Rodin

Candidate AI 3D provider:

https://hyper3d.ai/

Do not select a paid provider based only on generated showcase images.

The relevant question is:

> **How much time does this tool save in producing a reusable, riggable, animatable Blender asset?**

---

# 37. Final Study Principle

The project owner is an experienced software engineer, not an experienced animator.

Use that advantage.

Do not try to compete with traditional animators by manually performing every operation.

Instead:

```text
Learn enough to understand the system
             ↓
Build something small
             ↓
Judge the output
             ↓
Use AI to accelerate implementation
             ↓
Automate repeatable work
             ↓
Keep human control over quality
             ↓
Iterate until satisfied
```

The 15-second clip is not the final objective.

It is the first proof that this approach can become a scalable animation-production workflow.
