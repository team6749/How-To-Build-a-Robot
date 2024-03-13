next up is game flow. Since we know where points can come from, and where they go we can use this to guess how a game might play out during all 3 different stages. This process is similar to strategy, but different in the sense that we are trying to guess potential strategies, and how they might affect how we would design the robot or play the game. At this point we would read in the manual where robots start during the match.

Here is the empty field layout
![[field layout empty.png]]

## Starting Configuration
The starting configuration of each robot is fully within its community not in contact with the charge station. Realistically that means that one robot can start on each side of the charge station and one robot behind the charge station, or behind the robot nearest to the scoring table (not pictured at the bottom of the image).

We will also note any safe zones like the community and area near the substations as robot contact with the opposing alliance is prohibited in these areas.

![[starting config.png]]

## Autonomous
Autonomous mode aka auto is the first period (usually 15 seconds) of an FRC game. Robots are entirely preprogrammed for autonomous, meaning they do not use any player-controlled code. Robots usually use utilities such as [Limelight](https://limelightvision.io), [PathPlanner](https://pathplanner.dev/home.html), or other resources to assist them in automating scoring game pieces and travel on the field.
at the start of auto the robots will likely opt to score a game piece that they had pre-loaded, then move to acquire more game pieces.
![[auto blue only.png]]
In this example I have one robot opt to dock on the station for the bonus points. The bottom robot goes to get pieces off of the floor, and the top robot travels across the map to get pieces from the substations. However something important happens with the top robot. Since the field is mirrored, the opposing alliance also wants to do the same thing. There is a clear area where collisions are likely to occur immediately after auto. We also notice that since the substation is the only place where where game pieces come from that there will be a lot of traffic. Lets see how the flow of robots could look during the match.

## Teleop
Teleop, the main period of player-operated robots involves team communication to drive to acquire game pieces and score them in nodes. 
![[match flow.png]]
If we draw out some potential paths we can see there can be a lot of conflicts during teleop in the center area. It appears that if scoring and driving and intake at the substations takes similar amounts of time that there could potentially be a nice flow of a robot driving, placing, and intaking; assuming nothing goes wrong (which it will). As we can see with the red side, even if 2 robots are queued at the same kind of spot, we could still avoid blocking teammates, and for scoring if we scored furthest from the outflow around the charge station first there would be minimal wait time, even if 1 robot is slow or having issues. It appears that planning ahead with the alliance partners on how to flow around the field will be important.

## Extra Notes
- a swerve chassis may be beneficial with the complex movement around the charging station
- A method of keeping track of which cones and cubes are scored where would be helpful so that the robot can determine where to score to maximize points and prevent accidental double scoring.
- The substation is on the opposite side of the field from where the driver station is, meaning that a way for the robot to signal to the substation which type of game element to deploy might be beneficial, maybe through lights.
- defense robots will be especially effective this year against robots that cannot go over the charging station.