## overview
quick overview on how i would approach designing autos for the 2024 season. firstly there are 8 notes on the field, 3 preloaded into robots and you can place your robot anywhere along the close zone. our robot shoots up against the speaker (s1,s2,s3) and 3 robots can fit. there is stage, 3 close notes which cannot be grabbed by the opponent alliance, and 5 notes in the middle up for contention.

## "Greedy" Auto
we might have 3 strategies for auto, firstly, being an all in **selfish scoring auto**, which grabs every note and tries to maximize the number scored without regard to our alliance member robots. this is ideal for when your robot is the most capable robot on the alliance.

here is an example of a selfish auto. it scores up to 5 notes including the preloaded note! it just slurps up everything in its path!

`Using pathplanner screenshots from 2024`
![[5 note auto.png]]

now we might want to consider the order in which we slurp. a conservative strategy, one that tries to maximize points at all cost, might pick this as the ordering. This is to take the paths with the least risk first. **so the preloaded note does not move. so it is done first. then we do straight forward as its the closest. then we go up (which starts to have risk of interacting with alliance members), then down, which might hit the stage. lastly it does the note in the middle because it does not want to risk getting bumped by another robot**, its also maybe the path that is pushed to the highest speeds and might have tracking issues. so it is done last.
![[5 note auto numbered least risk.png]]
a more aggressive auto might go for the middle notes first, because we want to avoid the risk of an opponent robot going for that middle note at the risk of the rest of the auto failing losing out on half the points. but the risk might be worth it
![[5 note auto numbered risk.png]]

## Zone Based Autos
now lets talk about zones

specifically, autos that work with our alliance members. one robot cant do everything as fast as 3 robots can do the same thing as long as you divide and conquer

here are the **3 zones of responsibility** i might pick for this game. **each robot is responsible for the notes within their area.** any notes that are shared across the boundary (notes 5 and 7 in this image) have 2 robots in responsibility

### Zones Division Image
![[2024 3 zones.png]]

a team might also want to build up autos that work in 2 responsibility zones. **for instance, you could have an auto that does notes in zones 1-2 or 2-3**

the reason to have zones of responsibility is to avoid collisions and crossover

`typically the more selfish an auto the more zones it will cover. the auto pictured above, actually interacts in all 3 zones`

here is an example of a robot (254 cheesy poofs at Sacramento regional, running a selfish 6 note auto during qualifications. also notice how they shoot notes towards their side after auto ends. this could potentially be an entire auto strategy. generally its not worth it in terms of points to do that, because points are amplified in auto, but running and messing up notes 4-8 might be worthwhile against an opponent who scores all of the notes in the middle if you're not able to score as fast, and you have other robots on your alliance scoring) [https://www.youtube.com/watch?v=vA5vdtO_ypQ](https://www.youtube.com/watch?v=vA5vdtO_ypQ "https://www.youtube.com/watch?v=vA5vdtO_ypQ")

here is a finals match in the same regional. notice how the robots respect the general 3 zones and divide up the work? Robot 2 (the one in front of the speaker directly) does not even move because 254s auto did notes in zone 1 AND 2. these compatibilities are super important in alliance selection. you will want to design autos to be selfish (so that you can run them in qualification with robots that arent as capable), and also cooperative autos which respect reaonsable zone boundries so that you can maximize the compatibility with other teams. [https://www.youtube.com/watch?v=Bh5pfoohpTA](https://www.youtube.com/watch?v=Bh5pfoohpTA "https://www.youtube.com/watch?v=Bh5pfoohpTA")

on the blue side of this match the robot in zone 1 on the blue side did not move to allow for the robot to work zones 1 and 2 as well