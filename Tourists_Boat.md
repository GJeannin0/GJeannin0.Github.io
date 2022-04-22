# Tourists Boat
![boat](/images/boat.png)

# Context
As part of the 3rd bachelor year’s curriculum, students of the Games Programming section of the school are tasked with creating a video-game over the span of 7 months (end of september to end of april). We settled on the creation of a city builder we’ve named Voliday which can be found here: https://volcanoteam.itch.io/

During this project I was tasked to implement the boat that would bring tourists to the island.

### Task requierments

The boat was deisgned to arrive at a harbour placed anywhere on the island at regular intervals, it would then make a stopover, deliver the tourists and then leave the island. So I have to make the boat come in a straight line to the island in a direction depending of where the harbour is placed on the island.

### My approach

![schemeBoat](/images/schemeBoat.png)

In order to do this I calculate the direction from the harbour to the center of the island and rotate the boat in that direction, make it spawn at a set distance from the island, then move it to the harbour in a straight line.

I'd then use a timer to set the stopover duration, spawn the tourists, and then move the boat in the opposite direction to leave the island before being destroyed.

The task sounded easy enought not to use a behavior tree but afterwards it could have been faster to use one, even for the simple process of dropping tourists to the island and leaving.

### Challenges

I ended up having multiple issues on this task, I had trouble finding and using the move to function of unreal engine 4 for pawns, locate the harbour position, not to arrive in the island but in the harbour ...
I had to debug to solve some on these issues, like spawning the tourists on the island and not on the harbour.

I also managned to simplify the process by starting the timer when the boat spawns, add the travel time to the stopover time, and spawn the tourists at the end of this timer, just before the boat starts leaving the island.

### Conclusion

Working on this task helped me learn more about unreal engine 4 and especialy its debgging tools that I luckily didn't have to use much before this. And it made me think more of using the built in AI methods even for a small task.

