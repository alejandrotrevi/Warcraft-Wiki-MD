# API GetFlyoutInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Describes an action bar flyout.
 name, description, numSlots, isKnown = GetFlyoutInfo(flyoutID)

==Arguments==
:;flyoutID:{{apitype|number}}

==Returns==
:;name:{{apitype|string}} - Title line in the tooltip.
:;description:{{apitype|string}} - Second line in the tooltip.
:;numSlots:{{apitype|number}} - Maximum number of slots contained in the flyout, accessed with {{api|GetFlyoutSlotInfo}}().
:;isKnown:{{apitype|boolean}}
```