# 3D Beer Bottle Simulation

A real-time OpenGL/C++ simulation of a beer bottle with animated liquid, rising bubbles, and a mouse-driven light that changes color depending on whether it's over the bottle.

---

## Features

- **Textured beer bottle** rendered as a quad with alpha transparency
- **Animated liquid** — a procedurally generated cylindrical mesh with a wavy surface, updated every frame
- **Rising bubbles** — 150 particles that drift upward, wrap around, and reset at the liquid surface
- **Mouse-driven light** — a white point light that follows the cursor via unprojection
- **Inside/outside detection** — the light and the liquid's specular spot turn **orange** over the bottle body and **white** outside it (or over the neck), using a CPU-side texture alpha sample
- **Blended transparency** — the bottle and liquid are alpha-blended with depth-mask handling

---

## Requirements

- **C++ compiler** (g++, clang++, etc.)
- **OpenGL 3.3+** core profile
- **GLEW**
- **GLFW 3**
- **GLM**
- **STB Image** (`stb_image.h`)
- A PNG texture named `beer_bottle.png` in the working directory

### Linux install (Debian/Ubuntu)

bash
sudo apt install g++ libgl1-mesa-dev libglew-dev libglfw3-dev libglm-dev

build
g++ 3D_beer_bottle_simulation.cpp -lGL -lGLEW -lglfw -o beer_bottle

run
./beer_bottle
