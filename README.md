![Project-eden-logo](https://github.com/felinis/RoomEditImproved/assets/94763702/3da3780a-0894-454b-8f1a-4e065329b44a)

# Overview
Work-in-progress level editor for Project Eden, a video game released in 2001 by Core Design.
The program is written in C++. It is mostly object-oriented due to the nature of the file format although I am planning to switch over to a more data-oriented design.

# Project status
## Brief
A Vulkan port is in the works. I believe it would make the software easier to port to other platforms like Linux when time comes. Stay tuned for more updates.
## To Do list
- Implement LZJAT decompression and compression
- Implement texture WAD preview window
- Implement actor preview window
- Implement sound preview window
- Implement game's original metallic shader
- Update file format variable names with newest RE notes

# Rendering
The application uses a modern Direct3D 12 renderer. Video RAM and GPU heaps are managed manually using a linear arena for maximum performance.
On top of that, I implemented _bindless textures_, which is a feature allowing for more flexible texture streaming.

# User Interface
The program currently uses a Win32 UI, but I am currently planning on refactor it to use Dear ImGui instead.

# Screens
This screen shows the program user interface with a few levels loaded in. The UI is a work in progress.
<img width="948" alt="up" src="https://github.com/felinis/RoomEditImproved/assets/94763702/69db9ec7-f0ed-44d2-96a8-2915ea365020">
<img width="948" alt="down"
src="https://github.com/felinis/RoomEditImproved/assets/94763702/e746ca92-8bad-4bf9-8e52-a0623ca49228">
<img width="948" alt="room_editor_prop_value" src="https://github.com/felinis/RoomEditImproved/assets/94763702/3d5ec819-a61e-4bd4-ad07-328276621281">

# Building Instructions
- Install Visual Studio (2017 is recommended). I haven't tested MinGW, but make sure it supports C++17.
- Install CMake (minimum 3.12).
- Configure the CMakeLists.txt for the Visual Studio compiler. I personally used Visual Studio 2017 Professional.
- Build.
- Use the `edndec.exe` tool to decompress the level files, then open them inside Room Editor.
 
