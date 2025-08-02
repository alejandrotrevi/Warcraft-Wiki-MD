# API GetCameraZoom

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current zoom level of the camera.
 zoom = GetCameraZoom()

==Returns==
:;zoom:{{apitype|number}} - the currently set zoom level

==Details==
: Doesn't take camera collisions with the environment into account and will return what the camera ''would'' be at. If the camera is in motion, the zoom level that is set that frame is used, not the zoom level that the camera is traveling to.
```