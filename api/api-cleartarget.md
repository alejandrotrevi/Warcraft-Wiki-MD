# API ClearTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=TargetScript}} {{restrictedapi|protected|note=Use [[SecureActionButtonTemplate]]'s <code>"target"</code> action type, or the [[MACRO cleartarget|/cleartarget]] slash command.}}
Clears the selected target.
 willMakeChange = ClearTarget()

==Returns==
:;willMakeChange:{{apitype|boolean}}

==Patch changes==
* {{Patch 10.1.7|note=As of 2023-09-19 this appeared to be unprotected (build 53313) but was hotfixed shortly after.}}
* {{Patch 2.0.1|note=Protected.}}
```