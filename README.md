#Snake Game with OpenGL
#Overview

This is a classic Snake game implemented using OpenGL and C++ on Windows. The snake grows longer when it eats food, accompanied by a sound effect. The game ends with a "Game Over" screen and sound when the snake hits the window edges or itself. The score increases by 5 points per food consumed and is displayed on the screen.
#Features

Snake Movement: Control the snake using arrow keys (Up, Down, Left, Right).
Food Consumption: Snake grows by 2 segments and score increases by 5 when food is eaten.
Sound Effects: Plays pickup1.wav when eating food and pickup.wav on game over.
Collision Detection: Game ends if the snake hits the window boundaries (640x480) or itself.
Score Display: Shows current score in the top-right corner.
Game Over Screen: Displays "GAME OVER!", final score, and restart prompt (press 'R').
OpenGL Rendering: Uses points for snake (red) and food (green) with a white background.

#Prerequisites

Operating System: Windows (due to use of winmm.lib and Windows-specific paths).
C++ Compiler: MSVC (Visual Studio) or compatible compiler supporting OpenGL.
Libraries:
OpenGL (GLUT, included in freeglut or similar).
Windows Multimedia Library (winmm.lib) for sound.


Audio Files: pickup.wav and pickup1.wav in C:\New folder\animatedPoint\.
Development Environment: Visual Studio or similar IDE for linking libraries.

#Installation

Clone the Repository:
git clone https://github.com/zedozed/game/snake-game.git
cd snake-game


#Install Dependencies:

Install freeglut for OpenGL:
Download freeglut from http://freeglut.sourceforge.net/.
Add freeglut.lib to your linker settings and include headers.


Ensure winmm.lib is linked (included in Windows SDK).
Place pickup.wav and pickup1.wav in C:\New folder\animatedPoint\. Alternatively, modify the PlaySound paths in main.cpp to point to your audio files.


#Build the Project:

Open the project in Visual Studio.
Configure include and library paths for freeglut and winmm.lib.
Build the solution (e.g., main.cpp) in Release or Debug mode.
Alternatively, compile manually:cl main.cpp /link freeglut.lib winmm.lib opengl32.lib glu32.lib




#Run the Game:
.\main.exe



#How to Play

#Controls:
Arrow Keys: Move the snake (Up, Down, Left, Right).
R: Restart the game after game over.


#Objective:
Guide the snake to eat green food dots to increase score and length.
Avoid hitting the window edges (640x480) or the snake's own body.


#Game Over:
Triggered by edge or self-collision, with a sound effect.
Displays final score and restart prompt.



Project Structure

main.cpp: Core game logic, OpenGL rendering, and sound handling.
C:\New folder\animatedPoint\: Expected location for pickup.wav and pickup1.wav (modify paths if needed).

#Dependencies

OpenGL: Via freeglut for rendering.
Windows Multimedia: winmm.lib for PlaySound audio playback.
C++ Standard Library: For vector, string, and other utilities.

#Notes

The game is Windows-specific due to winmm.lib and hardcoded audio file paths.
To make it cross-platform, replace PlaySound with a portable audio library (e.g., SDL_mixer) and adjust file paths.
Audio files are not included in the repository; provide your own or update paths in main.cpp.
The game runs at a fixed 100ms update interval (10 FPS).

#Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Open a pull request.

#License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Built with OpenGL and freeglut for graphics.
Inspired by the classic Snake game.
Audio handling via Windows Multimedia API.

