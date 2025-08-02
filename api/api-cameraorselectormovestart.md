# API CameraOrSelectOrMoveStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Begin "Left click" in the 3D world.
 CameraOrSelectOrMoveStart()

==Details==
* This function is called when left-clicking in the 3-D world. It is most useful for selecting a target for a pending spell cast.
* Calling this function clears the "mouseover" unit.
* When used alone, puts you into a "mouselook" mode until [[API CameraOrSelectOrMoveStop|CameraOrSelectOrMoveStop]] is called.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
* {{Patch 1.10.0|note=Requires a hardware event.}}
```