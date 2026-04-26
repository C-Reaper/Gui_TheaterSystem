# Project README

## Overview
This project is a simple graphical user interface (GUI) application built using C programming language. The GUI application uses an internal library to handle the rendering and input processing. The application features basic navigation controls such as left, right, up, and down arrow keys.

## Features
- Basic GUI with custom rendering.
- Navigation control using arrow keys (left, right, up, down).
- Built-in support for Linux, Windows, Wine, and WebAssembly platforms.

## Project Structure
```
Gui_Theater_System/
├── build/              # .exe files produced by Main.c
├── src/                # source code directory
│   ├── Main.c          # Entry point of the application
│   └── *.h             # header files used by Main.c
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
├── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
└── LICENSE
└── .gitignore
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects:
  - Linux: X11, PNG, JPEG
  - Windows: WINAPI, GDI32, WINMM
  - Wine: WINAPI, GDI32, WINMM
  - WebAssembly: Emscripten

## Build & Run
### Build Process
To build the project for a specific platform, navigate to the project directory and use the appropriate Makefile:

- **Linux**:
  ```sh
  make -f Makefile.linux all
  ```
  
- **Windows**:
  ```sh
  make -f Makefile.windows all
  ```
  
- **Wine** (for cross-compiling for Windows on Linux):
  ```sh
  make -f Makefile.wine all
  ```

- **WebAssembly**:
  ```sh
  make -f Makefile.web all
  ```

### Execution
To execute the built application:

```sh
make -f Makefile.(os) exe
```

### Clean Rebuild
For a clean rebuild (removes build artifacts and starts fresh):

```sh
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

### Build Options
- `all`: Build the output.
- `do`: Build + executable output.
- `clean`: Remove build artifacts.

Replace `(os)` with the appropriate OS (linux, windows, wine, web).