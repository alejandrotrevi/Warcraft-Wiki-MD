# API C Club.GetTickets

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 tickets = C_Club.GetTickets(clubId)

==Arguments==
:;clubId:{{apitype|string}}

==Returns==
:;tickets:structure - ClubTicketInfo[]

{{:Struct_Club.ClubTicketInfo}}

==Details==
* Get the existing tickets for this club. Call RequestTickets() to retrieve tickets from server.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```