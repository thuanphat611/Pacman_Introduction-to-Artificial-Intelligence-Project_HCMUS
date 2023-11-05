### Introduction
![Pacman game example image.](/Docs/example.png)
You are given a file that describes Pac-man World. Suggest or implement
algorithms to assist Pac-Man in finding food without getting killed by monsters.
In the game Pac-Man, both Pac-Man and the monsters are constrained to moving in four
directions: left, right, up, and down. They are not able to move through walls. The game is
divided into four distinct levels, and each level has its own set of rules.
- Level 1: Pac-Man is aware of the food's position on the map, and there are no
monsters present. There is only one food item on the map.
- Level 2: Monsters are stationary and do not move around. If Pac-Man and a monster
collide with each other, the game ends. There is still one food item on the map, and
Pac-Man knows its position.
- Level 3: Pac-Man's visibility is limited to its nearest three steps. Foods outside this
range are not visible to Pac-Man. Pac-Man can only scan the adjacent tiles within
the 8 tiles x 3 range. There are multiple food items spread throughout the map.
Monsters can move one step in any valid direction around their initial location at
the start of the game. Both Pac-Man and monsters move one step per turn.
- Level 4 (difficult) involves an enclosed map where monsters relentlessly pursue
Pac-Man. Pac-Man must gather as much food as possible while avoiding being
overtaken by any monster. The monsters have the ability to pass through each other.
Both Pac-Man and the monsters move one step per turn, and the map contains a
multitude of food items.
The calculation of game points follows these rules:
- Each movement deducts 1 point from your score.
- Collecting each food item awards you 20 points.
### Specifications
**Input:** The given graph is represented by its adjacency matrix, which is stored in the input
file (e.g., map1.txt). The format of the input file is as follows:
- The first line contains two integers N x M, indicating the size of the map.
- The next N lines represent the N x M map matrix. Each line contains M integers.
The value at position [i, j] (row i, column j) determines the presence of a wall, food,
or monster. A value of 1 represents a wall, 2 represents food, 3 represents a monster,
and 0 represents an empty path.
- The last line contains a pair of integers indicating the indices of Pacman's position
(indices start from 0).

\
**Output:**
- It is recommended to utilize a graphic library for displaying the results.
- If a graphical display is not used, the result can be stored in a text file, such as
result1.txt. The file may include the pathfinding for Pacman, the path length, and
the game points. Each step of movement can be displayed individually or all steps
can be displayed on a single map. However, when monsters are able to move, steps
must be clearly separated.
