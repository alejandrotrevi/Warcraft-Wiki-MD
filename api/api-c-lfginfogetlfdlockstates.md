# API C LFGInfo.GetLFDLockStates

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGInfo|system=LFGInfo}}
Needs summary.
 lockInfo = C_LFGInfo.GetLFDLockStates()

==Returns==
:;lockInfo:{{apitype|LFGLockInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| lfgID || {{apitype|number}} || 
|-
| reason || {{apitype|number}} || index. See [https://github.com/Ennie/wow-ui-source/blob/master/FrameXML/LFGFrame.lua LFG_INSTANCE_INVALID_CODES]
|-
| hideEntry || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_LFGInfo.GetLFDLockStates()</code>}}
* {{Patch 3.3.0|note=Added as <code>GetLFDChoiceLockedState()</code>}}
```