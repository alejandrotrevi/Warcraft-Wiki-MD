# API NoPlayTime

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns true if the account is considered "unhealthy" for players on Chinese realms.
 isUnhealthy = NoPlayTime()

==Returns==
:;isUnhealthy:{{apitype|boolean?}} - <code>1</code> if the account is "unhealthy", <code>nil</code> if not.

==Example==
 if NoPlayTime() then
    print(string.format(PLAYTIME_UNHEALTHY, REQUIRED_REST_HOURS - math.floor(GetBillingTimeRested()/60)))
 else
    print("You are not limited by NoPlayTime.")
 end

==Details==
* Only relevant on Chinese realms.<ref>{{Ref web|publisher=Abacus News|author=Josh Ye|date=20191105|title=Kids can only play games for 90 minutes a day in China|url=https://www.abacusnews.com/games/kids-can-only-play-games-90-minutes-day-china/article/3036442}}</ref>
* The time left is stored on your account, and will display the same amount on every character.

==Patch changes==
* {{Hotfix|date=2020-02-05|note=Playtime now limited to 90 minutes daily between 08:00 and 22:00 local<ref>{{ref web|title=Blizzard puts curfew on underage Overwatch and WoW gamers in China|url=https://www.scmp.com/tech/article/3049181/blizzard-puts-curfew-underage-overwatch-and-wow-gamers-china|publisher=South China Morning Post|author=Abacus|date=2020-02-05}}</ref><ref>{{ref web|url=https://www.battlenet.com.cn/support/article/2526|title=Blizzard Games - Restrictions and Instructions for Minor Protection|accessdate=2020-02-29|language=cn|author=Blizzard Entertainment}}</ref>|comment=Previous allowed up to 5 hours of playtime, including overnight, with {{api|PartialPlayTime|partially reduced}} currency gain after 3 hours.}}

==See also==
* {{api|GetBillingTimeRested}} - The remaining time until this restriction comes into effect
* {{api|PartialPlayTime}} - A form of limited restriction (-50% to xp and currency) that is presumably removed from the game

==References==
{{reflist|2}}
```