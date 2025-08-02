# API issecure

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the current execution path is secure.
 secure = issecure()

==Returns==
:;secure:{{apitype|boolean}} - true if the current path is secure (and able to call protected functions), false otherwise.

==Details==
* This function will return <code>false</code> if called from any (insecure) addon code.
* Certain API functions (and FrameXML functions that check this function's return value) cannot be called from tainted execution paths.

{{API Trail Secure}}
```