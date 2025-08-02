# API GetExpertisePercent

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns your current expertise reduction to chance to be dodged or parried, in percent.
 expertisePercent, offhandExpertisePercent = GetExpertisePercent()

==Returns==
:;expertisePercent:{{apitype|number}} - Percentage reduction in dodge and parry chances for swings with your main hand weapon.
:;offhandExpertisePercent:{{apitype|number}} - Percentage reduction in dodge and parry chances for swings with your offhand weapon.

==Patch changes==
* {{Patch 11.2.0|note=Readded.}}
* {{Patch 5.0.4|note=Removed, and replaced by {{api|GetExpertise}}.}}
* {{Patch 2.3.0|note=Added.}}
```