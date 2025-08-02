# API C PartyInfo.RequestInviteFromUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Attempt to request an invite into the target party, requires confirmation in some cases (e.g. there is a party sync in progress).
 C_PartyInfo.RequestInviteFromUnit(targetName [, tank [, healer [, dps]]])

==Arguments==
:;targetName:{{apitype|string}}
:;tank:{{apitype|boolean?}}
:;healer:{{apitype|boolean?}}
:;dps:{{apitype|boolean?}}

==Patch changes==
* {{Patch 8.2.5|note=Moved to {{api|C_PartyInfo.RequestInviteFromUnit}}(). The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.2.5/Blizzard_Deprecated/Deprecated_8_2_5.lua#370]}}
* {{Patch 7.1.0|note=Added as {{api|RequestInviteFromUnit}}()}}
```