# Spider Robot Project
A prototype spider robot with leg stabilization mechanisms. Work in progress documenting design iterations, errors, and solutions.

**Video demos:**

https://youtube.com/shorts/J5rAIZbxhh4?feature=share

https://youtube.com/shorts/_QNONGRYIa8?feature=share


## Current Status

It doesn't walk. The front right leg has a problem - one of its servos stretches straight when powered on. The robot can't stand because of this.

## What Works

- 11 out of 12 servos respond correctly
- The leg movement sequences work in theory
- Power distribution handles 12 servos (took time to figure this out)

## What Doesn't Work

- Front right leg - one servo won't stay bent. Goes straight as soon as I turn it on.

## What I Tried

- Swapped the servo with a working one → same problem
- Checked wiring multiple times → looks fine
- Tested different code values → nothing changed
- Asked my teacher → he wasn't sure

## What I Learned

- How to control 12 servos at once
- Power management for multiple components (to make sure the servo motors didn't exceed 7V, a LM2596 DC-DC Step-Down power module was required as the two lithium batteries produced excess voltage)
- Debugging takes longer than building
- It's okay to not have it working yet

## Files Here

- /code - my Arduino code
- logbook.md - everything I tried and failed
- /media - photos and video
