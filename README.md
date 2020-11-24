
# Complexity in Video Games

> Trying to define the complexity of games for *developement* insight.

Here's a rough draft of my complexity scale. Subject to change.
Let me know if you disagree with my placements,
or think there should be another level.

For a game jam I would love to try to aim heavily toward level 1 or level 2.

---

## Table of Contents

- [Complexity in Video Games](#complexity-in-video-games)
  - [Table of Contents](#table-of-contents)
  - [Level 1](#level-1)
    - [Snake](#snake)
    - [Brick Breaker](#brick-breaker)
    - [Cubefield](#cubefield)
    - [Minigolf](#minigolf)
    - [Frogger](#frogger)
    - [Pacman](#pacman)
    - [Myst / Riven (click to go, turn or interact)](#myst--riven-click-to-go-turn-or-interact)
    - [Any one button runner](#any-one-button-runner)
  - [Level 2](#level-2)
  - [Level 3](#level-3)
  - [Level 4](#level-4)
  - [Level 6](#level-6)
  - [Level 7](#level-7)
  - [Level 8](#level-8)

---

## Level 1

> Single dimensional games,
> generally a single facet of control.
> A game in this category uses a single input at a time.

---

### Snake

**Definitions**

- Two Axis. (Snake can move on two axis.)
- Tile based.
- "Single Screen" (The view does not change.)
- Movement is by tile, per tick, limits are clamped by screen.
- Snake piece is left on tile for some number of ticks,
  depending on "length" of snake.
- Each tick the snake moves one tile in set direction.
- Collecting "token" increases length of snake.
- Every length of snake increases the amount of time a snake piece remains on a unit.

**Implementations**

- **Active**: None
- **Action**: <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>
- **Control**: Change direction of "1D unit direction" on **action** press.
- **Player Constraints**: Do not hit self. (Self is at any given spot temporarily.)

---

### Brick Breaker

**Definitions**

- Two axis. (Ball is on two axis, player is on one axis.)
- "Single Screen" (The view does not change.)
- Movement is dynamic, limits are clamped by screen.
  - The ball moves fluidly around the screen and bounces against limits and objects.
  - The paddle moves fluidly back and forth across the bottom of the screen.
- When ball intercepts brick, it is "downgraded" or destroyed, ball vector mirrors.
- (Extra) Powerups may fall down to be intercepted by paddle,
  they generally increase the speed of the ball, the power of the ball,
  or the number of balls.

**Implementations**

- **Active**: <kbd>←</kbd><kbd>→</kbd>
- **Action**: <kbd>Space</kbd> (Optional)
- **Control**: Hold **active** to move paddle 1D to edge of screen.
- **Player Constraints**: Do not miss ball. (Ball is moving.)

---

### Cubefield

> A partially obstructed "forever" runner on 1 axis.
> "Moving Screen" game.
> Movement is uncontrolled, direction is floating.
> Obstacles are static.

- **Active**: <kbd>←</kbd><kbd>→</kbd>
- **Action**: None
- **Control**: Hold **active** to change 1D forward vector.
- **Player Constraints**: Do not hit objects. (Player is moving.)

### Minigolf

> A partially obstructed "ball with velocity" course on 2 axis.
> Movement is floating and may occur on both axis at the same time.
> Surfaces may have different effects on the ball.

- **Active**: None
- **Action**: <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd> or Joystick,
  <kbd>Space</kbd> or "Button"
- **Control**: Adjust future 2D vector with **action** buttons.
  Trigger with special **action** button.
- **Player Constraints**: None

### Frogger

> An obsticle course on 2 axis.
> Movement is by unit, may only occur on one axis at a time.
> Obsticles move on a single axis.
> Water mechanics are the same, just flipped.

- **Active**: None
- **Action**: <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>
- **Control**: Trigger 1D direction with **action** buttons.
- **Player Constraints**: Do not hit objects. (Objects are moving.)

### Pacman

> A cat and mouse game restricted to hallways on 2 axis.
> Movement may only occur on one axis at a time.
> Mouse role may be swapped temporarily with special mechanics.
> Avoid cat role while collecting pellets,
> chase cats when able.

- **Active**: None
- **Action**: <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>
- **Control**: Change direction of "1D velocity" on **action** press.
- **Player Constraints**: Do not hit objects. (Objects are moving.)

---

### Myst / Riven (click to go, turn or interact)

**Definitions**

- Sequence of images with interactable components.
- Sometimes animated images or movies.
- Point and click mechanics.

**Implementations**

- **Active**: Mouse Move
- **Action**: Mouse Click
- **Control**: Click defined areas of screen, defined per image.
- **Player Constraints**: None

---

### Any one button runner

**Definitions**

- Scrolling 1D Screen
- Player can jump or "increase height" on an **action**.

**Implementations**

- **Active**: Hold a button to raise height.
- **Action**: Click a button to raise height.
- **Control**: Raise or lower player height.
- **Player Constraints:** Do not hit objects or fall off field.

---

## Level 2

- Flash Flash Revolution, Dance Dance Revolution (shoot, high precision sync)
- Donkey Kong (horizontal, jumping, dodging, climbing)
- Galaga / Gradeus (shoot, move)
- Tetris (orient, position, speed up)
- Asteroids (spin, velocity, shoot)
- Space Invaders (horizontal move, shoot)
- SkiFree (move, trick, dodge)
- Day of the Tentacle, The Secret of Monkey Island (click to proceed, many options for clicking)

## Level 3

- Commander Keen
- [Best Friends](https://www.youtube.com/watch?v=Rn6CyvXMRjY)

## Level 4

- Banjo Kazooie
- Donkey Kong 64
- Mirrors Edge

## Level 6

- Fallout
- Skyrim
- Dota, League
- Warcraft 3
- Starcraft
- Ragnarok Online, FlyFF, Maplestory

## Level 7

- Boneworks
- Half-life Alyx

## Level 8

> Level 6 + Networking / Multiplayer

- Halo
- Call of Duty
- World of Warcraft
