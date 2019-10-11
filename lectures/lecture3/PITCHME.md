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

TODO: UE4, Unity, others


Different view / workflows, architecture-wise, if we look generally, it is similar

TODO: images if possible?

other images arch from game engine arch book


---

#### FXGL Architecture

TODO: images


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
- Loop: (update engine timer
- Destroy (cleanup)
- Exit


---

#### Game Architecture (Start)

- Sanity check the system, e.g. graphics, audio, window
- Take control from the environment
- What is the entry point of any piece of software?


---

#### Game Architecture (Init)

- TODO




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

#### AI Subsystem

- Provides behaviour to game objects
- A set of pathfinding and search algorithms
- Works as a human replacement in single player mode





---

#### Conclusion

- One architecture to rule them all, many actual implementations

---

#### Tutorial

On StudentCentral