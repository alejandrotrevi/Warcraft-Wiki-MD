# API C ClubFinder.RespondToApplicant

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClubFinder|system=ClubFinderInfo}}
Needs summary.
 C_ClubFinder.RespondToApplicant(clubFinderGUID, playerGUID, shouldAccept, requestType, playerName, forceAccept [, reported])

==Arguments==
:;clubFinderGUID:{{apitype|string}}
:;playerGUID:{{apitype|string}}
:;shouldAccept:{{apitype|boolean}}
:;requestType:{{apitype|Enum.ClubFinderRequestType}}
{{:Enum.ClubFinderRequestType|nocaption=1}}
:;playerName:{{apitype|string}}
:;forceAccept:{{apitype|boolean}}
:;reported:{{apitype|boolean?}}

==Patch changes==
* {{Patch 8.3.0|note=Added <code>reported</code> argument.}}
* {{Patch 8.2.5|note=Added <code>playerName, forceAccept</code> arguments.}}
* {{Patch 8.2.0|note=Added.}}
```