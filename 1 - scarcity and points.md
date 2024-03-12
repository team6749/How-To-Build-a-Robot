Firstly we will skip to section 6 (match play). This is where we should start reading. Since we will be optimizing our robot for points, lets see what the game pieces are this year. It is important to understand where points come from.
- There are 54 cones and 44 cubes total
- Each robot can start with 1 piece
- 4 pieces are located on the field at the beginning alliance choice (OPTIONAL!)
- The remaining pieces are staged at each alliance. (20-27 cones, and 15-22 cubes per alliance)
![[field layout empty.png]]

Next lets identify **scarcity**. In this game its fairly easy, since there are a certain amount of pieces and a certain amount of places that they can be placed so we can determine scarcity across an entire match. We will skip to 5.5 GRIDS to determine where scoring can occur
- There are 3 grids
- Each with 3 hybrid nodes, 2 cube nodes, and 4 cone nodes
- Hybrid nodes can be accessed by pushing pieces across the floor, and cubes or cones can count
- There are 6 cube ONLY nodes, 12 cone ONLY nodes, and 9 nodes that can accept cubes or cones (hybrid)
We can notice that there are 27 cones which cover cone only nodes 2:1, and cubes which are covered 2:1. This means that game pieces are not scarce this game, scarcity will only come from where we acquire them. We also know that we get points for 3 scored pieces in a row creating a link (6.4.1). This means we need to score 2 cones and a cube. Scoring both game pieces is going to be advantageous this game with cones probably being a priority unless we only go for hybrid nodes, and they both might be able to be scored in similar ways given their similar heights and placements. 

How do we aquire game pieces? Well we know that they can come from the floor, and reading 5.6 they can come from substations. There is a double substation which provides a cube or cone at a similar height to the high nodes on each grid, and the single substation which can drop pieces on the ground. We specifically notice how similar the double substation is in height to the high nodes, and the orientation of the cubes and cones being similar to how we would want to score them. Pieces that come out of the single substation will fall and land in an unpredictable spot and location. This is immediately less desirable, since it provides no benefit to use the single substation versus the double substation in terms of scarcity. The single substation is slightly closer to the scoring area, and you can load multiple pieces into the ground ahead of time; though this advantage is likely to be lost due to the double substation having vision targets for easy robot alignment meaning a quick intake is likely. We also notice that game pieces from the single substation could block access to the double substation. Note how i am trying to keep use of relative numbers to keep the analysis abstract for now.

Now we know where the game pieces come from, and where they go, lets check out the other ways that we can score points. 5.4 the charge station is the other primary objective. The charge station is an elevated platform that has 2 sides with sliding slopes. Scoring happens on these conditions. Note how I am not considering the amount of points for scoring on any objective yet. That will be considered after we understand how each objective works.
- A robot (max) is on the platform and level at the end of auto
- and points for each robot docked and or engaged at the end of teleop. (up to all robots)
Ideally we want 1 robot at the end of auto, only one team needs to do this but it also might be difficult since going up a slidy ramp and leveling the robot can cause odometry to be lost due to wheel slippage and make it hard to reliably do. We will notice that the charging station is only 96in wide, meaning that we can only realistically fit 2 robots on the platform. There will be scarcity in terms of how many robots can realistically fit on the platform. Something we might consider in our robot design is a smaller size, or a mechanism to climb onto or on another alliance robot over the edge of the station towards the community. We understand that 3 docked robots will be scarce unless design decisions are taken. We may choose to consider the amount of points earned by doing both kinds of climbs too much this, or accept it later into the robot design process.


potentially notable details:
- There are about 2x more cones than cubes
- The double substation intakes at a similar height to the high scoring locations and has vision alignment
- Docking in auto may be difficult due to the moving platform
- Only 2 robots can realistically fit on the charge station at once