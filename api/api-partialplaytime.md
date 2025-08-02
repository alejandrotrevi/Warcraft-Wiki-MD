# API PartialPlayTime

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns true if the account is considered "tired" for players on Chinese realms.
 isTired = NoPlayTime()

==Returns==
:;isTired:{{apitype|boolean?}} - <code>1</code> if the account is "tired", <code>nil</code> if not. See details below for clarification. Returns <code>nil</code> for EU and US accounts.

==Example==
Based on the official function, changed a bit to output the text in the chat rather than the tooltip on your avatar:
 if PartialPlayTime() then
    print(string.format(PLAYTIME_TIRED, REQUIRED_REST_HOURS - math.floor(GetBillingTimeRested()/60)))
 elseif NoPlayTime() then
    print(string.format(PLAYTIME_UNHEALTHY, REQUIRED_REST_HOURS - math.floor(GetBillingTimeRested()/60)))
 else
    print("You are not limited by PartialPlayTime nor NoPlayTime.")
 end

==Details==
* Only relevant on Chinese realms.
* When you reach 3 hours remaining you will get "tired", reducing both the amount of money and experience that you receive by 50%.
* If you play for 5 hours you will get "unhealthy", and won't be able to turn in quests, receive experience or loot.
* The time left is stored on your account, and will display the same amount on every character.
* The time will decay as you stay logged out.

==See also==
* {{api|GetBillingTimeRested}}
* {{api|NoPlayTime}}
```