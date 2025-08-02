# API C ActionBar.EnableActionRangeCheck

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ActionBar|system=ActionBar}}
Used in conjunction with {{api|t=e|ACTION_RANGE_CHECK_UPDATE}} to inform the UI when an action goes in or out of range with its current target.
 C_ActionBar.EnableActionRangeCheck(actionID, enable)

==Arguments==
:;actionID:{{apitype|number}}
:;enable:{{apitype|boolean}} - True if changes in range for the action should dispatch ActionRangeCheckUpdate. False if the action no longer needs the event.
```