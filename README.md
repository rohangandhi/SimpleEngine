# SimpleEngine
SFML wrapped in the Visual Studio build system. The project is intended to be a quick way to start developing native windows applications using SFML.
This solves the problem of having to deal with the CMake and the hardcoded settings and references it generates when creating the Visual Studio Solution to build SFML.
With this project it should be very easy to apply specific Visual Studio build settings to all of SFML.

In this project, SFML is built to static libraries and SFML Examples are built to applications that can be debugged from within Visual Studio.

Versions supported:
* SFML 2.3
* Visual Studio 2013

The Build system uses property sheets (.props files) to allow applying build settings at various scopes. 
* The SimpleEngine.props file has settings that apply to all the Visual Studio projects.
* The SFML.props file has settings applicable to all Visual Studio projects that build SFML libraries.
* The Examples.props file has settings applicable to all Visual Studio projects that build Example Applications.
* Each visual studio project file (.vcxproj) can choose to override or extend any of the global settings.

It should be relatively easy to support new versions of SFML or Visual Studio.
