# API IsUsableAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the character can currently use the specified action (sufficient mana, reagents and not on cooldown).
 isUsable, notEnoughMana = IsUsableAction(slot)

==Arguments==
:;slot:{{apitype|number}} - [[Action slot]] to query

==Returns==
:;isUsable:{{apitype|boolean}} - true if the action is currently usable (does not check cooldown or range), false otherwise.
:;notEnoughMana:{{apitype|boolean}} - true if the action is unusable beacuse the player does not have enough mana, rage, etc.; false otherwise.
```