---
layout: post
title: Movement
---

I'll upload footage in a future post, but for now I am thinking about movement in the game!

For now movement is locked onto a grid, very much like Furcadia. For the first prototype I think this will be good for saving time on development.

For continuous movement, I may think about that if I ever implement client side prediction.

Many caveats of client side prediction is being able to abstract that to any worldcrafters.

At first, movement was limited to tapping. I added the ability for players to be able to hold the key they need to move. This caused an issue. The animation to move in addition to network latency psychologically caused the user to hold for way too long. When tapping to move, the user might accidentally move twice.

To combat this, I've made the initial press of a movement button have a slight delay. You can see this while moving, that there's a bit of a ramp-up where you stop and then you continue to move.

It's ever so slight but does a great job at allowing tap movement to work again.

I also added a client-side limiter to movement. This means when you move there is X amount of time before you can move again. It's jarring to have some of your keys ignored. I think I will build a input queue system to make this more manageable.
