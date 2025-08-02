# API GetBillingTimeRested

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of "healthy" time left for players on Chinese realms.
 secondsRemaining = GetBillingTimeRested()

==Returns==
:;secondsRemaining:{{apitype|number}} - Amount of time left in seconds to play as rested. See details below for clarification. Returns <code>nil</code> for EU and US accounts.

==Example==
The official function (modified to output in the chat frame) when you have partial play time left:
 print(string.format(PLAYTIME_TIRED, REQUIRED_REST_HOURS - math.floor(GetBillingTimeRested()/60)))

The official function (modified to output in the chat frame) when you have no play time left at all:
 print(string.format(PLAYTIME_UNHEALTHY, REQUIRED_REST_HOURS - math.floor(GetBillingTimeRested()/60)))

==Details==
* Only relevant on Chinese realms.
* When you reach 3 hours remaining you will get "tired", reducing both the amount of money and experience that you receive by 1/2
* If you play for 5 hours you will get "unhealthy", and won't be able to turn in quests, receive experience or loot.
* The time left is stored on your account, and will display the same amount on every character.
* The time will decay as you stay logged out.

==See also==
* {{api|PartialPlayTime}}
* {{api|NoPlayTime}}
```