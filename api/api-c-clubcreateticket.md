# API C Club.CreateTicket

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
This is protected and only available to the Blizzard UI. Used for creating a ticket for a community club.
 C_Club.CreateTicket(clubId [, allowedRedeemCount, duration, defaultStreamId, isCrossFaction])

==Arguments==
:;clubId:{{apitype|string}}
:;allowedRedeemCount:{{apitype|number?}} - Number of uses. nil means unlimited
:;duration:{{apitype|number?}} - Duration in seconds. nil never expires
:;defaultStreamId:{{apitype|string?}}
:;isCrossFaction:{{apitype|boolean?}}

==Details==
* Check canCreateTicket privilege.

==Patch changes==
* {{Patch 9.2.5|note=Added <code>isCrossFaction</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```