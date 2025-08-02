# API PetStopAttack

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0.1; Fails silently if called from an insecure execution path in combat. Consider using /petpassive instead.}}
Stops the pet from attacking.
 PetStopAttack()

==Details==
* This function is not called by FrameXML, and is only effective if called by addons while not in combat.

==Patch changes==
* {{Patch 2.0.1|note=Fails silently if called from a tainted execution path during combat lockdown.}}

==See also==
* {{api|PetAttack}}
```