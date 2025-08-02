# API SaveBindings

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Saves account or character specific key bindings.
 SaveBindings(which)

==Arguments==
:;which:{{apitype|number}} - Whether the key bindings should be saved as account or character specific.<sup>[https://github.com/Gethe/wow-ui-source/blob/9.1.5/Interface/AddOns/Blizzard_BindingUI/Blizzard_BindingUI.lua#L5]</sup>
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Constant !! Description
|-
| 0 || DEFAULT_BINDINGS || 
|-
| 1 || ACCOUNT_BINDINGS || 
|-
| 2 || CHARACTER_BINDINGS || 
|}

==Details==
* Bindings are stored in WTF\Account\ACCOUNTNAME\bindings-cache.wtf.
* Triggers {{api|t=e|UPDATE_BINDINGS}}

==Patch changes==
====<font color="#4ec9b0">Classic</font>====
* {{Patch 2.5.1|note=Changed to <code>SaveBindings()</code>}}
* {{Patch 1.13.2|note=Added as <code>AttemptToSaveBindings()</code>}}

==See also==
* {{api|GetCurrentBindingSet}}
```