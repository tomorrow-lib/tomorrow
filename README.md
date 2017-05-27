[WIP] Tomorrow [![license](https://img.shields.io/github/license/tomorrow-lib/tomorrow.svg?style=flat-square)]()
==============

A WIP simple and flexible job scheduling library for .Net Core, with a focus on supporting multiple queue handlers.

| Package                    | Nuget Status                                                                                                                                                           |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tomorrow.Core              | [![NuGet](https://img.shields.io/nuget/v/Tomorrow.Core.svg?style=flat-square)](https://www.nuget.org/packages/Tomorrow.Core)                                           |
| Tomorrow.Core.Abstractions | [![NuGet](https://img.shields.io/nuget/v/Tomorrow.Core.Abstractions.svg?style=flat-square)](https://www.nuget.org/packages/Tomorrow.Core.Abstractions)                 |
| Tomorrow.Core.Json         | [![NuGet](https://img.shields.io/nuget/v/Tomorrow.Core.Json.svg?style=flat-square)](https://www.nuget.org/packages/Tomorrow.Core.Json)                                 |
| Tomorrow.InProcess         | [![NuGet](https://img.shields.io/nuget/v/Tomorrow.InProcess.svg?style=flat-square)](https://www.nuget.org/packages/Tomorrow.InProcess)                                 |

Goal
----

_Tomorrow_ is designed to be a simple, flexible interface to handle scheduling
jobs.

Currently, the following libraries are available to assist implementations:

* `Tomorrow.Core.Json` - handles some JSON serialization logic to allow
  storage and retrieval of scheduled jobs

The following queue handlers are available:

* `Tomorrow.InProcess` - a basic in-process queue handler, which does not
  persist or distribute jobs.

Limitations
-----------

* The expression-based scheduling interface only supports invocations of
  instance methods on object instances retrieved from the DI pipeline. (This is
  by design until further security considerations are addressed)

Roadmap
-------

* [x] Support multiple queue handler backends in the some application (e.g.
    in-process to handle file uploads, Redis to perform encoding tasks)
* [ ] Support a persistent queue handler (Redis-based)
* [x] Support class-based jobs
* [ ] Support a reporting pipeline for jobs
* [ ] Consider supporting a richer set of queued expressions, balanced against security concerns
* [ ] Build documentation for consumers and implementors
* [ ] Provide some usage scenarios
