# Introduction to analytical thought applied to code
## How to not get frustrated when writing code and avoid using AI.

**All programmers who are ambicious**, but especially beginners, **get frustrated at some point** when writing new code or trying to contribute to an existing project.

I will argue that this is because **writing new code** involves more skills and is slower than **remembering steps** (how tutorials work).

### Frustration begins with feature creep

What many people don't know is that **frustration is entirely avoidable** in programming.

> Many people start their dream project by copying the things that they like. For example, I learned programming because I liked videogames a lot and I wanted to make my own.

> Then, they start **listing a set of features** that are required to finish **that dream project**. For example, here are the basic basic things that would be required to make my dream game, a Ratchet & Clank copy:
> - A player movement system
> - A camera that is movable by the user
> - A weapons system
> - Enemies that move and shoot the player with a certain logic
> - Creating 3D models
> - Animating the 3D models
> - ...

Then, **they get frustrated** because they can't **even create a bare command-line C# project**, or **download the runtime necessary to compile it.**

> Having ambition is good in programming. We didn't get into the profession to do just basic things and ambition keeps us moving forward. Overambition is what keeps you from going forward.

The ambition to develop a Ratchet & Clank game is perfectly good, and you can do that. Just **take into account these 3 tips:**

- **The 1% rule.** Instead of doing everything at once, improve 1% every day.
Instead of trying to program the **whole game in one piece**, separate it in **Systems**.
This allows you to work much more *focused on specific tasks* and *comprehend the technology*.

