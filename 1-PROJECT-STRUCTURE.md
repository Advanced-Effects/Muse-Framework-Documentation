# The Project Structure

In this guide I assume you know basic things such as [how to use git to download the source code](https://www.w3schools.com/git/default.asp), programming concepts such as objects and services, and [elemental C++ syntax](https://www.w3schools.com/cpp/default.asp). If not, click these links. They are going to be helpful.

### Opening project for the first time

When you open MuseScore, Audacity or Advanced Effects you will see a project structure like the following:

```
- .github
- .tx
- buildscripts
- demos
- docs
- fonts
- hooks
- sandbox
- share
- src
- test
- thirdparty
- tools
- vtest
- .clangd
- LICENSE.txt
- CMakeLists.txt
```

And this might confuse beginners and first and make it seem much more complicated than it really is. But 99% of the time you only really need to care about two of these files: `src/` and `CMakeLists.txt`.

This is one of the most important skills in programming and one that doesn't get taught in tutorials. See, 75% of the programming process isn't actually writing code. It's *planning* what you are going to write and how. The tutorials you see have *already gone through* that exploration phase and they only teach you about things like specific language syntax. But let's continue.

### If you expand `src/`, you will then again see a large quantity of folders:

```
- app
- appshell
- appshell_web
- braille
- commonscene
- context
- converter
- engraving
- framework
- importexport
- inspector
- instrumentsscene
- musesounds
- notation
- palette
- playback
- print
- project
- stubs
- webbridge
- CMakeLists.txt
```

But **then again, 99% of these folders are not necessary** to understand the code and open a window.

Browsing and understanding what the code means requires some time, that is completely normal in a new project. But let's ask **some questions**: 'What is `app/`? Why should it be called that way?' and make **some observations** that could **explain it.**

- **Ask questions:** 'What does this folder do? What do you think it could do?' (Ex. appshell could be the application's GUI because the shell is the UI face of chromium, for example.)
- **Make observations:** What files does the folder have? (Ex. check if `appshell/` has in fact UI files)
- **Extract a conclusion:** `appshell/` is (or *is not*) the application's UI layer.

We don't know what `app`, `framework` or `context` mean. But we can discard options. **We are looking for the start of the application** (main.cpp) to get a **feeling of how the source code works together**.

We could **start by discarting** some options. I guess `converter`, `importexport`, `project`, `stubs`, ... are **not essential** to understanding the code for now, so for now we're discarding all of them. What we are left with is this:

```
- app
- appshell
- framework
- context
- CMakeLists.txt
```