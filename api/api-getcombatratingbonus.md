# API GetCombatRatingBonus

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the bonus percentage for a specific combat rating.
 ratingBonus = GetCombatRatingBonus(ratingIndex)

==Arguments==
:;ratingIndex:{{apitype|number}} - One of the following values from <code class="plainlinks">FrameXML/[https://www.townlong-yak.com/framexml/live/PaperDollFrame.lua PaperDollFrame.lua]</code>:
{{:API GetCombatRating}}

==Returns==
:;ratingBonus:{{apitype|number}} - the actual bonus in percent the combat rating confers; e.g. 5.13452

==Example==
 hitBonus = GetCombatRatingBonus(CR_HIT_MELEE) -- 5.13452

==See also==
* [[API_GetCombatRating|GetCombatRating]]: Get's the underlying rating that contributes to the bonus
* [[API GetCritChance|GetCritChance]]: Gets the players current Crit Chance %
* [[API GetMastery|GetMastery]]: Get the player's current Mastery %
* [[API GetDodgeChance|GetDodgeChance]]: Gets the player's current Dodge Chance %
* [[API GetParryChance|GetParryChance]]: Gets the player's current Parry Chance %
* [[API GetBlockChance|GetBlockChance]]: Gets the player's current Block Chance %
```