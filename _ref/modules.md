---
title: "Modules"
---

A module could be considered a namespace, and is basically a group of data. Every RaptorScript program consists of at least one module, since every file is a module.

### Modules belong to `.rapt` files

Each `.rapt` file defines one module, by the name of the file (excluding the `.rapt` extension)

### Importing Modules

Modules can be imported for usage inside other modules.

### Structure

Modules have a hierarchical structure, starting from the source directory.

```
|- project/
   |- src/
      |- main.rapt
      |- ui/
         |- self.rapt
         |- menu.rapt
         |- popup.rapt
      |- util/
         |- string.rapt
         |- numbers.rapt
```

This structure defines the following modules:

-   `main`
-   `ui`
-   `ui.menu`
-   `ui.popup`
-   `util.string`
-   `util.numbers`

### Naming

Module names can contain only lowercase letters and underscores. A module named `self` will simply  be referenced by its parent module. As such, the module in `src/ui/self.rapt` will be referenced simply as `ui` in other modules.

It is recommended to give modules short, concise names, letting the structure handle avoiding ambiguity. As such, it is also always recommended to refer to modules as their fully qualified names. If these two rules are followed, the module structure will make semantic sense. As an example, use `util.numbers` instead of `util.number_utils`
