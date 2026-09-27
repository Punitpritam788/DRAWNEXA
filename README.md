# 🧬 DRAWNEXA

### **DRAW YOUR WEAPON. IT LEARNS YOU USING AI.**

<p align="center"><img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"><img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"><img src="https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white"><img src="https://img.shields.io/badge/WebGL-990000?style=for-the-badge&logo=webgl&logoColor=white"><img src="https://img.shields.io/badge/GLSL-5C2D91?style=for-the-badge"><img src="https://img.shields.io/badge/Canvas_API-000000?style=for-the-badge&logo=html5&logoColor=white"><img src="https://img.shields.io/badge/Web_Audio_API-111111?style=for-the-badge"><img src="https://img.shields.io/badge/Pointer_Events-0F6CBD?style=for-the-badge"><img src="https://img.shields.io/badge/Touch_Events-0F6CBD?style=for-the-badge"><img src="https://img.shields.io/badge/Web_APIs-4285F4?style=for-the-badge"><img src="https://img.shields.io/badge/Google_Fonts-4285F4?style=for-the-badge&logo=google&logoColor=white"><img src="https://img.shields.io/badge/cdnjs-0A0A0A?style=for-the-badge&logo=cdnjs&logoColor=white"><img src="https://img.shields.io/badge/AI%2FML-FF2F6E?style=for-the-badge"><img src="https://img.shields.io/badge/RBF_Classifier-A06BFF?style=for-the-badge"><img src="https://img.shields.io/badge/N--gram_Prediction-39E0FF?style=for-the-badge"><img src="https://img.shields.io/badge/Procedural_Generation-6BFF9E?style=for-the-badge"><img src="https://img.shields.io/badge/Single--File_Game-FFB03A?style=for-the-badge"></p>

<p align="center">
  <strong>DRAW IT. WIELD IT. LET IT LEARN YOU.</strong>
</p>

---

## 🧠 What is DRAWNEXA?

**DRAWNEXA** is a browser-based experimental action arena built around a simple idea:

> **Your weapon comes from your drawing.
> Your combat creates a pattern.
> The AI learns that pattern.
> Then it tries to use your habits against you.**

Instead of selecting a predefined weapon, you draw one.

The Forge analyzes the geometry and movement of your drawing and transforms it into a procedural 3D weapon with combat statistics, elemental properties, forms, and perks.

Then you enter the arena.

Every attack, movement, dash, guard, weapon swap, sigil, seal, and technique can become part of an adaptive prediction system.

The more predictable your behaviour becomes, the more accurately the arena can react.

### **The objective is not only to survive.**

### **It is to become difficult to understand.**

---

# ⚔️ THE CORE LOOP

```text
DRAW
  ↓
FORGE
  ↓
FIGHT
  ↓
AI LEARNS
  ↓
AI PREDICTS
  ↓
CHANGE YOUR PATTERN
  ↓
BREAK THE PREDICTION
  ↓
SURVIVE
```

DRAWNEXA connects procedural generation, adaptive behaviour, and action combat into one loop.

---

# 🎨 DRAW YOUR WEAPON

The Forge is the first major system.

Your drawing is treated as gameplay input rather than decoration.

The system extracts geometric and motion information including:

```text
Length
Elongation
Straightness
Turning
Density
Spikes
Closure
Symmetry
Coverage
Self-Intersection
Drawing Speed
Jitter
Stroke Count
```

That information influences the weapon that gets created.

---

# ⚒️ PROCEDURAL WEAPON FORGE

The drawing is processed by the game's weapon classification and synthesis systems.

Weapons can be associated with elemental identities such as:

```text
EMBER
FROST
VOLT
VOID
VERDANT
RADIANT
```

Generated weapon statistics include:

```text
Impact
Swing Speed
Reach
Arc Width
Critical Edge
Sigil Power
```

The weapon is then represented as an actual 3D object inside the Three.js scene.

---

# 🤖 AI-DRIVEN WEAPON CLASSIFICATION

DRAWNEXA combines a handcrafted geometry interpretation with a local classifier and a learned weapon preference system.

The classifier uses a feature vector derived from the player's drawing and evaluates candidate weapon archetypes.

The current implementation uses a local **prototype/RBF-style classifier** rather than an external AI API.

```text
DRAWING
   ↓
FEATURE EXTRACTION
   ↓
GEOMETRY ANALYSIS
   ↓
RBF CLASSIFIER
   ↓
WEAPON ARCHETYPE
   ↓
SMITH LEARNING
   ↓
FINAL WEAPON
```

