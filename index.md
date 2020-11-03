# SUPER SMASH VOLLEY-BALL GDD

## Pitch

Super Smash Volley-Ball is an online 2D game where stickmen play volley-ball together.

## Gameplay 3C

### Character
The game is playable on pc, each player control his stickman using directionnal keys and the space bar.

### Controls
Each stickman can move by going left, right and by jumping using the according keys and space to jump. 
Each stickman have 2 ways of hitting the ball, they can perform a forearm blow and a smash on the ball using repspectively up and down keys.
![Volley1](/images/voley1.png)
![Volley2](/images/voley2.jpg)

A game is won by winning 3 rounds, a round is won when the ball hits the ground on a side of the terrain, giving one point to the player of the opposite side.
At the beginning of each round the ball spawns above the engaging player.

### Camera
The camera will show the whole terrain all the time, and will shake when a player smashes the ball.

## Network challenges

SSVB's will use the rollback system of the neko engine for its networking.
The interactions between players will be focused around the ball, thus letting some time for the ball to reach the other side of the field and helping delay issues in case of high latency.
