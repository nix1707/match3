## 🌊 Match 3

> A lightweight, high-performance Match 3 game engine built from scratch for educational purposes.
<img width="1536" height="1024" alt="preview" src="https://github.com/user-attachments/assets/7751dda8-23fa-4a2d-94fd-56429ae243aa" />

## 🎮 About The Project

This project is a classic Match 3 puzzle game implementation that focuses on raw performance and clean code architecture. Built using **C** and the **Raylib** framework, it demonstrates how to manage game state, grid logic, and rendering without the overhead of heavy game engines.

It features a beautiful underwater pixel-art aesthetic and symbol-matching gameplay (#, @, $, %, &).

### ✨ Features

-   **Super Lightweight:** Written in pure C for maximum efficiency.
    
-   **Self-Contained:** Includes necessary Raylib headers and libraries locally.
    
-   **Educational:** Clean codebase designed to teach game loop mechanics and grid algorithms.
    
-   **Retro Aesthetic:** Pixel-perfect rendering with an underwater temple theme.
    

## 📥 Try the Demo

Don't want to build it yourself?

1.  Go to the **RELEASES** page.
    
2.  Download the latest version.
    
3.  Run `match3.exe`.
    

## 📂 Project Structure

The project is structured to be self-contained using CMake:

```makefile
match3/
├── assets/              # Fonts, Images, Audio (bgm.mp3, match.mp3, etc.)
├── include/             # Local Raylib headers (raylib.h, etc.)
├── lib/                 # Pre-compiled Raylib libraries (.lib, .dll, .a)
├── CMakeLists.txt       # Build configuration
└── main.c               # Source code
```

## 🚀 Getting Started

### Prerequisites

-   **C Compiler** (GCC/Clang/MSVC)
    
-   **CMake** (Version 3.0+)
    

### Build from Source

Since the project includes Raylib headers and libs locally, you can build using CMake:

1.  **Clone the repo**
    
    ```bash
    git clone [https://github.com/nix1707/match3.git](https://github.com/nix1707/match3.git)
    cd match3
    ```
    
2.  **Build with CMake**
    
    ```bash
    mkdir build
    cd build
    cmake ..
    cmake --build .
    ```
    
3.  **Run**
    
    -   On Windows, ensure `raylib.dll` (from the `lib` folder) is in the same directory as your executable if it isn't copied automatically.
        
    -   Run the generated executable:
        
        ```bash
        ./match3
        ```

## 📜 License

This project is distributed for **learning and experimentation purposes**.

## 💻 Author

Created by **Nazarii** _Genius, (future) billionaire, playboy, philanthropist xD_
