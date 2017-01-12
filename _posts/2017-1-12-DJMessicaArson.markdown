---
layout: post
title: "DJ Messica Arson"
date: 2017-1-12
categories:
description:
image: https://s28.postimg.org/lw0z7o79p/Screen_Shot_2017_01_12_at_3_39_57_PM.png
image-sm: https://s28.postimg.org/lw0z7o79p/Screen_Shot_2017_01_12_at_3_39_57_PM.png
---
During the break for the holidays, I was looking for a fun music related project to work on for the next Hack&&Tell. I have also always wanted to learn ruby and but haven't done too much with it. I stumbled upon [Sonic Pi](http://sonic-pi.net/) and I thought it would be fun to live code a DJ set for my 5 minute Hack&&Tell "talk".

With the built in help guide and [this guide](https://www.raspberrypi.org/magpi-issues/Essentials_Sonic_Pi-v1.pdf) I found myself writing code that sounded cool after play around for just a few minutes. The first live loop I wrote was as follows:

```ruby
live_loop :add_in do

  if one_in(3)
    sample :drum_heavy_kick
  else
    sample :drum_cymbal_closed
  end

  sleep 0.5

end
```
After that I was able to add more loops and buffers to create a start for tonight's set. A fun synth sound I wrote was as follows:

```ruby
live_loop :create do
  synth :dark_ambience
  n = (ring :g1, :g2, :g3).tick
  play n, attack: 6, env_curve: 7
  sleep 4
end
```

The full code for tonight's set can be found [here on my github](https://github.com/JessicaGarson/JessicaGarson.github.io).
