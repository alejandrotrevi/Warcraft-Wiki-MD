# API C Transmog.ApplyAllPending

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Confirms all pending transmogs.
 success = C_Transmog.ApplyAllPending(currentSpecOnly)

==Arguments==
:;currentSpecOnly:{{apitype|boolean}}

==Returns==
:;success:{{apitype|boolean}}

==Triggers events==
* {{api|t=e|TRANSMOGRIFY_SUCCESS}}
* {{api|t=e|TRANSMOGRIFY_UPDATE}}

==Patch changes==
* {{Patch 7.0.3|note=Moved from {{api|ApplyTransmogrifications}} to {{api|C_Transmog.ApplyAllPending}}.}}
```