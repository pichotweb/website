+++
title = "Game Engine Basics"
menuTitle = "Game Engine Basics"

description = ""
author = "razvan"

date = 2020-08-15T21:52:08+03:00
weight = 5
draft = true

difficulty = "beginner"
keywords = ["tutorial"]
+++

Learning a full-featured tool like [Godot](https://godotengine.org) can be overwhelming for beginners. In this tutorial we'll break down how a game engine works, from a programmer point of view, in the context of Godot and GDScript.

We'll learn about:

- What a game engine is and specifically about the Godot game engine
- GDScript basics: input handling and real-time processing
- What are signals and how to coordinate function calls with them

## What is a game engine

Godot is a full-featured tool for making games. Put very simply that is what a game engine is.

![Godot Game Engine](img/godot-engine.png)

The purpose of a game engine is to make game developers' life easier by automating repetitive tasks that appear in most game projects. This comes with advantages and disadvantages.

The advantages are that:

- We don't have to build everything from ground up facilitating fast prototyping and building a workflow pipeline
- Tool makers integrate with existing game engines making it easier to integrate their assets
- Developers can focus on game content rather than technicalities
- Makes it easier for non-coders to participate in the game development process

On the other hand, disadvantages include:

- It's harder to control performance since we can't easily tweak the backend code
- Workflows can become highly specialized making it difficult to integrate or expand with exterior tools

Godot is both a game engine and an editor. The editor allows us to visually create our game from different assets (images, 3D models, audio files etc.) while the engine is the framework that allows us to run our games. As a comparison, [Panda3D](https://www.panda3d.org) is a SDK (Software Development Kit) game engine without an editor.

These days we take for granted what Godot has to offer:

- User input handling
- Animation
- Audio
- Navigation
- Internationalization
- GUI (Graphics User Interfaces)
- Networking
- Rendering
- Particle system
- Physics simulations
- Profiling and debugging
- Compile and run projects on multiple platforms

And many more features.

### The game loop

So how does Godot work? The main concept of a game engine is **the game loop**. We can think of the game loop as the heart of the game engine. It's what makes it tick.

Among the many systems that build up the Godot game engine, we have an animation system and a physics simulation system. The physics engine is built such that it runs at 60 frames per second, while the animation system isn't required to keep a fixed frequency.

This means that some of these tasks are separated in threads, underneath the hood, for example some of the common ones are:

- idle frames (for animation decoupled from physics simulations)
- physics frames (for physics simulations)
- user input (such as button presses, mouse movement, joystick action etc.)

All of this functionality is managed by the main game loop. In Godot, we have a class called [`MainLoop`](https://docs.godotengine.org/en/stable/classes/class_mainloop.html#class-mainloop) which can be customized with our own implementation if need be.

The default `MainLoop` implementation is provided by the [`SceneTree`](https://docs.godotengine.org/en/stable/classes/class_scenetree.html#class-scenetree) class. It manages a tree hierarchy of nodes that together create a scene tree. To learn more about the `SceneTree` and Godot's particular implementation of the main loop check out the [`SceneTree` tutorial](https://docs.godotengine.org/en/stable/getting_started/step_by_step/scene_tree.html) in the official docs.

## The editor
