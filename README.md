# BoardEditor

### An ongoing project to create a 3d in-browser visualization for board games

# Description

BoardEditor is a tool intended for use in visualizing gameplay of any number of board games such as Chess or Backgammon.

It currently consists of tools to edit shapes that represent spaces on a game board, and to edit which spaces are considered "adjacent" to each other.

Further features, such as board serialization and piece visualization rules, are currently in development.

# Installation / Usage

To use this project, simply copy index.html from the [repo](https://github.com/rock-pulak/boardEditor) into your own project.

Alternatively, you can access the tool on my [github page](https://rock-pulak.github.io/boardEditor/).

Keyboard shortcuts for editing:
- CTRL + left click to add new shape
- left click + drag shape to move it
- right click shape to delete it

- left click on inactive shape to select it

- left click + drag yellow vertex to move it (changes shape)
- SHIFT + left click to create new vertex on current active shape
- right click yellow vertex to delete it from shape (line is drawn between adjacent, remaining vertices)

- SHIFT + left click + drag from red vertex (center point) to center point of different shape to create a connection between those two shapes

- Color editor in top left changes color of active object (Object needs to be de-selected to see change)

# Visuals
![checkerboard](https://github.com/user-attachments/assets/ad36028b-ab22-4362-a9b8-efb4d6321cb2)
![shapes](https://github.com/user-attachments/assets/5e1d36ce-dc7c-4225-afe7-f2ce489ab6c8)


# Future Improvements
There are a number of key features that still need to be implemented before this tool can be considered fully functional for visualizing board games.
- Serialization of board layouts (saving and loading)
- Rendering pieces on the board
- Framework for interpeting game communication protocols, such as Universal Chess Interface (UCI).

There are also many quality-of-life features I want to implement to make designing boards more intuitive and aesthetic
- Panel with instructions
- Snapping to vertices of other objects
- Standard keyboard shortcuts such as Copy/Paste and Undo/Redo
- Import images for reference or textures
- Drawing decorative shapes

# Known bugs
- When moving an object with connections to other objects, the visualization of those connections does not immediately update.
- Connections between objects do not delete properly
- When adding a new vertex, it is sometimes placed along the wrong edge, leading to unexpected behavior.

# Authors and acknowledgment
Thanks to Daniel Haehn, who provided code that served as the base for this project, as part of his [CS460 - Computer Graphics course](https://cs460.org/) at University of Massachusetts, Boston.

Although I heavily modified much of the starter code for [Project 3](https://github.com/bostongfx/CS460student/03) for that course, the inspiration still remains, as does his scene setup code (and his click detection code, which was refactored into functions getCameraRaycaster() and getPointProjected()).

All the other code in this project was written by myself with the occasional assistance of the [Three.js documentation](https://threejs.org/docs/)
