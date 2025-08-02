# API SetScreenResolution

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the current resolution in effect
 SetScreenResolution([index])

===Arguments===
:;index:{{apitype|number?}} - This value specifies the new screen resolution, it must be the index of one of the values yielded by [[API_GetScreenResolutions|GetScreenResolutions()]]. Passing nil will default this argument to 1, the lowest resolution available

===Example===
This sets the screen to 1024x768, if available:
 local resolutions = {GetScreenResolutions()}
 for i,entry in resolutions do
   if entry == '1024x768' then
     SetScreenResolution(i)
     break
   end
 end
```