# API C MountJournal.Dismiss

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Dismisses the currently summoned mount.

 C_MountJournal.Dismiss()

==Triggers events==
* {{api|t=e|COMPANION_UPDATE}}, at which time {{api|IsMounted}}() will correctly return false

==Details==
* Has no result if the player is not mounted.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_MountJournal.SummonByID}}
```