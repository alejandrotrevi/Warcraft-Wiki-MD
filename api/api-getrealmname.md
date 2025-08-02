# API GetRealmName

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the realm name.
 realm = GetRealmName()
 normalizedRealm = GetNormalizedRealmName()

==Returns==
:;realm:{{apitype|string}} - The name of the realm.
:;normalizedRealm:{{apitype|string?}} - The name of the realm without spaces, <code>-</code> hyphens, or <code>.</code> periods.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetRealmID}} }}
|}
* The normalized realm name is used for addressing whispers<ref>{{ref web|author=SDPhantom|date=2020-02-18|url=https://www.wowinterface.com/forums/showthread.php?t=57826#5|
publisher=[[WoWInterface]]|title=Re: Party members with server name?}}</ref> and in-game mail.
* When logging in, <code>GetNormalizedRealmName()</code> only returns information starting from as early as the {{api|t=e|PLAYER_LOGIN}} event.
: <syntaxhighlight lang="lua">
-- GetTime(), event, GetRealmName(), GetNormalizedRealmName()
11647.589 VARIABLES_LOADED: "Defias Brotherhood", nil
11647.655 PLAYER_LOGIN: "Defias Brotherhood", "DefiasBrotherhood"
11647.655 PLAYER_ENTERING_WORLD: "Defias Brotherhood", "DefiasBrotherhood"
</syntaxhighlight>
* When transitioning through a loading screen, <code>GetNormalizedRealmName()</code> may return nil between the {{api|t=e|LOADING_SCREEN_ENABLED}} and {{api|t=e|LOADING_SCREEN_DISABLED}} events.

==Example==
A small list of realm IDs and names.
<syntaxhighlight lang="lua">
-- /dump GetRealmID(), GetRealmName(), GetNormalizedRealmName()
503, "Azjol-Nerub", "AzjolNerub"
513, "Twilight's Hammer", "Twilight'sHammer"
635, "Defias Brotherhood", "DefiasBrotherhood"
1049, "憤怒使者", "憤怒使者"
1093, "Ahn'Qiraj", "Ahn'Qiraj"
1413, "Aggra (Português)", "Aggra(Português)"
1925, "Вечная Песня", "ВечнаяПесня"
</syntaxhighlight>

==Patch changes==
* {{Patch 5.4.1|note=CVar {{api|t=c|realmName}} was removed<ref>{{Ref web|title=GetCVar("realmName") gives nil|url=https://www.mmo-champion.com/threads/1375675-GetCVar(-quot-realmName-quot-)-gives-nil|publisher=[[MMO-Champion]]|date=20141030|author=SpaceDuck, Mule}}</ref>.}}
* {{Patch 1.5.0|note=Added.}}

==See also==
* {{api|UnitName}}() - Returns a character name and the server (if different from the player's current server)

==References==
```