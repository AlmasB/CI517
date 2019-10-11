---

### Lecture 6 - Physics Subsystem

> "Part 1. Particle Physics" - Ian Millington

- Vector maths
- Game object interaction
- Physics rules
- Approximations / performance


---

#### Last Week Recap

- ECS and game world

---

#### Objective

- Mainly to give you a bit of taste for physics breadth in game dev
- Don't worry if you don't understand *all* of it
- The engine takes care of most things for us ... oh, wait a minute!

---

#### Game Dev Maths

- Fundamental to the field
- Ranges from basic to very complex
- Important to know the difference between what, why and how

---

#### 2D Maths

- Luckily, not very complex
- Transtive skills from / to UI design

---

#### Point

- Ordered pair: (x, y)
- Location / position in space
- Extendible to n dimensions
- Crucial to most games

---

#### Game World vs Screen

- Positive Y axis
- Not always 1 to 1 mapping
- Visible area (viewport into _infinite_ world)

---

#### Point (Use Case)

- Distance to things
- Relative position to things

---

#### Vector

- Ordered pair: (x, y) - yes, same as point
- Displacement with direction and length (magnitude)
- Describes velocity, acceleration, direction, etc.
- Extendible to n dimensions

---

#### Vector (Use Case)

- Distance to things (recall point)
- Direction of an object
- Force / speed via length
- Angle representation

---

#### Transformations (Translate)

- Means move
- Apply over time to create a moving animation
- Apply with acceleration to simulate movement

---

#### Transformations (Scale)

- Means growing or shrinking
- Apply over time to create an animation
- Changes object dimensions (note for collisions)

---

#### Transformations (Rotate)

- Means changing angle
- Apply over time to create a spinning animation
- Changes occupying space (note for collisions)

---

#### Applying Concepts

- Demo of a moving object
- Demo with acceleration
- Demo with gravity

---

#### Representing Game Objects

- Objects have dimensions, e.g. width, height, depth
- Objects have an _anchor_ (position)

---

#### Game Physics

- Speed matters (functions get called many times in one frame)
- Need not be precise, just good enough
- Can utilise game specifics (e.g. platformer, tile based)

---

#### Collision Detection Phases

- Broad phase
- Narrow phase

---

#### AABB (Axis Aligned Bounding Box)

- Very fast
- Very easy to implement
- Extends to n dimensions
- Works in cases without rotations

---

#### Acitivity

Identify which part of the [FXGL](https://github.com/AlmasB/FXGL) code base performs AABB.

---

#### SAT (Separating Axis Theorem)

- Slower
- Easy to implement
- Extends to n dimensions
- Works in cases with rotations

---

#### Acitivity

Identify which part of the [FXGL](https://github.com/AlmasB/FXGL) code base performs SAT.

---

#### Grids

- Fast
- Easy to implement
- Extends to n dimensions
- Works in tile / grid based cases, as broad phase

---

#### Space Partioning (e.g. Quadtree)

- Speed depends on use case
- Harder to get "right"
- Extends to n dimensions
- Works only as broad phase

---

#### Pixel-level / Bitmap

- Very slow
- Relatively easy to implement
- Works only in 2D
- Works in cases with rotations

---

#### Continuous / Sweeping

- Slower
- Harder to get "right"
- Extends to n dimensions
- Mainly for fast moving objects or simulations

---

#### Special Cases

- Circle-circle collision
- Polygon clipping

---

#### Applying Concepts

- Demo AABB
- Demo SAT

---

#### High-level Usage

Old school

```
if (obj1.collidesWith(obj2)) {
    // do smth
}
```

Modern

```
addHandler(type1, type2, (obj1, obj2) -> {
    // do smth
})
```

---

#### Conclusion

- Physics, same as maths, very important for games
- Don't have to get exactly right
- Cheap and cheerful algorithms exist


---

#### Tutorial

On StudentCentral, Use collision callbacks in your game