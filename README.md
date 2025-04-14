### Features
- **User Interface**
  - ImGui
  - Runtime unloading
  - Log console
  - ImGui rendering

- **Combat Features**
  - Aimbot

- **ESP Features**
  - Player ESP
  - Vehicle ESP
  - Health bars

- **Utility Features**
  - Spectator list
  - Streamer mode

So I realised I fucked up, make sure you make a secondary folder and put all the 667.filters etc into a different folder called 667
including the include folder, lib folder and src folder then keep the .sln in the main folder and open it

### Use these build settings in your project to remove errors:
- Configuration Properties -> General -> `Configuration Type: Dynamic Link Library (.dll)`
- Configuration Properties -> General -> `Platform Toolset: Visual Studio 2022 (v143)`
- Configuration Properties -> General -> `C++ Language Standard: ISO C++20 Standard (/std:c++20)`
- Configuration Properties -> Advanced -> `Character Set: Use Unicode Character Set`
- C/C++ -> Preprocessor -> Preprocessor Definitions: `_CRT_SECURE_NO_WARNINGS`
- C/C++ -> Precompiled Headers -> Precompiled Header File: `common.h`
- C/C++ -> General -> Additional Include Directories: `$(ProjectDir)include;$(ProjectDir)src;%(AdditionalIncludeDirectories)`
- Linker -> Input -> Additional Dependencies: ```fmt.lib
DirectXTK.lib
freetype.lib
g3log.lib
minhook.x64.lib
%(AdditionalDependencies)```
- Linker -> General -> Additional Library Directories: `$(ProjectDir)lib;%(AdditionalLibraryDirectories)`
