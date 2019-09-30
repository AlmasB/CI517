---

### Lecture 4 - Application Framework

> "Before software can be reusable it first has to be usable." - Ralph Johnson

- Event systems
- Engine-level communication between subsystems
- Data structures

---

#### Last Week Recap

Game Engine Architecture and subsystems

---

#### Event Systems

(1 of) most important concepts ever used in games.

- Manage communication between large modules of a system. Applies to any software.
- Significantly reduces coupling between modules.
- Scalability.

---

#### Event Systems (3 fundamental concepts)

- Event
- Listener / handler / subscriber
- Manager / dispatcher

---

#### Event Systems (Event)

`Something` of interest to `someone`.

---

#### Event Systems (Handler)

Interested parties register with the manager / dispatcher, then listen for events.

---

#### Event Systems (Dispatcher)

The (potentially single) party that fires events and notifies interested parties.

---

#### Event Systems (Whiteboard example)

Communicating with a module that you don't know anything about.

---

#### Event Systems (Game engine example)

Activity:

Suppose we have a physics engine and an audio engine. Collisions occur in the physics engine, whereas the sound effects are in the audio engine.

Using an example earlier, construct a solution to the above problem.

---

#### Event Systems (High-level Design)

Activity:

There are three concepts. How are they related? Can we create a schematic diagram of the relationship between them?


---

#### Event Systems (Usage, based on design)

```
dispatcher.onEvent(EventType.PLAYER_DIED, {
    showGameOverScreen()
})

var event = Event(EventType.PLAYER_DIED)
dispatcher.fireEvent(event)

```


---

#### Conclusion

- 

---

#### Tutorial

On StudentCentral