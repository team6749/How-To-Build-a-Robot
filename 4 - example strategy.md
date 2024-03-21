## Intro
this is the point where we will start making design decisions, this is where iteration will happen the most. Especially since there are many valid angles to take when designing a robot. What i like to consider is robots that follow trade-offs of the main scoring objectives at a high level noting the pros and cons. **By analyzing the different scoring objectives and their ultimate value to the came, we can analyze what trade offs need to be made when designing.** Let's consider some hypothetical robots.

When calculating point scoring I will use the average point each piece is worth (3.3)
Also, when picking these numbers, I am using past experience with how "good" robots typically are, top level robots will excel at all things, also considering how many points are available vs scorable can get a good idea of what a typical robot might be able to do. Try to use comparably complex robots when deciding how to pick which way design your robot at a high level.

Creating these numbers is an involved process and requires understanding of the game and capabilities of the team, and the capability of other teams. They will never be accurate and could vary significantly. The point of this here is to consider the viability of certain scoring techniques versus the complexity of the scoring. It requires intuition which is not innate.

scoring only robot:
- Efficient at scoring, so they can reliably score 3 links, and 9 pieces (scores until the end of the game)
- can pick pieces off of the ground and can take full advantage of the 4 starting pieces on the field.
- has complex vision for placing and retrieving pieces quickly
- can score top middle and bottom due to complex arm assembly
- Designed to move quickly across the field, but cannot go on the charging station easily
CONTRIBUTION:
15 link points
30 high piece points
= 45 total points

balancing only + defense robot:
- Has code to automatically balance the platform during auto, does it consistently.
- The robot has a low center of mass and is heavy allowing it to block opponent robots in the zones of high contention. (ref 2. game flow). The robot can increase the opponent cycle time by about 3 seconds per robot. This would result in about 3 less scored pieces and 1 less scored link.
- This robot has a special deployable lift that another robot can drive on and can hold up the robot to allow 3 robots to be climbed at the end of the game
- This robot can only push around game pieces already on the ground, limiting it to the bottom row and scoring at most a few pieces per game, but defending is usually worth more points.
CONTRIBUTION:
12 auto park
10 scoring points
5 link points
10 self park points
10 alliance park points (sometimes)
= 37-47 total points

robot of all trades:
- This robot can score 6 pieces and 2 links; however it can only intake from the substation.
- This robot can drive up the charging station but it might not be able to balance it reliably, and cannot do it in auto.
CONTRIBUTION:
10 link points
20 scoring points
10 endgame docking points
= 40 toal points

These are the three main categories that you can usually design. However there are usually permutations, like cubes or cones only; only scoring cubes because you can shoot them like balls; top middle bottom scoring; or levels of climbing, or robots that cant score, but only move pieces for other robots to score (this is usually not effective).

Your robot design will usually not align perfectly with any of these archetypes but these will help you align your design decisions. The more combinations of scoring that you can find and estimate, the better idea you will have on how to make a robot that is reasonable and effective. The point value contribution of all of these robots are close, but you can pick more exactly what to do to optimize time+complexity versus point gain and reliability. 