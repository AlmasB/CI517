---

### Lecture 3 - Game Engine Architecture

> "If builders built buildings the way programmers wrote programs, then the first woodpecker that came along would destroy civilization." - Gerald Weinberg

- Mapping a game engine architecture against a game architecture
- What subsystems exist and what they do

---

#### Last Week Recap

- C++

---

#### Game Engines

- Different view / workflows, 
- Architecture-wise, if we look generally, it is similar


---

#### Game Engines (Unity)

TODO: image

---

#### Game Engines (Unreal)

TODO: image

---

#### Game Engines (Godot)

TODO: image

---

#### Game Engines (FXGL)

TODO: image


---

#### Game Engine Architecture

other images arch from game engine arch book


---

#### Game Architecture

- Start
- Init
- Loop: Input, Update, Render
- Destroy
- Exit

---

#### Game Engine Architecture

- Start
- Init (graphics, audio, background threads, asset manager, event system, etc.)
- Loop: (update engine timer)
- Destroy (cleanup)
- Exit


---

#### Game Architecture (Start)

- Sanity check the system, e.g. graphics, audio, window
- Take control from the environment
- What is the entry point of any piece of software?


---

#### Game Architecture (Init)

- Load assets and data
- Show load screen or main menu

---

#### Game World Subsystem

- Manage (store, update) many game objects simultaneously
- Allow queries

---

#### Physics Subsystem

- Compute valid positions of objects
- Simulate (fake) physics
- Detect collisions


---

#### Graphics Subsystem

- Draws objects (entities + UI) to the screen
- Computes complex post-processing effects
- Graphics system stack (hardware -> ... -> high-level API)

---

#### Activity

Let's explore existing open-source game engines:
1. Find a repo on GitHub with game engine source code
2. Identify their versions of "Game World", "Main Loop", "Render" and "Physics Tick".

---

#### Event Subsystem

- Communication between subsystems
- Manage and dispatch in-game events, expose them to users

---

#### Audio Subsystem

- 3D positional sound
- Ambient effects
- Ability to control properties of audio being played (volume, rate)

---

#### AI Subsystem

- Provides behaviour to game objects
- A set of pathfinding and search algorithms
- Works as a human replacement in single player mode

---

#### UI Subsystem

- Manage the UI view of the game
- Provide simple objects for manipulation
- Complex animations with interpolations
- Front-end validation

---

#### Asset (Resource) Manager Subsystem

- (Pre)load and store assets in an efficient way
- Allow easy access to stored assets

---

#### Profiling / Debugging Subsystem

- Manage crashes gracefully
- Provide important data to developers (stacktrace, performance)
- Attempt to identify what went wrong

---

#### Networking Subsystem

- Updates, DLC, one-time events, notifications, friends list
- Multiplayer
- Cloud saves

---

#### Maths Subsystem

- Simplify domain code by reusing existing functions
- Handle combat / gameplay specifics

---

#### Platform Subsystem

- Identify platform specifics (OS, capabilities)
- Map engine code to appropriate back-end

---

#### Scripting Subsystem

- Allow easy engine extensions (user content)
- Reduces compilation times


---

#### Activity

Consider a game of your choice (examples: Minecraft, TESV Skyrim, etc.) and in pseudo code / script
construct a plugin that implements a new gameplay element.

---

#### Conclusion

- One architecture to rule them all, many actual implementations
- This is only the surface -- there are many more subsystems. Feel free to explore!

---

#### Tutorial

On StudentCentral