---

### Lecture 5 - Entity-Component System

> "Either make it so simple that there are obviously no deficiencies or make it so complicated that there are no obvious deficiencies." - (Tony Hoare, adapted)

- How to represent game objects and store them
- Logic behind each game object
- Managing a large number of game objects

---

#### Last Week Recap

- Event systems 

---

#### Game Objects and World

To start us off:

- What is a game object?
- What is a game world?
- Why do we need these concepts? 

---

#### ECS - Entity

- **Everything** is an entity
- Without extra information an entity is like an object without fields and methods
- The most primitive entity is just an `int`

---

#### ECS - Component

- Holds data & behaviour
- Defines an entity
- Self-contained, but may depend on other components (e.g. view depends on position)

---

#### ECS - System

- Holds a collection of components of the same type
- Performs bulk operations

---

#### ECS - Example Component


```
class MoveableComponent extends Component {

    constructor() {
        this.x = 0.0;
        this.y = 0.0;
    }
}

```

---

#### ECS - Example Entity


```
let entity = new Entity();

// now entity knows about its position and that it can move
entity.addComponent(new MoveableComponent());
```

---

#### ECS - Real-world Examples

- TODO: eg Unreal Engine
- TODO: eg Unity

---

#### ECS - Activity

Design a simple game of any genre that is built using the ECS model.

---

#### Advantages

- Composition over Inheritance (no inheritance hell)
- Can mix components easily
- Scaling and management (clearly defined dependency) 

---

#### Disadvantages

- Redundant iteration (recall collision checks)
- More verbose API:
```
entity.getComponent(MoveableComponentType).velocity = new Vec2();
```
- Need to manage communication between components

---

#### ECS - Updating

Every component defines an update:


```
class MoveableComponent extends Component {

    constructor(velocity) {
        this.x = 0.0;
        this.y = 0.0;
        this.velocity = velocity;
    }
    
    update(tpf) {
        x += velocity.x * tpf;
        y += velocity.y * tpf;
    }
}

```

---

#### ECS - Example Update


```
let entity = new Entity();
entity.addComponent(new MoveableComponent(new Vec2(100, 50)));
```

Whenever `update()` is called, `entity` moves.
Each update is called by the corresponding System,
but who controls the Systems?

---

#### ECS - Game World

- Collection of Systems (which are a collection of entities / components)
- _Can_ be a collection of entities based on its architecture (e.g. Entity Component Control mechanism)
- Responsible for entity updates and queries

---

#### ECS - Game World - Activity

Design a (simple) open world, such as the TES5 Skyrim world with its associated game objects. Attempt to use the ECS model.

---

#### ECS - Game World - Explore

Let's consider existing ECS implementations in game engines.


---

#### Game World - Queries

- By type
- By layer
- By position
- Random
- etc.

---

#### Conclusion

- ECS - a powerful pattern in game dev
- Entities - just generic objects
- Components - add "flavour" to entities
- Systems - update components


---

#### Tutorial

On StudentCentral