The project therefore uses AI-style decision systems directly inside the browser instead of requiring a remote inference service.

---

# 🧬 THE SMITH

The Forge contains a learned system called **Smith**.

Smith can learn from the weapons you actually choose and use during the session.

Conceptually:

```text
YOUR DRAWING
      ↓
SMITH PREDICTION
      ↓
YOU CHOOSE A WEAPON
      ↓
GAME OBSERVES THE CHOICE
      ↓
SMITH LEARNS
      ↓
FUTURE FORGE RESULTS CHANGE
```

This creates an evolving relationship between the player and the Forge.

---

# 🔀 MULTI-FORM WEAPONS

Weapons are not limited to a single attack style.

A weapon can contain multiple forms that change how it behaves.

Forms can support mechanics such as:

```text
Melee
Charge
Shot
Beam
Zone
Field
Throw
Summon
Guard
Blink
```

Weapon switching is also visible to the adaptive combat model, meaning your choice of form can itself become part of your behavioural fingerprint.

---

# 👁️ THE ADAPTIVE MIND

This is the central AI mechanic of DRAWNEXA.

Player actions are transformed into a stream of behavioural tokens.

Examples include:

```text
ADVANCE
RETREAT
LEFT
RIGHT
LIGHT
HEAVY
DASH
GUARD
SIGIL
SEAL
SWAP
SHOOT
THROW
BEAM
ZONE
SUMMON
```

The system uses a **back-off n-gram prediction model** to learn action sequences.

For example:

```text
LIGHT → DASH
LIGHT → DASH → HEAVY
```

The model tracks previous behaviour and tries to estimate what you are likely to do next.

---

# 🧠 AI PREDICTION

The game continuously exposes the prediction process through its HUD.

```text
Predicted Next Move
Prediction Hit Rate
Surprise Streak
Gnosis
```

The idea is simple:

```text
REPEATED BEHAVIOUR
       ↓
MORE INFORMATION
       ↓
BETTER PREDICTION
       ↓
MORE DANGEROUS COUNTERS
```

You can fight the model by changing your behaviour.

---

# 🧬 GNOSIS

**Gnosis** represents how strongly the system understands your current behavioural pattern.

The game treats predictability as a gameplay mechanic instead of hiding the AI behind the scenes.

```text
LOW GNOSIS
   ↓
LESS UNDERSTANDING

HIGH GNOSIS
   ↓
MORE UNDERSTANDING
   ↓
GREATER PRESSURE
```

The HUD makes that relationship visible while you play.

---

# 💥 BREAK THE MODEL

The prediction system can fail.

When enough predictions fail, the boss can enter a **Breach** state.

Conceptually:

```text
PLAYER CHANGES PATTERN
        ↓
PREDICTIONS FAIL
        ↓
SURPRISE STREAK
        ↓
BREACH
        ↓
BOSS VULNERABILITY
        ↓
PLAYER CAPITALIZES
```

The player therefore has a second objective beyond dealing damage:

### **Make the AI wrong.**

---

# 👑 NULLIARCH

The game's current central boss is **NULLIARCH**:

> *that which has already seen this*

NULLIARCH is designed around increasingly advanced prediction phases.

```text
PHASE I
OBSERVE

PHASE II
MIRROR

PHASE III
PREEMPT

PHASE IV
RECURSION
```

As the boss progresses, it gains access to more aggressive prediction-driven behaviour.

---

# 🎯 PREDICTION-BASED COUNTERS

NULLIARCH can select counters according to what it expects the player to do.

Examples:

```text
ATTACK PREDICTION
→ PARRY / SIDESTEP

DASH PREDICTION
→ LEAD THE MOVEMENT

GUARD PREDICTION
→ GUARD BREAK

RETREAT PREDICTION
→ CLOSE DISTANCE

ADVANCE PREDICTION
→ AREA CONTROL

SIGIL PREDICTION
→ WARD
```

This creates the game's defining combat relationship:

```text
YOU ACT
  ↓
AI LEARNS
  ↓
AI PREDICTS
  ↓
AI COUNTERS
  ↓
YOU ADAPT
  ↓
AI LEARNS AGAIN
```

---

# 🌀 GESTURE-BASED SIGILS

DRAWNEXA includes a gesture recognition system.

Hold the sigil control and draw a shape.

