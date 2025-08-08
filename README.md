# How to understand source code from other people and projects
## Analyzing MuseScore's source code

This is a set of documents that tries to **explain a thought process** for not just understanding [MuseScore's](https://github.com/musescore/MuseScore), [Audacity's](https://github.com/audacity/Audacity) and [AE's](https://github.com/advanced-effects/Advanced-Effects) source code, but also how to **analyze code** from any project.

- 📔 A method
- 🧠 for comprehending code
- 🚧 from **ANY** project
- 🤖 Without AI

## Index

- **0. Introduction.** [How to not get frustrated when writing code](/0-WARNING-FRUSTRATION.md)
- **1. Overview.** [The project structure.](/1-PROJECT-STRUCTURE.md)
- **2. The build system.** [Create your own module](/2-BUILD-SYSTEM.md) (`DeclareModuleSetup.cmake`)
- **Application workflow.** [Starting the application from start to finish.](/3-APPLICATION-WORKFLOW.md) (`main.cpp`)
- **Application loading.** [What is `IApplication` and what are modules (`IModuleSetup`).](/4-APPLICATION-LOADING.md)
- **Modularity.** [What is `ioc()`, `Inject<...> = { this };`.](/5-MODULARITY-INJECT-AND-IOC.md)
