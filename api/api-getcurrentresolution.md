# API GetCurrentResolution

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}__NOTOC__
Returns the index of the current screen resolution.
 index = GetCurrentResolution()

===Takes===
: Nothing

===Returns===
: Number index
:: This value will be the index of one of the values yielded by [[API_GetScreenResolutions|GetScreenResolutions()]]

===Example===
 message('The current screen resolution is ' .. ({GetScreenResolutions()})[GetCurrentResolution()])
Output:
 The current screen resolution is 1024x768
```