# Pygame Platformer (2019)

## Animation

This is the animated branch. 

### Hero Animation

The hero has three additional attributes.

- `facing_right` is a boolean which is `True` when the hero is facing right and `False` otherwise. When the hero is first initialized, `facing_right` is set to `True`. Using the arrows to move right or left set this variable while playing.
- `steps` is a variable that tracks how many iterations of the game loop have elapsed while the hero is walking.
- `step_rate` is the number of frames that elapse before toggling between the walk1 and walk2 images.

Two functions have been added to the hero.

`step` is called whenever the player is pressing either the right or left arrow key. This function increments the `steps` variable by one. Each time the `steps` variable reaches double the step rate, it resets to zero.

In  the heros `update` function calls a new function set_image. `set_image` looks at the current direction and state of the hero (hurt, jumping/falling, idle, or walking) to set the appropriate image.

### Enemy Animation
