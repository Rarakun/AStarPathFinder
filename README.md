# AStarPathFinder
Hosted the code made by http://www.csharpcity.com/reusable-code/a-path-finding-library/

## Sample Code

Below is some sample code to set up a simple grid, and detect if there’s a path between the elements of that grid.

```
using DeenGames.Utils.AStarPathFinder;

// Sample initialization code
int width = 5;
int height = 3;
width = PathFinderHelper.RoundToNearestPowerOfTwo(width);
height = PathFinderHelper.RoundToNearestPowerOfTwo(height);

byte[,] grid = new byte[width,height];
for (int i = 0; i < 8; i++) { for (int j= 0; j < 4; j++) { grid[i, j] = PathFinderHelper.EMPTY_TILE; } } // Create a grid like this (X = wall, . = free): // .X... // .X.X. // ...X. grid[1, 0] = PathFinderHelper.BLOCKED_TILE; grid[1, 1] = PathFinderHelper.BLOCKED_TILE; grid[3, 1] = PathFinderHelper.BLOCKED_TILE; grid[3, 2] = PathFinderHelper.BLOCKED_TILE; List path = new PathFinderFast(grid).FindPath(new Point(0, 0), new Point(4, 2));
if (path != null) {
// found the path!
}
```
