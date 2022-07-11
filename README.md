# What is this repository about?
I wanted to kind of document + research + see how the Minimum Framerate Option in Halo Infinite affects overall performance.

## What is Minimum Framerate? (DRS)
DRS or Dynamic Resolution Scaling is a feature in Halo Infinite which makes the game dynamically adjust the render resolution to hit said minimum framerate.          
Its kind of a hit or miss, DRS can also induce stuttering due the resolution being adjusted constantly, if it is struggling to maintain the minimum framerate.

## Testing DRS

### Let me go over the testing bench here:
System:
> i7-10700K       
> GTX 1650       
> 24 GB @ 2667 MHz      
> 75 Hz Monitor.

Halo Infinite Settings:
> Everything set to Low + Options which can be turned off are turned off.         
> Render Resolution > 71%   
> Sharpening: 100%         
> Sensory Effects are disabled.
> Game was played at `1920x1080` and `1600x900` **Display Resolutions**. (Not Render Resolution.)

Map:
> Fragmentation       
> Player was set to stand Idle, with the crosshair looking directly at the structure.       
<p align='center'><img src='images/Untitled.png'></p>

## Benchmarks

### Fragementation > `Halo Infinite Vanilla Settings`

### FPS
<p align='center'><img src='images/fragementation.png'></p>

### Percentage
<p align='center'><img src='images/fragementation percent.png'></p>

### Observations
1. It seems using the Minimum Framerate boosted overall 0.2% Lows (Percentile).    

2. We can see `1600x900 Uncapped Min FPS > 75` offers overall better stability and a decent performance boost as compared to `1920x1080 Uncapped`.

3. `1920x1080 Uncapped Min FPS > 75` & `1600x900 Uncapped Min FPS > 75` offers similar performance but `1600x900 Uncapped Min FPS > 75` has better 0.2% Lows.


### Fragementation > `Halo Infinite Vanilla Settings + Minimum Framerate set to 960`

You can set the Minimum Framerate to 960 in Halo Infinite's config file.
```json
"spec_control_minimum_framerate": {
        "version": 2,
        "value": 960
    },
```

### FPS
<p align='center'><img src='images/fragementation 960.png'></p>

### Percentage
<p align='center'><img src='images/fragementation 960 percent.png'></p>

### Observations
1. DRS works more aggressively when the Minimum Framerate is set to 960.

2. `1600x900 Min FPS > 960` takes performance out of the ball park as compared to the other tests.

3. `1600x900 Uncapped Min FPS > 75`'s Avg. FPS is equal to the `1920x1080 Min FPS > 960`'s 0.2 Lows.

4. Overall playing the game at `1920x1080` with the minimum framerate set to 960 yields a 57% performance boost.             
   And playing at `1600x900` with the minimum framerate set to 960 yields 75% performance boost.


## Downsides with having Minimum Framerate at 960.
With having your minimum framerate at 960, Dynamic Resolution Scaling aka DRS tends to work more aggressively, but there are downsides to this.

1. You might experience the game somewhat stuttering but that isn't case, its the game simply bumping/decreasing the render resolution at more aggressive rate instead of gently.

2. Mouse movement might appear stuttery/jittery but this is only visual and only occurs if your minimum framerate is set to `960` or when DRS (Dynamic Resolution Scaling) acts very aggressively.

    > Currently figuring out ways to either minimize or eliminate this issue.