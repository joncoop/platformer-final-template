# Pygame Platformer (2019)

## About

Use the code from this repository as a template to create your own platformer. Each idea you implement is worth points based on difficulty. See the 'Grading' section below for details. If you have ideas that I haven't thought of, tell me and I'll add them to this list.

## Ideas for student projects

### Very Easy

- Name your game.
- Change the dimensions of the game window.
- Find your own custom artwork for tiles.
- Find your own custom artwork for the hero.
- Find your own custom artwork for enemies.
- Find a background images for a level. Be sure the background images are scaled to fit the game window and that they tile without showing seams. Adjust the parallax settings as you see fit.
- Find different background images for each level you make.
- Find your own theme music for a level.
- Use different theme music for each level you make.
- Include tiles in the foreground layer of a level. The hero should run behind these images and not interact with them.
- Keep your assets folder organized. Use subfolders to store different types of assets. Remove unused asset sets from your repository.
- In your assets folder, update the sources.txt file to keep track of where each set of assets is from.
- Play music during the start screen. The music should be different than that used for any of the levels.
- Play music when the player wins the game. The music should be different than that used for any of the levels.

### Easy

- Design a complex standard level. Your level should be at least 40 blocks long. Your level should be significaltly different from the template to receive credit.
- Create a level which takes place on a different planet. You can modify the gravity and terminal velocity in the level data to create the physics you want. (A gravity of less than 1 will make the world 'bouncier'.) Use a space-themed tiles and background images for your level.
- Create your own custom artwork for one unanimated entity in the game. http://www.piskelapp.com/ is a good site for this.
- Create your own custom artwork for at least three unanimated entities in the game.
- Add sound effects to each of the following events: jumping, getting items, colliding with an enemy, completing a level, and when the game ends in a loss.
- Create an interesting start screen that does more than just show the name of the game. 
- Create an interesting loss and win screens that do more than just state the outcome of the game. 
- Add an item other than a coin and give it a point value.
- Give the hero a maximum number of hearts. Then display hearts/max rather than just hearts. (Displaying heart icons is in the 'Medium' section.)
- Create an item which gives the hero a heart. When the hero gets this item, hearts should not increase beyond the maximum number the hero can have.
- Create an item which increases the max hearts a hero can have. 
- Give points for getting the flag at the end of the level. Do so in a way that landing higher on the flagpole earns more points. One way to do this could be to check the y-coordinate of the hero when the flag is reached and devise a formula to award points.
- If your character has lives in addtion to hearts (see the 'Hard' section), display lives in the format [character icon] x [number of lives].
- If you made an invincibility powerup (in the 'Medium' section), make the player kill enemies collided with while invincibleBe sure that the temporary invincibility acquired after colliding with an enemy does not result in killing enemies.
- Animate your hero sprite. The hero should have separate images for idle, jumping, and at least two walking images. Each image should be mirrored so that the hero is always facing the direction that it is moving.
- If you animated your hero, add an additional image to your hero to indicate when it is hurt. This should only show during the brief invincibility period while hurt. Be sure it does not display for invincibility earned through a powerup. 
- Add a 'happy' image to your hero animation that is displayed when your hero completes a level.

### Medium

- Create a game with at least 4 levels total. Levels should be significantly different in layout and each should be at least 40 block long.
- Create your own custom artwork for one animated entity in the game. Entities that only flip when they change directions are not considered animated. Animation should include multiple frames such as when the hero runs. http://www.piskelapp.com/ is a good site for this.
- Create your own custom artwork for at least three animated entities in the game.
- Use tiles in the midground layer to create complex artwork. For example, the end of the level could have a castle that the hero can run in front of. (Perhaps the location of the door on the castle could correspond to the goal zone.)
- Display actual hearts to show health. Show empty hearts up to the max hearts limit when the hero's hearts are not at the maximum level.
- Create invincibility (star) power-up that gives the hero a timed period of invincibility. If you are using an image to indicate when the hero is invincible due to being hurt, be sure that that image is not shown in this situation. This means you will need to create a different timer to track invincibility time from a power up.
- Invent your own power-up which lasts a limited amount of time or until the player hits an enemy or completes a level.
- Increase the max hearts a player can have when some milestone is achieved, perhaps completing a certain number of levels or achieving a certain score.
- Invent an item which has a negative consequence on a player other than reducing hearts, lives, or points.
- Put gaps in the blocks that run along the bottom of the level. Then modify the check_world_edges function so that the hero's hearts get set to zero if the player goes past the bottom edge of the world. You'll need to make sure enemies that fall through these gaps are also removed from the game. Pygame's sprite.kill() function will be useful for this.
- Add a PAUSE stage to the game which is activated when the player presses 'p' (or a button on the joystick). All movement and time should stop during a pause stage. Pressing 'p' again should resume. Be sure to show a message indicating the game is paused. Theme music should also pause. (Pygame has pause and unpause functions for music. Consider adding music helper functions along with play and stop to accomplish this.)
- Use a modifier key/button that makes you run faster (or perhaps jump higher) while the key/button is held. The hero's move_left and move_right functions will need to take an additional argument (probably True or False) to see if a modifier key is being held.
- Create a custom enemy with unique behavior regarding movement.
- Require the hero to perform a task in order to complete the level. For example, maybe the hero needs to collect a key in order to open a door in the level goal area.
- Utilize vertical scrolling in a level. You'll need to modify the calculate_offset function to get vertical scrolling to work.
- Show time on the stats layer. Give a time bonus for completing a level. Have the hero die if the level is not completed in a set amount of time.
 - Have the hero track coins separately from the score. (They can still be worth points.) Either increase the max hearts or give an extra life when a number of coins is earned. Reset the coin count after the award is given.