The gesture is normalized and compared with available patterns.

Recognized techniques include:

```text
ARC
NOVA
CHAIN
SIEGE
ASCENT
PLUNGE
VORTEX
LANCE
```

This turns drawing into a real-time combat input.

---

# 🐍 HAND SEALS

A separate gesture system allows sequences of hand signs to become techniques.

Available signs include:

```text
RAT
OX
TIGER
HARE
SNAKE
HORSE
BOAR
BIRD
```

Different combinations produce different techniques.

The boss can also learn recurring seal patterns.

---

# ☠️ NULL EDICT

One of the more unusual abilities is **NULL EDICT**.

Instead of functioning only as a conventional attack, it interacts with the boss's learned behavioural state.

It can:

```text
Disrupt recent learned sequences
Reduce prediction pressure
Create an opening
Stagger the boss
Deal damage
```

The ability therefore connects the game's combat system directly to its adaptive model.

---

# 🤖 AUTOPILOT

DRAWNEXA includes an experimental AI Wielder / Autopilot mode.

The Wielder evaluates possible actions using factors such as:

```text
Combat usefulness
Distance
Threat
Weapon state
Prediction pressure
```

The system also considers how strongly the current model expects an action.

Conceptually:

```text
COMBAT VALUE
+
POSITION
+
THREAT
+
WEAPON STATE
-
PREDICTABILITY
=
ACTION
```

This allows the Wielder to play against the prediction model rather than simply following a fixed attack script.

---

# 👻 PHANTOM WIELDER

A Phantom ally can use the same general decision architecture.

```text
                 WIELDER
                    │
          ┌─────────┴─────────┐
          ↓                   ↓
      AUTOPILOT           PHANTOM
```

The same style of decision-making can therefore control different combat bodies.

---

# 📈 STYLE

The Style system rewards combat variety.

Repeatedly performing the same action becomes less effective than changing your behaviour.

```text
VARIETY
   ↓
STYLE
   ↓
COMBAT OUTPUT
```

This creates another connection between combat performance and unpredictability.

---

# 🌑 RUN STRUCTURE

A typical run follows a descent through increasingly difficult encounters.

```text
FORGE
  ↓
WAVE 1
  ↓
WAVE 2
  ↓
WAVE 3
  ↓
WAVE 4
  ↓
NULLIARCH
```

Between waves, the player can access the Forge and modify the build.

---

# 🧪 BOONS

Runs can contain temporary modifiers such as:

```text
Whetted
Quickened
Deep Well
Stubborn
Third Form
Echoing
Bound Phantom
Swift Seals
Flourish
Feast
```

These provide additional variation during a run.

---

# 📱 MOBILE CONTROLS

DRAWNEXA includes touch-oriented combat controls.

| Touch Input       | Action     |
| ----------------- | ---------- |
| Left half + drag  | Move       |
| Right half + drag | Look       |
| Right half + tap  | Attack     |
| Two fingers       | Draw Sigil |
| Three fingers     | Hand Seals |

The source also includes touch-specific handling and dynamic touch input for the combat systems.

---

# 🎮 DESKTOP CONTROLS

| Input        | Action             |
| ------------ | ------------------ |
| `W A S D`    | Move               |
| `Mouse`      | Look               |
| `Left Click` | Attack             |
| `Space`      | Dash               |
| `Q / E`      | Guard              |
| `Shift`      | Draw Sigil         |
| `F`          | Hand Seals         |
| `R / 1 2 3`  | Change Weapon Form |
| `P`          | Autopilot          |
| `Tab`        | Reforge            |
| `Esc`        | Pause              |

---

# 🎨 RENDERING PIPELINE

The game uses Three.js with a custom WebGL rendering pipeline.

The current renderer includes:

```text
Three.js
WebGLRenderer
WebGL Render Targets
Custom Shader Materials
GLSL Shaders
Bloom Extraction
Blur Passes
Composite Pass
Chromatic Aberration
Vignette
Film / Noise
Time-Dilation Effects
Procedural Particles
Combat VFX
```

The source creates multiple render targets and custom shader passes for brightness extraction, blur, and compositing.

---

# 🖌️ CANVAS SYSTEMS

The project uses browser Canvas APIs for several interactions.

The Forge uses a 2D canvas for:

```text
Drawing
Stroke visualization
Weapon previews
Gesture feedback
```

The game also uses canvas-backed visual systems for HUD-related rendering.