- **Get your project compilable as fast as possible.** Motivation lasts for a limited amount of time. It is especially shorter if you don't see any progress being made because *the project never compiles* and *you're constantly getting errors*. Instead, I propose you to advance in little steps. For example, before making that R&C dream game, I would first make a bare C# template that only runs to the command line. *When* that is finished, I would go onto drawing graphics, or maybe doing basic 2D movement.
This is what I did with [Muse-Qml-App-Template](https://github.com/Advanced-Effects/Muse-Qml-App-Template) and [Rendering-Lab](https://github.com/Advanced-Effects/Rendering-Lab) (a bare app template that uses MuseScore ui components and a bare application that integrates OpenGL + Skia). It is good for everyone because while you're keeping tasks little, you *create projects that others can benefit from* (templates!).

- **Make systems, not games.** Don't start with the R&C game because then you're going to have *multiple pieces* that aren't isolated. Make systems, not projects. For example, maybe 1 day you can make a **project focusing on the player movement**, finish and **publish** that. Then you can work on a separate system that demonstrates *3D animations working in a game engine*, or *create a 3D model yourself*. You can **focus on the indivudal tasks** a lot better because now you have the **space and time to invest mental effort** into them, comprehending what you do. Without worrying about errors, or other parts of the code interacting with them. And then, **the final task is just adding those systems back together.** That's much easier than having to create all of them from scratch, in one attempt!

### Programming isn't just writing code

When you begin your adventure as a programmer you usually imagine yourself in front of a coding editor writing code most of the time. That's the normal thing that developers do, right? Write code. Every **second** that isn't **spent writing code** in front of a screen **is wasted time.**

**❌ WRONG!**

Well, at least wrong **for you**. Extremely experienced developers, when tackling challenges that they already somewhat solved previously can just **remember how it was done** and just write it in code.

That's **not true for you**. You are still **learning** to **think analytically**. **You will only** spend **25% of the time** in front of a code editor. Perhaps, even less.

The **trick** that **most people don't know** is that **75% of time when writing code is spent on the planning phase.** The planning phase consists of stopping to ask: *WHAT do we want?*, *and HOW do we do it?*. (These 2 are SEPARATE!)

A way to think about this is imagining the interaction between a Tab Bar and the Text Editor in a coding app. The two elements are visually together, but that doesn't mean they work together. The tab bar, for example, needs to track one thing in the application: currently open files. So, for example, you might have a Singleton `AppState` with a variable `File[] openFiles;`. The task of the tab bar is to display the files that are open, and when the user clicks on a file, set the `File *currentlyOpenFile`.
The text editor then would only need to load the `currentlyOpenFile` and make any changes of it.

Of course, in real applications everything's a bit more complex, but this gives you an idea of what developing real projects looks like.

If you're already here I highly recommend a document called [Thinking in React](https://react.dev/learn/thinking-in-react) which gave me this mindset. You  develop a full app by **thinking of each component** separately and what it needs to keep track of.

And even for the most skilled developers, *quitting the computer* to take a walk, or talk with another programmer can help clear the mind and find solutions faster!

### The planning phase is a wandering thought phase

Take notes, go for a walk, make drawings about your code. Talk with your peers, or maybe to people in a Discord support channel. Enjoy a youtube video that explains some interesting story or a programming concept. I recommend LiveOverflow a lot for this.

### Programminmg is a scientific activity

It is wrong to think that programming consists of only writing code in front of a code editor. That idea is promoted a lot by agents like ChatGPT. It is WRONG!

Programming is a scientific thought activity, where you need to *comprehend* the systems that are in play.

> You'll eventually read errors and know what they mean, without having to go to AI or StackOverflow (like the us, the old dudes used to do :D).

### On rubberduck debugging

[Rubberduck debugging](https://rubberduckdebugging.com/) is the *old and trusted method* to *explain what your code does, line-by-line* to a plastic duck.

> DUCK DEBUGGING REALLY HELPS! Did you ever went to a forum asking a question, because you've spent 3 hours trying to fix a problem, only realizing of the solution when you just sent the message?

> My tip: **have a Journal of Programming** explaining to yourself the problems that you face. Make a list of proposals that could maybe fix the issue. **Remember, it's the THOUGHT METHOD that matters, NOT the SOLUTION!** It's okay to take multiple days or even weeks to solve a specific problem, or be only able to solve 1 problem per day. **In the long term, that's making you a better programmer.**

#### My proposal

It's useful to write a journal. But not to publish or to document, to mentally planify what needs to be done and what is left, and place limits. Sometimes one has the perception that if you aren't writing code in the editor, you are losing time. This planification process and comprehension is between 50-75% of the whole process of programming a project. You don't have to subestimate it!

When I began to develop this program, I didn't know practically anything about CMake and QML. Now, throughout the way, I can more or less explain you in few words how the MuseScore's build system works (Concepts like Targets, Resources, Modules, Namespaces...).

I **propose you a specific method** to *self-report* your issues based on the following principle. This way, **you won't need ChatGPT or other people's help** anymore. WARNING: this method requires meditation, it **requires to think about what you're doing**.

> Asking the right question is 50% of the answer

A real example:

- *The problem*: I'm getting the error `The module "Muse.UiComponents" is not installed`
- *What has happened?* / *Why is the error happening?*
    1. The file *Main.qml* **has tried to import** the module "*Muse.UiComponents*".
    2. But, the application doesn't exactly know what this means. Which classes should form part of this module? How should it know it?
    3. In a QtQuick application there is a **very specific way to find the modules:** the QML Engine has searched a *qmldir* file (QML module declaration and its files) in the folder `Muse/UiComponents` in **every** of the **PREFIX PATHS.**
    4. It **hasn't found** any.
- *Why do you think this happened?* (Possible options, hypothesis to verify)
   - ~~The file **/Muse/UiComponents/qmldir** does **not exist**.~~
    (it DOES exist in the source code!)
   - It does exist in the source code, but it *hasn't been added* to the **Qt Resource Tree** (.qrc).
      -> A way to check this. How to show the Qt Resource Tree recursively?

      *(When I found a way to show it)* The resource tree **shows** that `Muse/UiComponents` does **exist**, **but it's inside a folder** called `/qml`. But the QML Engine was expecting to find it inside `:/` (PREFIX PATH) + `Muse/UiComponents`, so when it goes there it finds nothing.

      But **if we import the module like `import qml.Muse.UiComponents`**, it **does work!** That's because when it goes inside `:/qml/Muse/UiComponents` it **finds a qmldir** file.
- *Propose a solution.

### How to learn the specifics

Sometimes when you want to tackle a new project, you will **inevitably have to learn new things.** Maybe it's a new programming language, a different programming paradigm or something else.

The point is that **having to learn new stuff is inevitable**. Sometimes you'll be lucky and the thing you want to learn will be explained by a video. But other times you'll have to use a technology that **doesn't have video tutorials available**, or they're very limited and you'll have to read documentation. Or worse, that **documentation doesn't exist** and you have to **read raw source code**.

- **Sometimes videos will be okay**. Clarifying general programming concepts, or step-by-step tutorials of widely-used languages and frameworks.

- **Eventually, you'll need to read.** If you need to read, my recommendation is to **print the important parts** to paper. For me, it helps to concentrate and to separate yourself from the IDE.

- **Remember, reading isn't just sounding the letters.** Reading means going through a phrase, comprehend the meaning, and be able to explain it to someone else. **You DON'T need to read EVERYTHING!**. It's more important that you read few pages, but you keep track of what they mean, **than reading a lot and forgetting everything**-

- **Reading isn't a static process.** Explain it to a five year old, make a drawing, a story, or a video. Something that helps *you* remember and create meaning in your head. Remember *memory is the residue of thought* (Dan Willingham, notable education researcher).

### Rest, workaholics, rest!!!

This is a tip more for me than for you.

Many times us hobbyist devlopers **get so hyped about a code project** that we **forget about ourselves**. We do this because we are so excited on a project and want to see **quick results**. As a result, we work too many hours without any real rest later.

But **undersleeping**, **overworking** and **thinking about work all day** aren't only bad because we need to socialize and disconnect. **Overworking** is **NOT not productive** at all!!

It is in moments of **boredom** and rest that our brains really start connecting things and getting new ideas.
