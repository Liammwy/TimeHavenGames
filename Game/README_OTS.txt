# First Time Setup – 'Game' Project (C++ Enabled)

Hey team! 👋

The project now includes a lightweight C++ module to help with plugin rebuilding (especially for Niagara). This change allows better engine integration — but **you can still work as normal in Blueprints, Niagara, level design, materials, etc.** with no changes to your workflow after the initial setup.

You only need to follow these steps **once** after pulling the latest version from GitHub.

--------------------------------------------------------------------------------------

## ✅ One-Time Setup Instructions

### 🪟 Windows

#### 1. Install Visual Studio
Make sure you have **Visual Studio 2022** installed with the following components:

- ✅ Desktop development with C++
- ✅ Windows 10/11 SDK
- ✅ MSVC v142 or v143 toolset (depending on your UE version)
- ✅ CMake tools for Windows *(optional but helpful)*

#### 2. Generate Project Files
After cloning or pulling:

- **Right-click** the `Game.uproject` file  
- Choose **"Generate Visual Studio project files"**

This will create the `Game.sln` file.

#### 3. Build the Project
- Open `Game.sln` in Visual Studio
- From the menu: **Build > Build Solution**

#### 4. Open in Unreal
You can now launch the project as usual by double-clicking `Game.uproject`.  
You don’t need to open Visual Studio again unless you want to write C++ code.

-----------------------------------------------------------------------------------------------

### 🍎 macOS

#### 1. Install Xcode
- Download **Xcode** from the App Store.
- Open Xcode at least once to agree to the licence.
- (Optional) Install command line tools:
  ```bash
  xcode-select --install

2. Generate Xcode Project Files
Right-click Game.uproject and select "Generate Xcode project",
or run:

bash
Copy
Edit
/Path/To/UnrealEngine/Engine/Build/BatchFiles/Mac/GenerateProjectFiles.sh -project="/Path/To/Game/Game.uproject"

3. Build the Project
Open the generated .xcodeproj or .xcworkspace

Build the project once in Xcode

4. Open in Unreal
Launch Unreal Engine and open the Game.uproject as usual.

------------------------------------------------------------------------------------------------

🐧 Linux
1. Install Build Tools
Ensure your system has:

clang, make, cmake, and other C++ build essentials.

On Ubuntu, run:

bash
Copy
Edit
sudo apt install build-essential clang cmake

2. Generate Project Files
From the terminal, run:

bash
Copy
Edit
/Path/To/UnrealEngine/Engine/Build/BatchFiles/Linux/GenerateProjectFiles.sh -project="/Path/To/Game/Game.uproject"

3. Build the Project
Use make to build the project:

bash
Copy
Edit
make

4. Open in Unreal
Launch the Unreal Editor (installed or built) and open Game.uproject.

-----------------------------------------------------------------------------------------------------

🧹 Notes
This is now a C++ Unreal project, but you don’t need to use C++ unless you want to.

You can still work entirely in Blueprints, Niagara, level design, and so on.

This change enables the project to rebuild plugins (like Niagara) that require source access.

📁 Git Repo Hygiene
Make sure your repo includes a .gitignore with the following:

swift
Copy
Edit
/Binaries/
/Intermediate/
/Saved/
/DerivedDataCache/
/.vscode/
/.vs/
*.sln
*.VC.db
*.opensdf
*.sdf
These folders are local build artifacts and should not be committed.

If anything goes wrong or feels weird, reach out!
You’re not expected to know this stuff — that’s what teamwork is for 💻🔧