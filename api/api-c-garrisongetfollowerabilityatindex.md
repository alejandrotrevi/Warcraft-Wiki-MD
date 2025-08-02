# API C Garrison.GetFollowerAbilityAtIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns an ability for the follower.
 abilityID = C_Garrison.GetFollowerAbilityAtIndex(followerID, index)

==Arguments==
:;followerID:{{apitype|string}} : [[GUID#Follower|FollowerGUID]]
:;index:{{apitype|number}} - Usually between 1 and 4

==Returns==
:;abilityID:{{apitype|number}}

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_Garrison.GetFollowerAbilities}}
```