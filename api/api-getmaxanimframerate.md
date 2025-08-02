# API GetMaxAnimFramerate

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the maximum animation frame rate for throttled animations.
 maxFPS = GetMaxAnimFramerate()

==Returns==
:;maxFPS:{{apitype|number}} - Maximum frame rate for throttled animations in frames per second.

==Details==
* Animations obey this global animation frame rate limit by default -- even if the client's FPS is significantly higher, animations will only update at the frame rate returned by this function. Animation groups may opt out of this throttling using 
 AnimationGroup:SetIgnoreFramerateThrottle(true)

==Patch changes==
* {{Patch 4.1.0|note=Added.}}

==See also==
* {{api|SetMaxAnimFramerate}}
* {{api|t=w|AnimationGroup:SetIgnoreFramerateThrottle}}
```