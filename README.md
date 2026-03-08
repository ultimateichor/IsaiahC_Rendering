Unreal Engine Project Setup Guide

[PREREQUISITES]
Unreal Engine 5.7 (install via Epic Games Launcher or download from Epic Games)
Install Git to clone the repository. You can get Git from git-scm.com/downloads.
Verify installation via git --version.

Also, install Git LFS using git lfs install.
Download Git LFS at git-lfs.github.com.

Visual Studio (Windows Only)

For compiling C++ projects, install Microsoft Visual Studio.

Required workloads:

Desktop development with C++

Game development with C++

Recommended version:

Visual Studio 2022
Clone the Repository

Clone the project from GitHub:

git clone https://github.com/ultimateichor/IsaiahC_Rendering.git

Navigate to the project folder:

cd IsaiahC_Rendering
Setup the Project
1. Generate Project Files

Locate the .uproject file in the project directory.

Right-click it and select:

Generate Visual Studio project files

Alternatively, run:

GenerateProjectFiles.bat
2. Open the Project

Double-click the .uproject file.

Unreal Engine will prompt to:

Build missing modules

Click Yes.

3. Compile the Project

If the project uses C++:

Open the generated .sln file in Visual Studio.

Select:

Development Editor
Win64

Click Build → Build Solution.

Running the Project

After compilation:

Open the project through Unreal Engine.

Click Play in the editor to run the game.

Alternatively:

Run the project directly from Visual Studio using:

Local Windows Debugger
Updating the Project

To pull the latest changes:

git pull

If new assets were added via Git LFS:

git lfs pull

Troubleshooting
Missing Modules Error

If Unreal reports missing modules:

Regenerate project files

Rebuild the solution in Visual Studio

Git LFS Files Not Downloaded

Run:

git lfs pull
Engine Version Mismatch

Open the .uproject file and verify the engine version matches the installed Unreal Engine version.

Project Structure

Typical Unreal project folders:

/Content        → Game assets
/Source         → C++ source files
/Config         → Project configuration
/Plugins        → Unreal plugins
