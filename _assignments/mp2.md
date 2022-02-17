---
layout: assignment
title: "Level Design"
index: 10
due: "Mar. 2, 2022 @ 11:59 PM"
material: ~
points: 50
rubric:
-
    name: Health System
    points: 5
    description: Display and track a player health metric
-
    name: New Mechanic
    points: 5
    description: Add a new mechanic to the player character
-
    name: Implement Enemies
    points: 10
    description: Implement all enemies as described in the MP spec
-
    name: Create New Enemy Type
    points: 5
    description: Design and implement another enemy type of your design
-
    name: Level Layout
    points: 5
    description: Create a level layout that can be traversed in 5 minutes and has a level complete screen
-
    name: Enemies
    points: 5
    description: Strategically place all enemy types throughout the level
-
    name: Collectibles
    points: 5
    description: Place collectible objects around the level and display them on the UI
-
    name: Design Document
    points: 10
    description: Submit a document that explains your level design and design decisions
---

# MP 2: Level Design
Your second MP is all about level design and all the important factors that go in to it. In this MP we will touch on player abilities, level layouts, and enemy AI.

To start you off we will need you to get familiar with the basics of how the level editor works in Unreal. We would recommend you complete the tutorial found here in order to do so: https://docs.unrealengine.com/4.27/en-US/BuildingWorlds/LDQuickStart/

Once you have done that you can continue on to the main assignment.


Your objective with this assignment is to design and create your own 3D platformer level. You will be provided with a player character and you are going to place assets, add mechanics, and create enemies for that character to interact with.

The basic player controller along with a large number of assets you may want to use are found here: 
https://www.unrealengine.com/marketplace/en-US/product/unreal-learning-kit-games (it will say it only is updated for 4.26, just open it with 4.27 and it will work fine)

The character controller you will be using is under BP_HourOfCode_Character.

## Part 1: Update Your Character
The first thing you need to do is update your character. You need to do this in two ways.

1. Add a health system.
    This should be very similar to the system used in the first MP. It should have a bar displayed somewhere on the screen, and a game over screen should be displayed if it reaches 0. You should also make an item that can be placed in the world and picked up to restore health. This item should be destroyed on collection. There are several given assets that could work well for this but you can use whatever you want.

2. Add a new mechanic to the player character.
    This can be basically anything you want. An ability to attack, a grapple hook, a roll. It should be similar in complexity to the flight mechanic the character controller already has.

## Part 2: Make Some Enemies
We need obstacles to fill our level. So lets make some enemies. You will be making 4 distinctly different enemy types.
All enemy types should:
-	Be destroyed when the players collides with their “head” (the top of whatever model you decide to use)
-	Reduce the players health on collision with any part that is not the head
-	Knock the player back and remove player control for a short duration after a health reducing collision
The enemy types you will create are:
1.	The Pursuer. The Pursuer should:
-	Have a looping patrol path that it follows
-	Run at the player when they get within a moderate distance of each other, and they have line of sight with each other
-	Within reason, return to its patrol path if the player gets too far away (this should be done by the enemy moving, not teleportation)
2.	The Flyer. The Flyer should:
-	Fly at a specific height above the player
-	Move to a new location ever few seconds, trying to keep some distance between itself and the player (the exact form of this is up to you)
-	Launch projectiles that lead the players movements
-	The projectiles should reduce the players health on collision
3.	The Mortar. The Mortar should:
-	Be an unmoving enemy placed on the ground
-	Randomly launch projectiles above and around it in an arc
-	The projectiles should cause a small explosion on collision with other objects
-	The explosions should knock back and reduce the players health on collision
4.	An enemy of your own design. It should have similar complexity to the other three and also be distinct and take on a different role.

## Part 3: Putting It All Together 
The last step of the MP is to put it all together and make a platforming level.

Your level should:
- Be completable in around 5 minutes
- Present some degree of challenge
- Return the player to their start location when their health is reduced to zero or if they fall off the map
- Display a level complete screen upon reaching the end of the level
- Utilize all the created enemies in a way that contributes to the design
- Have health pick ups scattered around the level
- Have floating collectibles scattered around the level to guide the player and encourage them to explore
- You can use any asset you want for these, and there are several included in the given assets
- These objects should be destroyed on collection, and the number collected should be displayed some where on the UI
- The design of the level should specifically take into account the flight mechanic, the mechanic you created, and your enemy design

As far as environmental and visual assets, you can use any of the provided, built in, or any other assets in your level creation.

# Submission Instructions
Hand-in will be done on Canvas. You will be expected to upload the following:

1. A link to a git repo or drive/box folder containing your project code. It should be possible to build your game in Unreal using the submitted code.

2. A short video up to 10 minutes long (can be much shorter) showing your level and demonstrating all the required features. Your video ideally should be a screen capture with brief narration by you pointing out the features as they appear in the game.

3. A short written document, either pdf or docx format, explaining your process of designing you level. It should be at most a page long. It should explain how you went about the design process and how your design had to accommodate the new mechanic and enemy you created. 