The Forge explicitly obtains a 2D canvas context to render the player's strokes.

---

# 🔊 AUDIO

The game includes browser-native sound generation using the **Web Audio API**.

Audio is created directly from browser audio nodes rather than loading a large external sound library.

This keeps the prototype lightweight and self-contained.

---

# 🧩 BROWSER TECHNOLOGIES

DRAWNEXA makes use of several browser APIs directly:

```text
Canvas API
Pointer Events
Touch Events
Keyboard Events
Mouse Events
Wheel Events
Pointer Lock
Web Audio API
requestAnimationFrame
WebGL
Responsive viewport APIs
```

---

# ⚡ PERFORMANCE

The project is designed around a lightweight browser-first architecture.

The source uses:

```text
Delta-time simulation
Object pooling
Data-oriented entities
Explicit state machines
Render targets
Reduced-resolution bloom passes
Device-pixel-ratio limiting
```

This allows a relatively complex combat scene to remain inside a single HTML document.

---

# 🗺️ GAME ARCHITECTURE

```text
                         DRAWNEXA
                            │
          ┌─────────────────┼─────────────────┐
          ↓                 ↓                 ↓
        FORGE             COMBAT            BOSS
          │                 │                 │
          ↓                 ↓                 ↓
   Weapon Classifier    Adaptive Mind      Counters
          │                 │                 │
          ↓                 ↓                 ↓
        SMITH          N-GRAM MODEL       NULLIARCH
          │                 │                 │
          └─────────────────┼─────────────────┘
                            ↓
                          PLAYER
                            ↓
                    THREE.JS / WEBGL
```

The project source explicitly describes its architecture around delta-time updates, data-oriented entities, explicit state machines, and object pools.

---

# 🧠 AI ARCHITECTURE

The project's adaptive behaviour can be viewed as two connected systems.

### Weapon Intelligence

```text
DRAWING
 ↓
FEATURES
 ↓
CLASSIFIER
 ↓
SMITH
 ↓
WEAPON
```

### Combat Intelligence

```text
PLAYER ACTIONS
 ↓
SEQUENCE MODEL
 ↓
PREDICTION
 ↓
BOSS COUNTER
 ↓
PLAYER ADAPTATION
```

Together they create:

```text
DRAW
 ↓
WEAPON
 ↓
COMBAT
 ↓
LEARNING
 ↓
PREDICTION
 ↓
ADAPTATION
```

---

# 📁 PROJECT STRUCTURE

The current prototype is intentionally kept inside one main HTML file.

```text
drawnexa/
│
├── index.html
└── README.md
```

This single-file architecture makes the prototype easy to:

* Experiment with
* Share
* Modify
* Deploy
* Run in a browser

---

# 🚀 RUN LOCALLY

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/drawnexa.git
cd drawnexa
```

Then start a local server:

```bash
python -m http.server
```

Open:

```text
http://localhost:8000
```

---

# 🌐 LIVE DEMO

Add your GitHub Pages URL here:

```text
https://YOUR-USERNAME.github.io/drawnexa/
```

---

# 🧪 EXPERIMENTAL STATUS

DRAWNEXA is an experimental browser-game project focused on exploring:

```text
PROCEDURAL GENERATION
+
PLAYER BEHAVIOUR
+
AI PREDICTION
+
ADAPTIVE COMBAT
+
GESTURE INPUT
```

The project is intentionally experimental, and its gameplay systems can continue evolving.

---

# 🔮 FUTURE DEVELOPMENT

Possible directions include:

```text
Persistent AI memory
More weapon classes
More adaptive enemies
Additional bosses
More gesture techniques
Procedural arenas
Replay analysis
Behaviour visualization
Improved mobile controls
More advanced prediction models
Expanded weapon evolution
```

---

# 🧠 WHY DRAWNEXA?

Most action games ask:

> **Can you react fast enough?**

DRAWNEXA asks:

> **Can you stop the enemy from understanding how you react?**

Your drawing creates your weapon.

Your combat creates your pattern.

Your pattern becomes data.

The AI learns the data.

Then you have to change.

---

# ⚔️ DRAWNEXA

### **DRAW YOUR WEAPON. IT LEARNS YOU USING AI.**

<p align="center">
<strong>DRAW IT.</strong><br>
<strong>WIELD IT.</strong><br>
<strong>BREAK THE PATTERN.</strong>
</p>

<p align="center">
<em>The arena remembers your habits.</em>
</p>
