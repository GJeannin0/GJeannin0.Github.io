# Grid System
![Grid](/images/grid.png)

## Context
As part of the 3rd bachelor year’s curriculum, students of the Games Programming section of the school are tasked with creating a video-game over the span of 7 months (end of september to end of april). We settled on the creation of a city builder we’ve named Voliday which can be found here: https://volcanoteam.itch.io/

At the begining of the project I was tasked to investigate what solutions were available to implement a grid system in unreal engine 4.

## The grid

During my research I considered that we could need thousands of tiles in a city builder, and I found an adequate solution on https://www.youtube.com/c/ReidsChannel and I decided to implement it on my side to test it out.

It consists of drawing produral meshes to create the shape of the grid. 

The shape of the grid is customizable, the size of lines, of tiles, height and length of the grid, it suits needs for any shape of grid we could use.
![Grid](/images/grid1.png)
![Grid](/images/grid2.png)

It also displays wich tile the cursor is pointing to.

It would have requiered more work to couple the grid with the tiles logic system but it could have been implemented. Unfortunately the grid wasn't implemented in the final project.
