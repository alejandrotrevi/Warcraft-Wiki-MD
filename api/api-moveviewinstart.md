# API MoveViewInStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Begins zooming the camera in.
  MoveViewInStart(speed)

==Arguments==
:;speed:{{apitype|number}} - Speed at which to begin zooming.

==Returns==
:Nothing

==Example==
  MoveViewInStart(5/tonumber(GetCVar("cameraZoomSpeed"))) -- zoom the camera in at 5 increments/second

==Details==
:*Speed is a multiplier on the CVar 'cameraZoomSpeed', which is in increments/second. A zoom increment appears to be about a yard from the character.
:*If speed is omitted, it is assumed to be 1.0.
:*Negative numbers go the opposite way, a speed of 0.0 will stop it.
:*This is not canceled by moving your character, but is canceled by using the mousewheel to zoom.
:*Applying a negative speed is not the same as using the other function to go the opposite way, both vectors are applied simultaneously. If you zoom both ways equally, it will appear to stop, but the rotations are still being applied, though canceling each other.
```