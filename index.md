# SUPER SMASH VOLLEY-BALL GDD

## Pitch

Super Smash Volley-Ball is an online 2D game where stickmen play volley-ball together.

## Gameplay 3C

### Character
The game is playable on pc, each player control his stickman using directionnal keys and the space bar.
The terrain is flat with a vollayball net at the center.

### Controls
Each stickman can move by going left, right and by jumping using the according keys and space to jump. 
Each stickman have 2 ways of hitting the ball, they can perform a forearm blow and a smash on the ball using repspectively up and down keys.
![Volley1](/images/volley1.png)
![Volleyball](/images/volleyball.png)

A game is won by winning 3 rounds, a round is won when the ball hits the ground on a side of the terrain, giving one point to the player of the opposite side.
At the beginning of each round the ball spawns above the engaging player.

### Camera
The camera will show the whole terrain all the time, and will shake when a player smashes the ball.

## Network challenges

The main challenge is making sure the state of the game is the same for every player.
SSVB uses the rollback system of the neko engine for its networking.
It works using a single server and clients connecting to it, only the server controls the state of the game using the inputs sent by the clients.  

The interactions between players will be focused around the ball, thus letting some time for the ball to reach the other side of the field and helping delay issues in case of high latency.

