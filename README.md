# Mobius-Conquer
In the Mobius Conquer battle the players fight for positions on a möbius strip, created from a rectangular field by giving it a half-twist, and then joining the ends of the strip along its height to form a loop. Both sides of the field are divided into cells, some of which are marked as impassable (note that positions of the players are not considered impassable). A player is said to control a cell if the cell is closer to him in terms of shortest paths on the strip.

The Mobius Conquer battle is almost over: ratiorg and his enemy have both reached their final positions. The only thing to do now is to determine the winner. Given the coordinates of both players, coordinates of the impassableCells and the size of the field, calculate the number of cells controlled by each player.

[input] array.integer field

Array of two integers, the size of the field. The first element is its height, and the second one is its width.

Constraints:
field.length = 2,
1 ≤ field[i] ≤ 100

[input] array.integer ratiorg

Ratiorg's position as an array of three integers. The first integer defines the side of the field (either 0 or 1), the second one defines the row, and the last one defines the column (both 0-based).

Note, that the row and the column of the second side of the field is defined assuming that the first side of the field was flipped vertically.

Constraints
ratiorg.length = 3,
0 ≤ ratiorg[0] ≤ 1,
0 ≤ ratiorg[1] < field[0],
0 ≤ ratiorg[2] < field[1].

[input] array.integer enemy

The enemy's position in the same format as ratiorg. It is guaranteed that ratiorg ≠ enemy.

Constraints
enemy.length = 3,
0 ≤ enemy[0] ≤ 1,
0 ≤ enemy[1] < field[0],
0 ≤ enemy[2] < field[1].

[input] array.array.integer impassableCells

Array of impassable cells, where each cell is given in the same format as ratiorg and enemy. It is guaranteed that all impassable cells are unique, and that no impassable cell coincides with ratiorg or enemy.

Constraints
0 ≤ impassableCells.length < 2 · field[0] · field[1],
impassableCells[i].length = 3,
0 ≤ impassableCells[i][0] ≤ 1,
0 ≤ impassableCells[i][1] < field[0],
0 ≤ impassableCells[i][2] < field[1].

[output] array.integer

Array of two integers, where the first integer is the number of cells controlled by Ratiorg, and the second one is the number of cells controlled by his enemy.
