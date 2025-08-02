# API GetTrainerServiceDescription

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the description of a specific trainer service.
 serviceDescription = GetTrainerServiceDescription(index)

==Arguments==
:;index:{{apitype|number}} - The index of the specific trainer service.

==Returns==
:;serviceDescription:{{apitype|string}} - The description of a specific trainer service. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].

==Example==
Prints the description of the trainer service with index 3, in the chatwindow
 print(GetTrainerServiceDescription(3))

 > "Permanently enchant a weapon to often deal 20 Nature damage to an enemy damaged by your spells or struck by your melee attacks. Cannot be applied to items higher than level 136."
```