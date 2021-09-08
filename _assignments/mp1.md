---
layout: assignment
title: "Your First Game: An Infinite Matrix"
index: 10
due: "Sept. 24, 2021 @ 11:59 PM"
material: ~
points: 40
rubric:
-
    name: Complete the tutorial
    points: 5
    description: Have working code that matches the functionality described in the tutorial
- 
    name: Health system
    points: 5
    description: Display and track a player health metric
- 
    name: Score system
    points: 5
    description: Display and track a game score
-
    name: Health packs
    points: 5
    description: Spawn health packs that can be picked up 
- 
    name: Speed increase
    points: 5
    description: Gently increase player speed over time
-
    name: Enemies
    points: 5
    description: Spawn enemies...the visual representation is up to you.
-
    name: Player projectile attacks
    points: 5
    description: Add a player controllable projectile weapon
-
    name: Creative addition
    points: 5
    description: Modify the game aesthetic in some way 

---
![Matrix](https://github.com/illinois-cs498gd/illinois-cs498gd.github.io/raw/main/img/matrix.PNG){:width="800px"}

## Specification
For your first programming assignment, in honor of Keanu Reeves turning 57 years old and the upcoming release of Matrix 4 Resurrections you will implement a simple Matrix-themed game.  The goal here isn't to build a AAA game...it's probably not going to look amazing and that's fine. The goal is to learn to build an Unreal project from nothing and make an actual working game that expresses some creativity. And in any case, your game will likely be more entertaining than the Matrix sequel movies. 

![Matrix](https://github.com/illinois-cs498gd/illinois-cs498gd.github.io/raw/main/img/matrix-4-5.png){:width="800px"}

Your task is to do the following:

### 1. Complete the Tutorial:<br/>
Complete this [tutorial on making a simple game by Ray Wenderlich](https://www.raywenderlich.com/454-how-to-create-a-simple-game-in-unreal-engine-4). Do not skip the tutorial and just grab the finished code; complete the tutorial. It teaches almost all of what you need to know to implement the additional features below (features that are not included in the finished tutorial code posted at the site).

### 2. Add a health system for the player. Your health system should:
- Be displayed as a bar or number on the UI
- Decrease their health value upon collision with an obstacle
- Stop the player only when their health value this 0
- Have a max health value
- Correctly reset to its max health value when the game is restarted 

### 3. Add a score. Your score should:
- Be displayed as a number on the UI
- Increment only when the player successfully goes through a hole in an obstacle
- Reset to 0 when the game is restarted

### 4. Add health packs. Your health packs should:
- Be a collidable object
- Be destroyed upon collision with the player
- Be destroyed shortly after if the player goes past them
- Increase the health value upon collision with the player, up to a max health value
- Appear in tunnels at a randomized rate, but never more than once per tunnel
- Have a semi randomized location in the tunnel that does not collide with other objects

### 5. Add player projectile attacks. Attacks should:
- Create a projectile on left mouse click that shoots forward down the tunnel faster than the player
- The projectile is destroyed upon collision with anything and after a short duration
- Have a short cooldown on shooting projectiles
- The projectile is created at the player/mouse position

### 6. Add enemies. Enemies should:
- Be a collidable object
- Be destroyed on collision with projectiles or the player
- Increase the score on destruction by a projectile
- Decrease the health value on collision with the player
- Be destroyed shortly after if the player goes past them
- The visual representation of the enemy is up to you...it can be simple.

### 7. Increase the player speed over time. The player speed increase should:
- Get faster over time, either directly based on time, or based on the player score
- Increase at a rate that is noticeable but does not ramp up the difficulty too fast

### 8. Add one creative modification that is unique to your game. Some ideas are:
- Health bar decreases along a gradient of colors
- Add screen shake on collision with barriers and enemies
- Color of the walls change depending on player health

## Advice

**Start working now...try to complete the tutorial in a couple of days and then work on adding a new mod every two days.** Do not be afraid to ask for help...on [CampusWire](https://campuswire.com/c/G18C1B62F/feed) or in [office hours](https://illinois-cs498gd.github.io/officehours.html). You can help out other students - answering questions on how to do things on CampusWire is very much encouraged. Learning how to implement a mechanic online or from someone on CampusWire is not plagiarism.

**Also, do not be afraid to change the initial game defaults in order to make the game more playable.** You can have the initial speed be slower, have the tunnels be longer or bigger...change things so that it is a game you think is a reasonably good experience. 

**Keep your code in a repo...and use .gitignore and LFS support to handle large files.** You can find a reasonably good [tutorial here](https://odederell3d.blog/2020/04/22/unreal-engine-4-github-first-steps/) . You can use the commercial [github.com]() or the [internal UIUC github](https://github-dev.cs.illinois.edu/).  
