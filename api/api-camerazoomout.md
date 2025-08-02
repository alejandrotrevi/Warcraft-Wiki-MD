# API CameraZoomOut

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Zooms the camera out.
 CameraZoomOut([increment])

==Arguments==
:;increment:{{apitype|number|default=1}}

==Details==
* Zooms the camera out of the viewplane by ''increment''.  The increment must be between 0.0 and the ''max camera distance''. 
* As of patch 1.9.0 if the 'Interface Options > Advanced Options > Max Camera Distance' setting is set to Low, then the largest value for increment is 15. If this setting is set to High, then the largest value for increment is 30.  You can test for the ''max camera distance'' by zooming in to first person and counting the number of times you can call this function with ''increment'' set to 1.0 and still zoom out.
```