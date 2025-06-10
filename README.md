# Wumpus_world_logical_agent
The logic behind this Wumpus World game works using both Python and Prolog. Python handles the interface and overall flow, while Prolog is used to process logical reasoning and decision-making based on rules.
Wumpus World Game Logical Agent

Aim:
       To simulate the Wumpus World environment using a logical agent that interacts with a 4x4 grid, avoiding hazards (Wumpus and pits), collecting gold, and returning safely to the starting position. The implementation uses Prolog for logical reasoning and Tkinter for a graphical user interface.

Objective:
1.	Develop an interactive GUI-based Wumpus World game.
2.	Utilize Prolog to manage game logic, state, and percepts.
3.	Enable player actions such as moving, shooting, grabbing gold, and climbing out.
4.	Provide real-time feedback on percepts (breeze, stench, glitter) and game metrics (score, moves).

Facts:
1.	Grid Layout: 4x4 grid with the agent starting at (1,1).
2.	Hazards:
o	Wumpus at (4,4).
o	Pits at (1,4) and (3,1).
o	Gold at (3,3).
3.	Adjacency: Squares are connected horizontally and vertically (e.g., (1,1) is adjacent to (1,2) and (2,1)).
4.	Percepts:
o	breeze/1: True if the current square is adjacent to a pit.
o	stench/1: True if the current square is adjacent to the Wumpus.
o	glitter/1: True if the gold is in the current square.



Rules:
1.	Movement:
o	The agent can move to adjacent squares.
o	Entering a pit or the Wumpus's square results in death.
2.	Shooting:
o	The agent can shoot an arrow in one direction (up, down, left, right).
o	Killing the Wumpus removes all stench percepts.
3.	Gold Collection:
o	Grabbing gold increases the score.
o	Climbing out at (1,1) with the gold wins the game.
4.	Scoring:
o	Collecting gold: +1000 points.
o	Dying: -1000 points.
o	Each move: -1 point.
o	Shooting an arrow: -10 points.
