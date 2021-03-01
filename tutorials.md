#### Tutorial 1

Note: take breaks at regular intervals between tasks and talk to your peers (on Teams).

1. Think about / choose your game engine aspect. (15 mins)
1. Discuss with your peer (on Teams) the game engine aspect you would like to build. (15 mins)
1. On your own (refine) your ideas. (20 mins)
1. Background research (see what you can find online about your aspect. (15 mins)
1. Make notes about your research and thoughts into a document and leave this until next week. (20 mins)

---

#### Tutorial 2

Note: take breaks at regular intervals between tasks and talk to your peers (on Teams).

1. Clone and build the assignment code. (15 mins)
1. Run / play the assignment game example and skim through the code. (15 mins)
1. Create a Word (or alternative) document. Add a title page that says "Game Engine Fundamentals: MY_ENGINE_ELEMENT" and replace "MY_ENGINE_ELEMENT" appropriately.
1. Add a Table of Contents page.
1. Add another page with a few sentences related to what the chosen engine element will do. For example: "I will extend the xcube2d engine with a particle system. The system will produce visual effects in the form of moving particles...".
1. Make sure you can build and run the code that is provided as part of the assignment.
1. Consider the existing code base of the engine to see where your new code might reside.
1. Start designing (on paper) what the system will look like (visually), how it will work (architecture), what other systems it will communicate with, etc.
1. By the end of this tutorial, you should have a strong idea of what you are going to do. It is fine if you don't yet know how to implement it.

---

#### Tutorial 3

Note: take breaks at regular intervals between tasks and talk to your peers (on Teams).

1. (Optional but recommended) Create a fork of xcube2d under your GitHub account. This is where you will be developing your assignment work. Remember to back up, **computer scientists do not lose data!**
1. Last week you started reading a bit of the codebase. Now read through all of the codebase and consider where the major parts, such as the main loop, graphics drawing and input, are located.
1. Start designing (on paper) how the subsystems you identified last week are going to talk to your new subsystem (you *don't have to* use events subsystem for this assignment).
1. By the end of this tutorial, you should be able to build, run and extend the given code. Add some code to the assignment code base, such as the one shown in the tutorial demonstration, or start a basis for your own engine subsystem.

---

#### Tutorial 4

Note: take breaks at regular intervals between tasks and talk to your peers (on Teams).

1. Create a class in `MyEngineSubsystem.h / .cpp` (from the assignment codebase).
1. Add a function to the new class to make it do something. For example a simple function that prints `System is initialized` to the terminal should do it.
1. Instantiate your newly created system in `MyGame.cpp` and call your newly created function. 
1. On paper, design the visual aspect of the game demo that you will develop. This can help you figure out the API for your system.
1. By the end of this tutorial, you should have some simple (original, i.e. added by you) code that runs with the engine.

---

#### Tutorials 5+

Note: take breaks at regular intervals between tasks and talk to your peers (on Teams).

From this tutorial onwards, you should focus only on the assignment codebase, in order to complete the coursework. The following tips should help you develop:

1. Have a storyboard or similar on paper that helps you visualise your goal, i.e. what the end-result looks like. Then develop to meet that end-result.
1. Read the source of existing systems in the codebase -- they will help you structure your own code.
1. Start developing your demo alongside the engine to help you guide the API of your system.
1. Ask any questions you have (in the Q&A channel on Teams) as soon as possible to expedite the development.
1. [CPP reference](https://en.cppreference.com/w/) is a great resource for C++ documentation.

---