# API SpellStopTargeting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "stop" action type of [[SecureActionButtonTemplate]] or the [[MACRO stopspelltarget|/stopspelltarget]] slash command.}}
Cancels the spell awaiting target selection.
 SpellStopTargeting()

==Details==
* Also cancels some types of weapon buffs when they ask for confirmation.  For example, if you attempt to apply a poison to a weapon that already has a poison, the game will ask you to confirm the replacement.  You can accept the replacement with ReplaceEnchant() or cancel the replacement with SpellStopTargeting().

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```