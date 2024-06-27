# Breakout Ball Game
Welcome to the Breakout Ball Game project, a classic brick-breaker game developed in Java using the Swing framework. This game challenges players to break all the bricks with a ball while controlling a paddle at the bottom of the screen.
## Features
* **Classic Gameplay:** Enjoy the timeless brick-breaking action with a modern twist.
* **Dynamic Difficulty:** The game's difficulty increases as you progress, offering a challenging experience for players of all skill levels.
* **Customizable Brick Layout:** Utilize the ```MapGenerator``` class to customize the layout and difficulty of the brick arrangement.
* **Scoring System:** Keep track of your score with each brick you break. Aim for the high score!
* **Restart Option:** Easily restart the game after winning or losing by pressing the Enter key.

## Details
* **Java Swing Framework:** The game's graphical user interface is built using the Java Swing framework, ensuring a smooth and responsive gameplay experience.
* **Collision Detection:** Advanced collision detection mechanics between the ball, the paddle, and the bricks, providing accurate and realistic gameplay.
* **Game Loop:** A game loop controlled by a ```Timer``` ensures consistent game updates and rendering.

## How to Run
To play the Breakout Ball game, follow these steps:

1. Ensure Java is installed on your system.
2. Download or clone this repository to your local machine.
3. Navigate to the directory containing the game files.
4. Compile the ```Main.java``` file using the Java compiler: 
```bash 
javac Main.java 
```
5. Run the compiled ```Main``` class with Java:
```bash
java Main
```

## Game Controls
* **Left Arrow Key:** Move the paddle left.
* **Right Arrow Key:** Move the paddle right.
* **Enter Key:** Restart the game after a win or loss.


## ```Main.java``` Overview
The ```Main.java``` file is the entry point of the game. It sets up the game window and initializes the ```Gameplay``` class, which contains the game's logic. Here's a brief overview of what happens in ```Main.java```:

* A ```JFrame``` object is created to serve as the main window.
* The window's dimensions are set, and it's made non-resizable.
* The title of the window is set to "Breakout Ball".
* The default close operation is set to exit the application.
* An instance of ```Gameplay``` is added to the frame.
* The frame is made visible to start the game.

## ```Gameplay.java``` Overview
The ```Gameplay.java``` file is the core of the Breakout Ball game, implementing the game mechanics, graphics, and controls. Here's an overview of its functionality:

* **Game Initialization:** Initializes the game state, including the map of bricks, paddle position, ball position, and game status flags.
* **Graphics Rendering:** Handles all the drawing operations for the game, including the background, paddle, ball, bricks, and text for scores and game status messages.
* **Game Logic:** Contains the game loop and logic for moving the paddle, bouncing the ball, and detecting collisions with the paddle, bricks, and walls.
* **Score and Level Management:** Manages the player's score and tracks the number of bricks remaining to determine game over or victory conditions.
* **User Input Handling:** Listens for keyboard events to control the paddle and restart the game after a win or loss.

    #### Key Components:

* **Paddle and Ball Movement:** Allows the player to move the paddle left or right using the arrow keys and calculates the ball's movement, including bouncing off walls, the paddle, and bricks.
* **Collision Detection:** Implements collision detection between the ball and the paddle, the ball and the bricks, and the ball and the game area boundaries.
* **Game State Transitions:** Manages transitions between different game states, such as starting, playing, winning, and losing, including resetting the game state for a new game.

This class leverages Java Swing for rendering the game's GUI and handling user input, making it a comprehensive implementation of the Breakout game mechanics.

## ```MapGenerator.java``` Overview
The ```MapGenerator.java``` file is responsible for generating and managing the layout of bricks in the Breakout Ball game. It provides the functionality to create a grid of bricks, draw them on the screen, and modify their state during gameplay. Here's a detailed overview of its features and functionalities:

* **Brick Grid Initialization:** The constructor ```MapGenerator(int row, int col)``` initializes a 2D array representing the grid of bricks. Each brick's presence is indicated by setting its value in the array to 1. The size of the grid is determined by the ```row``` and ```col``` parameters, allowing for customizable levels of difficulty and complexity.
* **Dynamic Brick Sizing:** Based on the number of columns and rows specified, the class calculates the width and height of each brick to ensure they fit evenly across the game area. This dynamic sizing helps maintain the game's visual consistency across different levels or screen sizes.
* **Brick Drawing:** The ```draw(Graphics2D g)``` method is responsible for rendering the bricks on the screen. It checks each element in the brick array; if a brick is present (value > 0), it draws a rectangle in the specified position. The method uses Java's ```Graphics2D``` class to set the color and stroke of the bricks, creating a visually distinct grid.
* **Brick Collision Handling:** The ```setBrickValue(int value, int row, int col)```method allows the game logic to update the state of a brick when hit by the ball. By setting the value of a brick to 0, the brick is effectively "destroyed" and will no longer be drawn on the screen, allowing for the game's progression.
* **Visual Enhancement:** The class includes additional drawing commands to outline each brick, enhancing the game's visual appeal and making it easier for players to distinguish between individual bricks.

This class is a key component of the Breakout Ball game, enabling the creation of varied and challenging levels by simply adjusting the grid's dimensions and the state of individual bricks.
## Contributing
Contributions to the Breakout Ball game are welcome! Feel free to fork the repository, make your changes, and submit a pull request.