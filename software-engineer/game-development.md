[العربي](./05-game-development_ar.md)

# <a name="-5-game-development"></a>🎮 Chapter 5: Game Development

## 1. What is it?

Game Development is the art and science of creating video games. It is a multifaceted discipline that combines programming, art (2D and 3D graphics), sound design, level design, and storytelling to create an immersive interactive experience.

## 2. What does the specialist do?

A Game Developer, specifically a Gameplay Programmer, is the one who writes the code that defines the game's rules, logic, and interactions. Their tasks include:

* Programming game mechanics: Writing code for character movement, shooting, jumping, and interacting with the environment.
* Artificial Intelligence (AI): Programming the behavior of enemies and non-playable characters (NPCs).
* Physics: Implementing a physics system to simulate gravity, collisions, and forces.
* User Interface (UI): Programming menus, heads-up displays (HUD), and score screens.
* Integrating game components: Ensuring that programming, graphics, and sounds work together harmoniously within the "game engine."

## 3. Sub-domains

* Gameplay Programmer: Focuses on the core game logic and player experience.
* Graphics Programmer: Works on the rendering engine, lighting, shadows, and visual effects. This is a very complex specialization that relies heavily on mathematics.
* AI Programmer: Specializes in making game characters appear intelligent and realistic.
* Network Programmer: Specializes in building online multiplayer games.
* Tools Programmer: Builds custom tools within the game engine to help designers and artists build the game more easily.

## 4. Expanded Key Concepts

* `Game Engine`: The core software that provides an integrated framework for building games. It offers ready-made services like graphics rendering, a physics engine, sound, and scripting.
* `Game Loop`: The infinite loop that runs at the heart of every game. In each "frame," it performs three main tasks:
     1. Process Input: Reading player commands from the keyboard, mouse, or controller.
     2. Update Game State: Moving characters, updating scores, applying physics.
     3. Render: Drawing everything on the screen.
* `Physics Engine`: A subsystem within the game engine responsible for simulating physical laws like gravity, friction, and collision detection.
* `Assets`: All non-code resources used in the game: 3D Models, 2D Sprites, sound files, music, and fonts.
* `Shader`: A small program that runs directly on the graphics processing unit (GPU) to control how each pixel is drawn on the screen (e.g., how light interacts with a water or metal surface).
* `AI Pathfinding`: Algorithms (like A*) used by AI to find the shortest or best path for a character to get from one point to another, avoiding obstacles.

## 5. Expanded Tools & Technologies

* Game Engines: Unity (using C#), Unreal Engine (using C++ and Blueprints system), Godot (free and open-source).
* Programming Languages: C++ (for high performance in engines like Unreal), C# (the language of the Unity engine), Python or Lua (sometimes used for scripting).
* Graphics APIs: DirectX (for Windows and Xbox), OpenGL (cross-platform), Vulkan (modern and low-level), Metal (for Apple devices).
* 3D Modeling Software: Blender (free), Maya, 3ds Max.
* Version Control: Git LFS (for handling large files), Perforce (common in large studios).

## 6. In-Depth Workflow

Project: Program a 2D platformer character to move and jump.
Engine: Unity.

 1. Project Setup and Asset Import: Create a new 2D project in Unity. Import the character's "Sprite Sheet" (a single image containing all animation frames).
 2. Create the Player Object: Drag the character's image into the "Scene" to create a GameObject. Add "Components" to it:
     * `Sprite Renderer`: To make it visible.
     * `Rigidbody2D`: To make it affected by physics (like gravity).
     * `BoxCollider2D`: To define its boundaries and detect collisions with the ground.
 3. Write the Movement Script: Create a new C# script named `PlayerController` and attach it as a Component to the player object.
 4. Write the Code:
     * Inside the `Update()` function (which runs every frame), check for player input (`Input.GetAxis("Horizontal")` for right and left movement).
     * Apply a force or change the velocity of the `Rigidbody2D` to move the character.
     * Check if the jump button is pressed. If the character is touching the ground, apply an upward force to make it jump.
 5. Animation: Use the Animator window in Unity to create an "Animator Controller." Define "States" like "Idle," "Running," and "Jumping." Then create transitions between these states based on the character's speed.
 6. Build the Level: Use the Tilemap editor in Unity to "paint" the level using the imported tile images.
 7. Run and Test: Press the "Play" button inside the Unity editor to test the game directly. The developer can adjust variables (like movement speed and jump force) in real-time until they achieve the desired feel.

## 7. Common Job Roles

* Gameplay Programmer
* Graphics Programmer
* AI Programmer
* Tools Programmer
* Technical Artist: A bridge between artists and programmers.

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`AI`** | Artificial Intelligence, used to control the behavior of non-player characters. |
| **`Asset`** | Any resource used in the game (image, sound, 3D model). |
| **`A* (A-star)`** | A popular algorithm used for pathfinding. |
| **`Blueprint`** | A visual scripting system in Unreal Engine. |
| **`Collider`** | An invisible component that defines the physical shape of an object for collision detection. |
| **`Component`** | A functional piece that can be added to a `GameObject` in Unity (like a physics component or a script). |
| **`Delta Time`** | The time elapsed between the previous frame and the current one, used to make movement smooth and device-speed independent. |
| **`Game Engine`** | The integrated development environment for making games. |
| **`GameObject`** | Any object that exists in the game world in Unity. |
| **`GPU`** | Graphics Processing Unit, responsible for all rendering and drawing operations. |
| **`HUD`** | Heads-Up Display, the information overlay shown to the player (like health and ammo bars). |
| **`LOD (Level of Detail)`** | A technique that uses less detailed models for distant objects to improve performance. |
| **`Material`** | Defines how an object's surface looks (color, shininess, texture). |
| **`Mesh`** | The polygonal net structure that forms any 3D model. |
| **`NPC`** | Non-Player Character, controlled by AI. |
| **`Physics`** | Simulation of physical laws like gravity, force, and collision. |
| **`Prefab`** | A ready-made, saved `GameObject` template that can be easily reused (like an enemy prefab). |
| **`Procedural Generation`** | Algorithmically creating game content (like levels or worlds) instead of designing it manually. |
| **`Raycasting`** | Firing an invisible ray in a specific direction to detect what it hits (used for shooting or checking for ground). |
| **`Rendering`** | The process of drawing the 3D scene onto your 2D screen. |
| **`Rigidbody`** | A component that makes an object affected by physics. |
| **`Shader`** | A small program that runs on the GPU to control the appearance of Materials. |
| **`Sprite`** | A 2D image used as a character or object in 2D games. |
| **`State Machine`** | A common way to program AI behavior (states like: "patrol," "chase," "attack"). |
| **`Texture`** | A 2D image that is "wrapped" around a 3D model to give it surface detail. |
| **`Transform`** | A component that defines the Position, Rotation, and Scale of any object in the game. |

</details>

[⬆️ Back to Table of Contents](README.md)

