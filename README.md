# Cave-of-the-Dragon-s-Gold-
 
A compact text adventure inspired by Colossal Cave Adventure (ADVENT). Explore a small underground world, solve simple puzzles, fight the dragon, and bring the treasure back to the building to win.

Files

- `adventure.py`: Python 3 version of the game logic, played in the terminal.
- `adventure_ui.html`: Browser version with a clickable compass, action buttons, item buttons, and a scrolling log. Open it directly in any modern browser.
- `adventure.html`: Standalone HTML version.

Running the Game

### Python

Requires Python 3. No extra packages are needed.

```bash
python3 adventure.py

HTML
Open adventure_ui.html in a web browser. No server or build step is needed.

Commands
Command	Action
GO <direction>	Move north, south, east, or west (or use N/S/E/W).
LOOK	Describe your surroundings.
GET <item>	Pick up an item in the room.
DROP <item>	Leave an item in the room.
FILL LAMP	Use one oil to refill the lamp to full.
INVENTORY	List what you are carrying and how many lamp turns remain.
KILL DRAGON	Attack the dragon. You need the sword.
XYZZY	Teleport between the building and the cave.
HELP	Show the command list.
QUIT	Exit the game (Python version only).
Map Layout


            [Treasure]
                |
   [Building]  [Dragon]  <- north passage from the cave
        |          |
        |      [Cave]
        |          |
     [Road] --- [Pit]
Road: Start here. The sword is on the ground. The building is north, the pit is east.
Building: Contains the lamp and a flask of oil. Connected to the road to the south.
Pit: Dark. Contains a gem. Leads north to the cave.
Cave: Dark. Contains gold. The dragon blocks the passage north.
Dragon's lair: Dark. The dragon must be killed before you can pass.
Treasure chamber: Dark. Holds the treasure.
Key Items
Lamp: Needed to see and take items in dark rooms. Burns for 40 turns before it runs out.
Oil: Refills the lamp. Each flask is used up when you run FILL LAMP.
Sword: Required to kill the dragon.
Gem and gold: Collectible treasures.
Treasure: Bring it back to the building to win.
Lamp Timer
The lamp starts with 40 turns of light.
Each successful GO, GET, DROP, or KILL uses one turn.
A warning appears when 5 turns remain.
When the lamp runs out, dark rooms stay dark until you refill it with FILL LAMP.
Winning the Game
Pick up the treasure, carry it to the building, and drop it there. The game ends with a victory message.

Notes
The HTML version includes oil and FILL LAMP. The Python version currently has the 40-turn lamp timer but does not yet include oil refills.
Commands are not case-sensitive.




