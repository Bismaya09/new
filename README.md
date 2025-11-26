Text Action  Game in C :

This is a simple command-based text action game written in C. The player is stuck inside a dark room and must explore, find a key, and escape through a locked door. The program demonstrates basic concepts such as loops, string comparison, conditional logic, and user input.

 Features :

Interactive command-based gameplay

Continuous game loop until escape

Unique:

ASCII movement animation

Simple inventory system (hasKey)



Gameplay Overview :

The player starts in a dark room and can enter commands:

Command	Description :

move -	Shows a walking ASCII animation
look -	Shows an old treasure chest
findkey	- Finds the key required to escape
explore	- Shows a locked door in the room
open -	Opens the door if key is found; ends the game
run	- Attempts to run but door is locked
other - Shows error message for unknown command

The game ends only when the player enters open after finding the key.

 Working Process :
 
1. Program Starts

The game welcomes the player and prints available commands.

Variable hasKey is initialized as 0 (key not found).

2. Infinite Game Loop

A while(1) loop runs continuously.

The player is prompted:

What do you want to do?

User input is collected using scanf.

3. Command Processing Using strcmp()

The program compares the typed command with all possible actions:

If command == "move" → prints walking ASCII figure.

If command == "look" → shows a treasure chest.

If command == "findkey" → sets hasKey = 1.

If command == "explore" → shows a locked door.

If command == "run" → shows that running is impossible.

If command == "open":

 a : If player has the key (hasKey == 1), the door opens and the loop breaks.

  b : Otherwise, shows “door is locked” message.

Any unknown command → prints error message.

4. Inventory System

The variable hasKey changes from 0 → 1 only when the player uses the findkey command.

This variable controls whether the player can open the door.

5. Game Ends

When the player enters open with hasKey == 1, the message:

You unlocked the door and escaped! You are free! is printed.

The loop ends using break.

Program finishes.

<img width="1701" height="1070" alt="Screenshot 2025-11-24 141932" src="https://github.com/user-attachments/assets/06f35035-3f1d-46d2-8e90-262ec7ea3cf5" />
