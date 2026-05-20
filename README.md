# vulkan-render-graph

Minimal C++20 Vulkan rendering experiment focused on building a small render
graph playground. The repository currently contains a GLFW/Vulkan window
bootstrap and local dependency headers/libs used by the prototype.

## Current Scope

- CMake-based C++20 project.
- GLFW window initialization.
- Vulkan SDK include/lib wiring.
- Render-graph exploration code and supporting headers.

This is an early prototype, not a packaged engine.

## Repository Hygiene

Generated CMake/Ninja/build outputs are ignored by `.gitignore` and should not
be committed. Build in a separate directory such as `build/`:

```powershell
cmake -S . -B build
cmake --build build
```

The original local `cmake-build-debug/` directory and binary artifacts were
removed from Git history going forward.

## Requirements

- CMake 3.29 or newer
- C++20 compiler
- Vulkan SDK
- GLFW libraries compatible with your compiler toolchain

The current `CMakeLists.txt` expects dependencies under `Dependency/`. Adjust
the include and library paths if your local Vulkan/GLFW layout differs.
