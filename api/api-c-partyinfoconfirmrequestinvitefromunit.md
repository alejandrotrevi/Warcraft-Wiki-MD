# API C PartyInfo.ConfirmRequestInviteFromUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Immediately request an invite into the target party, this is the confirmation function to call after RequestInviteFromUnit, or if you would like to skip the confirmation process.
 C_PartyInfo.ConfirmRequestInviteFromUnit(targetName [, tank [, healer [, dps]]])

==Arguments==
:;targetName:{{apitype|string}}
:;tank:{{apitype|boolean?}}
:;healer:{{apitype|boolean?}}
:;dps:{{apitype|boolean?}}

==Patch changes==
* {{Patch 8.2.5|note=Added.}}
```