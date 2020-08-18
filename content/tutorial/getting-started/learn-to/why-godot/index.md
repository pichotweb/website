+++
title = "Why Godot?"

description = "Our pick for GDQuest is the Godot game engine. Why do we think this it's worth the time for you to look into it?"
author = "razvan"

date = 2020-08-18T18:25:08+03:00
weight = 10
draft = true
+++

If you're just starting out you may be interested in our [other article]({{< ref "tutorial/getting-started/learn-to/game-engine-basics/index.md" >}}) covering the basics of game engines in general.

## How to choose a game engine - advanced developers

When it comes to picking a tool, usually it isn't a clear cut answer. We have to weigh the pros and cons on a case-by-case basis. One framework that works for you might not work for us. With that in mind we'll cover next a few ideas to consider when browsing for a game engine.

#### Closed source VS open source

This can become a complex matter, it can be philosophical on one hand as well depending on your personal feeling towards an open source software as opposed to a closed source package. On the practical side, an open source tool gives us the ability to customize the code for our particular needs. Closed source also means that the company might, for whatever reason, drop support and availability for the tool version you require.

#### License, royalties and fees

Sometimes overlooked, license can play a big role in choosing a tool. It can start free for indie developers for example and after a successful start you might be required to pay fees that you haven't initially considered.

#### Documentation and support

This is a huge important factor to consider. An undocumented complex tool with is almost useless so good official docs are a must.

#### Editor

A GUI editor is much simpler to use than to code everything, although, as mentioned before, it can be a subjective matter. It's something to consider.

#### 2D/3D support

Some game engines have been specifically developed to work with 2D or 3D. There are a few that support both visual styles.

The complexity comes from the fact that, although there is overlap, when it comes to the implementation there is enough difference to split the functionality between 2D and 3D.

#### Available scripting languages

Depending on your background, scripting language availability might turn out to be a big factor. Not everyone is willing to learn a new language from scratch. On the other hand, artists and non-coders might want prefer visual scripting languages.

#### Customizability

This is different from being an open source project which can be customized at the low level. Most game engines these days have a plugin system in place that allows extensibility and customization of the workflow. It's one factor to consider.

#### Performance, storage and run-time memory

These can be important factors, but not as important as some people might think. Most devices these days are good enough to run even unoptimized projects on them. We start thinking about these factors once we get to a point where we create complex games such that every frame we need the best performance, or if we target low-end platforms.

#### OS cross-compilation

Supported platforms is a major factor to consider since this might limit our availability on the market place.

#### Support for different asset types

Importing assets from external tools isimportant as not everything can and is done through the game engine framework itself.

#### Community

Having a community available can help us get unstuck on specific issues we might encounter. Not everything is covered by the official documents and having a strong community to rely on can save us a lot of grief and time spent debugging.

#### Tool design philosophy and architecture

This can cover a wide spectrum of concerns, going from object oriented programming concepts all the way to functional programming concepts and beyond. Design philosophy of the tool can influence our workflow greatly so it's a factor to consider.
    
#### Tool development cycle

How fast a tool releases updates, fixes, new version is something to consider. It's a sign of people being interested in the tool and the activity behind the management.

#### Up-to-date tech

Especially with game development, being up to speed with the latest tech and research is almost a requirement these days. Depending on our project needs we might require state-of-the art functionality or just an available framework that uses the latest developments in performance improvement and visual presentation.

### Conclusion

These are a few of the things to consider when researching game engines and the right tool for our needs. Game engines can be so much more than simple tools we choose for specific tasks and projects. They can literally dictate how we grow as a team or individual in our pursuit for game development.

In the next part we'll look at a few highlights from the Godot game engine.

## Why Godot

At GDQuest we have astrong connection with the Godot game engine. It's a tool that successfully worked for our specific needs. Let's look at how the considerations above stack up against Godot:

#### Closed source VS open source

It's open source meaning we have access to the internals of the engine, making it highly customizable.

#### License, royalties and fees

It's MIT licensed meaning we can change and profit from the engine as we need, with 0 fees.

#### Documentation and support

When we first started using Godot, documentation was lacking. These days it has pretty good support and docs although it can definitely be improved.

#### Editor

Godot has abeginner-friendly game editor which is a big plus.

#### 2D/3D support

Godot supports both 2D and 3D, having the engine split to accommodate both styles. Details matter here so for example 2D is much more mature than 3D support at the time of this writing.

#### Available scripting languages

Officially supported are:

- GDScript: a beginner-friendly custom scripting language heavily influenced by Python
- C#: a well established scripting language for power users
- Visual Scripting: artist and non-coder friendly visual node-based editor
- Community languages including: Python, Javascript, Rust and more.

So Godot is packed with options when it comes to this question.

#### Customizability

Godot currently has a clunky plugin system which is in the process of being re-written. At GDQuest we have sparingly used it for our projects so it isn't a main concern.

#### Performance, storage and run-time memory

As mentioned before, the 2D part of the engine is much more mature and so the performance is good, while 3D is lagging behind.

There is considerable effort to bring the latest tech into the 3D implementation. We expect a bing change with Godot v4.

The executable itself is has asmall storage footprint which isimpressive for the functionality that it brings. Likewise the compiled projects can besmall in size and this can also be optimized further.

For us this means aimportant growth impact when it comes to this consideration.

#### OS cross-compilation

Godot can compile for virtually all available platforms. From mobile, to PC, Linux, even iOS and VR/AR.

#### Support for different asset types

This game engine supports most main-stream assets and there are a number of tools that have created exporters for Godot. So this part iswell covered.

#### Community

Godot has avibrant community, growing at asteady pace with many contributors to the project itself, but also to giving feedback and helping out beginners.

### Conclusion

Given all the above positive points we decided that Godot is a good starting tool for us. Even with the few downsides we mentioned.

## A short overview of Godot

As we saw above, it comes with an impressive list of features, packed in a tiny executable package. The software includes a game editor and lots of built-in classes to simplify the game building process.

![Godot Game Engine](./img/godot-engine.png)

One of Godot's main design goals is to be user-friendly, having alow entry bar which means that artists and non-coders can learn to make games with it just as much as anyone else.

Its main coding language is called GDScript, an in-house built scripting language highly influenced by Python, but far more simpler. Being derived from Python means that it'sclose to the English spoken language which is one reason why it can be learnedquickly. Among other things, Godot also comes with a visual script editor which means that we can code visually, connecting nodes together. For advanced users, Godot also officially supports C# as an alternative scripting language.

![Godot Visual Script Editor](./img/godot-visual-scripting.png)

In Godot, we have a class called [`MainLoop`](https://docs.godotengine.org/en/stable/classes/class_mainloop.html#class-mainloop) which is this game engine's main game loop. It can be customized with our own code if required, although in practice this issituational.

The default `MainLoop` implementation is provided by the [`SceneTree`](https://docs.godotengine.org/en/stable/classes/class_scenetree.html#class-scenetree) class. It manages a tree hierarchy of nodes that together create a scene tree. To learn more about the `SceneTree` and Godot's particular implementation of the main loop check out the [`SceneTree` tutorial](https://docs.godotengine.org/en/stable/getting_started/step_by_step/scene_tree.html) in the official docs.

![Godot Scene Tree](./img/godot-scene-tree.png)

The image above shows a scene tree structure made with built-in nodes, from one of our demo projects. This is a core architecture design of Godot.

All of these features and design decisions that go into creating a game engine come into play when deciding on which package to choose for our own projects. For us, Godot is our main pick as one of the fastest growing open source game engines available.

Perhaps it can be for you too.
