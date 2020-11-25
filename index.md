# SUPER SMASH VOLLEY-BALL Technical Document

## Pitch

Super Smash Volley-Ball is an online 2D game on PC where stickmen play volley-ball together.

## Gameplay

Each player controls a stickman that can move left and right, serve, and hit the ball.
Players respectively use arrow keys + ctrl and WASD + spacebar.
Spacebar/control is for engaging, it spawns the ball on the side of the serving player.

Stickmen do rotate when they accelerate, because it looks more fun.
Stickmen move by accelerating towards the left or the right and their speed is capped to a maximum speed.
Stickmen are bound to the field's borders and cannot move outside of it.
The ball has ballistic movement and is also bound to the field's borders.

Stickmen automaticaly hit the ball each time they contact the ball.
Players score a point when the ball hits the ground on the opposite side. (Note : Points currently aren't registered when scored)
The first player to score 3 points wins the game.

The camera shows the whole terrain all the time.

![Volley1](/images/volley1.png)

## Network challenges

The main challenge is making sure the state of the game is the same for every player.
SSVB uses the rollback system of the neko engine for its networking.
It works using a single server and clients connecting to it, only the server controls the state of the game using the inputs sent by the clients.  

The interactions between players are focused around the ball, thus letting some time for the ball to reach the other side of the field and helping delay issues in case of high latency.
High latency only causes others players to teleport when changing direction, and the game keeps running without issues despite that.

I started making the game by working from the asteroid game.
Tweaking elements to better understand how the rollback system works.

From there I managed to implement my own features, ballistic trajectory, acceleration, map borders.
I couldn't implement all the features I originaly wanted in the given time, so I focused on getting a minimum viable product looking like a Tennis for two clone.

## Flaws and possible Improvements

Additional features like smash, screenshake and jump.
The point system currently doesn't work properly.
The MVP gameplay is here, but the game doesn't tell when a player scores a point or who's turn it is to serve.
This allows players to spawn volley balls whenever they want. 
High latency can cause lots of teleporting when a lagging player keeps alternating left and right, resyncs could be more fluid.

The field is unclear, the borders are not showing and there is no net in the middle.
There could be sprite changes when a player changes direction or hits the ball.
