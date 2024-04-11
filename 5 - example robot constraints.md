
## Introduction
This process is the one which the most time will be spent, and is only 1 step away from realizing the robot. Multiple iterations, and different designs are important to refine and pick the best possible one. We will use all of the information we have gathered to start picking real numbers and constraints here!

I will create a summary of objectives and goals of what my hypothetical design is first. The final document below will have been modified and tinkered with many times, maybe a specific goal changes slightly, or gets removed, or added before I am happy with my final constraints. Also testing prototypes and futher refinement will change the final robot design, but the constraints should be things that are fairly constant, like the angle required to climb up the charging station this year.

## Constraints for bucket bot
after considering scoring and things I will attempt to design a robot that is based on the balance/defend robot archetype; however I think we can also make it extremely productive by scoring bottom pieces using a bucket mechanism because it should be fairly easy to implement and we can get pieces from the single substation by sitting under it and dropping pieces onto it. I want to focus on scoring low as part of the game, but defense is also an option if the bucket isnt reliable (Notice the easy fallback design to help the robot be effective at every step of development, not just at completion or if everything is ready). I want the robot to have some code to **balance the platform**, and some sort of a forklift style contraption to climb other robots in endgame off of the edge of the charging station, **ideally a last second climb so it can score for as long as possible.**

Following the estimates I made before. During auto I plan to have the robot dump a piece into the low section and then immediately level the charging station. This is the only auto I plan to do, and I will rely on other teammates to do other scoring. During teleop I want to score 5 at least game pieces into the lower section from the single substation. However my priority is endgame, where I want to have a leveled charge station. This flexibility will allow for all 3 robots to easily climb. 
Estimated contribution each round:
12 auto level
3 auto bottom game piece (1)
10 bottom game pieces (5)
10 for links (2) 
10 endgame climb
10 endgame alliance partner climb
**= 55 minimum points of contribution each match; 45 if no alliance partner climbs**
+13 for max game piece scoring and another link

list of robot functions, which we can use to define the constraints, and are constraints on their own:
- Score low using a bucket that tips over the edge
- collect game pieces from the single substation into the bucket
- have a lift mechanism that can deploy off of the edge of the robot to climb on an alliance partner over the edge of the charging station
- automatically level the charging station during auto and ideally during endgame

Now we can start looking at real constraints

Auto leveling constraints:
- Bumper to wheel clearance of at least 35 degrees to climb onto the charging station reliably when it is already level.
- Accelerometer to automatically level the robot during auto
- The center of mass of the robot needs to be low if possible for stable climbing

Scoring cubes and cones lower constraints:
- vision or sensor solution to quickly score points or align to the single substation. It does not need to be insanely accurate. Our smallest scoring zone is 48cm wide. And our largest game piece is a sideways cone which is 33cm. This means we have 26cm of margin to score (2/3 overlap of game piece and scoring zone).
- To collect the game pieces from the single substation which drops pieces from 69cm tall, we need a bucket. The single substation is 58cm wide, so we will try and accomodate that width; but maybe we can have the human player push the game piece along the edge.
- Our bucket needs to be large enough to hold 1 game piece in it, lets say it needs to be 2/3 height of the cube 24cm, and as wide as a sideways cone 33cm plus our positioning margin (26cm) minus our overlap margin (21cm). The depth of the bucket needs to be at least the max game piece length of 33cm. (drop test video https://www.youtube.com/watch?v=pVI7ZZcx7eo)
- The bucket will be positioned such that the pieces will reliably fall into the bucket when dropped from the substation. This is likely upwards and near the edge of the robot.
- The bucket needs to be at least 5 inches from the ground at its lowest point due to the height of the edges of the hybrid nodes.
- The bucket needs to rotate enough that it can reliably drop any game piece. This likely means we need greater than 90 degrees of rotation. A motor is probably appropriate to rotate our bucket versus a piston.
- The bucket needs to follow the exension limits of 48in and only on 1 side of the robot.
- The shape of the bucket should encourage the pieces to center and prevent them from leaving.

Constraints to pick up an alliance partner for the assisted climb.
- Our climb mechanism must fit between the top of the charging station and the bottom of the robot, meaning it needs to be 9.125in off of the floor.
- Our climb mechanism must avoid the cable protector on the field.
- We must have a long enough attachment to go under at least half of our alliance partner.
- The climbing mechanism needs to be tall enough to avoid any weird cantalevering for a stable climb
- The mechanism needs to be spaced wide enough that it can easily balance. Lets say at least 5in apart
- The fork must not be slippery to avoid slipping out of the alliance partner during the climb
- Our robot needs to be as light as possible to avoid needing strong motors.
- Our lifting mechanism must rotate enough to have the robots center of mass cross over the top to avoid requiring a mechanism to keep the robot in place after being disabled at the end of the match. This will directly conflict with the ideal low center of mass!