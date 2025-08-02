# API IsAttackAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if an action is the "Auto Attack" action.
 isAttack = IsAttackAction(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - The action slot to test.

==Returns==
:;isAttack:{{apitype|boolean}} - true if the slot is an attack action and should flash red during combat. false if the specified slot is not an attack action, or is empty.
```