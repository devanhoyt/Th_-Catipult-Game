# Th_-Catipult-Game

## Code Formating
To keep things orginized, here are the formating conventions for the code:
- Variables:  all lowercase using underscores to seperate words.  (my_varible)
- Classes: Prefrebly one word, capitilized.  (Engine)

## Filestructure
The game is composed primarily of three main files, with all other assets contained within the appropriate "Assets" sub folder.  The Core.py file conains the main game, while the game_settings.csv file works as long term storage for the game.  The game_save.csv file keeps track to run sespific elements of the game, tracking user informaion for future use.

## core.py Structure
The core.py file is structured into two main components, the Engine and the Interface.
- Interface:  The interface is responsible for managing all graphical elements, allowing the user to see into the game world.  This includes the game window (the section of screen that is the game), The room (the 'location' that the game is taking place in), and the camera (the secion of the room that is displayed at any given time)
- Engine: the Engine is responsible for handling all the elements that the user does not directly see.  Game objects, the Physics engine, and save/load systems all fall into this catagory.  


## Catapult Game states
### IDLE GAME STATES

Primed: Catapult is in its Primed position, without a rock loaded
Fired: Catapult arm is in its furthest deployed state.  
Loaded: As Primed, but a rock is on the launch arm

### ACTIVE GAME STATES

Fireing: While in this state, the catapult's arm swings out, launching a rock
Arming: While in this state, the catapult arm will slowly wind back until it reaches its "Primed" Position

###VIEWS
The game is set up with arcade views to change between the different levels and screens. To change levels or screens call the view class and call the setup function if applicable. There is a start view, level 1-3 view, victory view, and gameeover view. Each level has a setup function that is called which creates all the level objects and sets them up. The starting view incorporates a login system and the game overview incorporates a retry element. The victory view continues to the next level.
###LEVELS
Each level has an enemy slime(game_objective) that the player must hit to advance the game. 

### Other notes
there is a varable called "arm_game_state" and this referes to either "Primed" (a rock is loaded) or 
