---

### Lecture 8 - AI subsystem

> "A computer lets you make more mistakes faster than any invention in human history." - Mitch Radcliffe

- dd
- dd

---

#### Last Week Recap

- Graphics and Audio

---

#### Pathfinding

- Used by AI agents (entities) to calculate a valid route to player (entity)
- Usually game world is converted to grid / graph data structure
- A* algorithm is popular for its performance and result

---

#### Graphs

- A collection of nodes and edges
- Nodes represent rooms / tiles / a single movement block
- Edges represent the existence of a path between 2 rooms / tiles / blocks

---

#### Game World -> Graph

```
let graph = new Graph();

world.tiles.forEach(tile => graph.addNode(node(tile)));

graph.nodes.forEachPair(node1, node2 => 
    if (node1.tile can go to node2.tile) {
        graph.addEdge(node1, node2);
    }
);
```

The result is a _connected_ graph, assuming you can get to any tile from any other tile.

---

#### Apply Algorithms

We have converted a specific problem to a generic problem.
We can now apply existing algorithms to solve our problem.

---

#### Apply A*

```
let path = A*.apply(graph, startTile, endTile);
```

`path` contains a list of tiles, which is the shortest route from `startTile` to `endTile`.


---

#### Activity

Examine the provided code base regarding maze generation. How would you solve the problem of finding a path from the start to the end of the maze?

---

#### Various AI Behaviour Types

- FSM (Finite State Machine)
- BTrees (Behaviour Trees)
- GOAP (Goal Oriented Action Planning)
- Squad Tactics

---

#### FSM

- Can only be in 1 state at a time
- Works for most simple AI

---

#### BTrees

- Can define complex behaviour from simple actions
- It's like the ECS pattern of AI (can mix and match tree elements)
- Flexible

---

#### GOAP (F.E.A.R)

- Define actions (like BTree) but do not specify order, i.e. dynamic
- Use game world queries to determine its state
- Build a chain of actions that will lead AI to the "best" world state

---

#### Squad AI

- Game world queries (identify valid position, filter out rest based on e.g. threat)
- Squad "center of mass" (dynamic)

---

#### AI Behaviour

- Can be implemented via `AIComponent`
- Different per each game context (e.g. Fallout 4 vs Assassin's Creed)

---

#### Activity

Design and implement a two-state FSM for your player.

---

#### Conclusion

- Many AI algorithms already exist
- Find a way to translate your problem to one that's been solved
- Important to "contain" AI, as it can overwhelm the player

---

#### Tutorial

On StudentCentral