### Hard

- Give your hero a lives attribute, perhaps set to 3 when the game starts. When the hero loses all hearts, subtract a life from the hero and have the level restart. The game should end when all lives are used.
- Change the game so that it uses the XBox controller instead of the keyboard. Be sure to map all game functions such as start and pause to the controller and not just player control. (https://github.com/joncoop/pygame-xbox360controller)
- Create an underwater level. You can use low gravity and low terminal velocity to slow down the up and down motion. You should use the jump key to swim up and then let the player slowly drift down. The tricky part is getting the jump to work whether or not you are standing on a block. Be sure that jumping still functions normally in land levels.
- Create a game with at least 8 levels total. Levels should be significantly different in layout and each should be at least 36 block long.
- Kill enemies when you land on them. You'll need to check which direction you hit the enemy from in process enemies. When you do kill an enemy, make the hero bounce up a bit rather than just fall through the enemy. Also, be sure that the hero doesn't become invincible for a brief period after a kill as he does when normally colliding with an enemy. Award points for killing an enemy.
- If you kill enemies, create enemies that take more than one hit to kill. You should either bounce high enough off of the enemy to force a delay between first and second hits or give an enemy a brief invincibility period after a hit.
- Make the game save high scores to a text file in a data folder. The high score should be displayed on the splash screen and on the end screen. Be sure that the end screen makes the player aware if they achieve a new high score.
- Animate a scenery element such  flickering torches. This is probably best accomplished by creating an AnimatedTile class. Animated tiles should have an update function which cycles through images. When the level is loaded, AnimatedTiles should be added to their own sprite group which can be udated each iteration of the game loop and then drawn to the 'active' layer.
- Create a Warp item in the game that transports the player instantly to another part of the level. Warps should be declared in the level.json file and indicate both the location of the warp item and the location that the player will warp to. (A four-element list would work well for this.) Make the warp either a necessary part of solving a level or a way for a player to get otherwise unreachable prizes. Don't try to make two-way warps. One-way will be much easier.

### Very hard

- Add ladders to the game. If a player is on a ladder, don't apply gravity. Assign vy by player input instead. Also disable jumping while on a ladder. You should use animated climbing images too.
- Put switches in the game that open and/or close areas of a level.

### Super hard

- Create a Chest item with a boolean attribute locked set to True when it is initialized. Then create a Key object that a player can acquire. If the player intersects a locked chest with a key, then locked should be set to False and the image should be updated. The chest should also have an item attribute. Once the chest is opened, the item can be added to the level.items sprite group. The location of the item that the player can acquire should be in the grid location directly above the chest.
- Give your player a gun. Let your player kill enemies by shooting them. You'll need to create Bullet objects which spawn at the hero's gun and travel in the direction the hero is facing. Bullets shouldn't travel indefinitely. Limit the number of ticks a bullet will exist before it calls the kill() function on itself. Enemies can be given a process_bullets function. (You might need to make the shooter/hero a bullet parameter so that when the bullet hits an enemy, points can be awarded.)
- Make a sign you can read or a character that 'speaks'. Display a message when the hero intersects the sign or speaking character while holding the up arrow (or up on the d-pad). Add a show_message helper function to the Game class which takes arguments containing the message. The message should be displayed nicely, perhaps in a box that looks like a sign or in a box that looks like a speech bubble.
- Make a special level at the end of the game with a boss that needs to be defeated. The boss should take multiple hits to kill, have a unique behavior compared to other enemies, and do something to try to kill the hero. (Shoot stuff, breathe fire, ...?)

## Grading

Points will be awarded for each feature as follows:

- Very Easy: 2 points each
- Easy: 4 points each
- Medium: 8 points each
- Hard: 12 points each
- Very hard: 16 points each
- Super hard: 20 points each

This project will count as a major assessments. When you reach 100 points, you can show me your work to get credit for the first assessment. You may optionally work with a partner. If you choose to work with a partner, then multiply your total points by 2/3 to determine your grade.

## Final Exam

The platformer project will also be used as the basis of your final exam. Below is a list of things that may be expected. Don't consider this list final yet. I just want you to have some idea of what to expect now.

- Use GitHub Pages or Google Sites to create a website for your game. 
- Create cover art for your game. Save it as a PNG file. Print it in color so that I can post it in the room.
- Create an executable file from your project. The executable should be downloadable from your website.
