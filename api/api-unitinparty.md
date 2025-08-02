# API UnitInParty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the unit is a member of your party.
 inParty = UnitInParty(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;inParty:{{apitype|boolean}} - if the unit is in your party

==Example==
 if UnitInParty("target") then
     print("Your target is in your party.")
 else
     print("Your target is not in your party.")
 end

==Details==
: Pets are not considered to be part of your party (but see {{api|UnitPlayerOrPetInParty}}).
: Battleground raid/party members are also not considered to be part of your party. 
: UnitInParty("player") returns nil when you are not in a party.
: <strike>As of 2.0.3, UnitInParty("player") always returns 1, even when you are not in a party.</strike>
: <strike>UnitInParty("player") should return nil. (since patch 1.11.2, always returned 1 before)</strike>
: Use {{api|GetNumPartyMembers}} and {{api|GetNumRaidMembers}} to determine if you are in a party or raid.

==See also==
* {{api|UnitInRaid}}
```