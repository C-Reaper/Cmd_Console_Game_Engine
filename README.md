# Project README

## Overview
- A simple console-based game engine using a custom library for rendering and input handling.

## Features
- Basic movement control (A, W, S, D)
- Mouse position tracking
- Rendering of solid-colored triangles with wireframes
- Fixed frame rate and elapsed time calculation

## Project Structure
```
Cmd_Console_Game_Engine/
├── build/              # .exe files produced by Main.c
├── libs/               # *.c for bin
│   └── Console_Lib     # Custom library used in the project
│       ├── Console.h   # Header file for the custom library
│       ├── Console.c   # Implementation file for the custom library
├── src/                # Source code
│   ├── Main.c          # Entry point of the application
│   └── Console_Lib.h   # Standalone header-based C-file, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects (example given WINAPI, X11, ALSA)

## Build & Run
### Linux
To build the project on a Linux system:
```bash
cd Cmd_Console_Game_Engine/
make -f Makefile.linux all
```
To run the application:
```bash
make -f Makefile.linux exe
```

### Windows
To build the project on a Windows system:
```bash
cd Cmd_Console_Game_Engine/
make -f Makefile.windows all
```
To run the application:
```bash
make -f Makefile.windows exe
```

### Wine
To cross-compile for Windows on Linux using Wine:
```bash
cd Cmd_Console_Game_Engine/
make -f Makefile.wine all
```
To run the application:
```bash
make -f Makefile.wine exe
```

### WebAssembly
To build the project for web assembly:
```bash
cd Cmd_Console_Game_Engine/
make -f Makefile.web all
```
To run the application:
```bash
wasmtime ./build/Main.wasm
```