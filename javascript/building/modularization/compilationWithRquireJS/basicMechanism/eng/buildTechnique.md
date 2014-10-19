Automatic generation of standalone vendor-free javascript files from RequireJS modules
=============

Over the years it has become clear for the javascript community the need of modularization for their projects. This is because dividing any project in little chunks of independant code has advatajes that becomes critical as the project grows:

*   **Team-ready project** Each developer on a team can be assigned a set of modules to develop and can work in parallel with minimal conflicts. Additionally, everyone can write in their own preferred style within the context of the module without preferences getting in the way of progress.
*   **Less merge conflicts** As the project is divided in several files, changes in the repository has low probability to produce a merge conflict.
*   **Code coupling reduction** Modularization forces the developers to create abstractions.
*   **Code reutilization** If there is a module that works well for a particular functionality, the developers do not have to reinvent the wheel as they can reuse it.
*   **Automatic dependency resolution** By reusing code, new modules that depend on functionality provided by other modules are loaded as a complete black-box component which provides the required functionality, with all the dependecies resolved.
*   **Custom builds** Given that the project functionality is devided in modules, and that the module's dependencies are resolved automatically, a team can produce different builds with a different set of features just by loading a different set of modules.
*   **Quality improvement** When a developer does not have to worry about the entire code, he can make sure that his individual piece of code is flawless. Then, when all of the parts are combined, fewer errors are likely to be found overall.
*   **Testeability** A module can be easily tested as a component by loading it with its dependencies.

Today, one of the most common ways to get modulization is through the AMD specification which is used by asynchronous libraries like RequireJS. For browser applications, it have a problem: They end up depending on external vendor libraries (e.g. RequireJS). There are cases where we may need to generate a single standalone javascript file which does not need RequireJS to work, but we still want to develop it with modules.

In this post I will show a very cool technique that is being used by some of the most popular javscript libraries like Modernizr and JQuery, in which the code is completely developed in RequireJS modules and then those modules are compiled into a single vendor-free javascript file.

How this works
-------------



Contact us
-------------

**e-mail**: augusto.altman@gmail.com, matiascarranza@gmail.com