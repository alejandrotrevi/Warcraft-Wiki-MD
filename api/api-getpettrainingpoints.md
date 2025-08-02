# API GetPetTrainingPoints

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the training point information about the current pet.
 totalPoints, spent = GetPetTrainingPoints()

==Returns==
:;totalPoints:{{apitype|number}} - The total of points spent and points available.
:;spent:{{apitype|number}} - The number of points spent.

==Patch changes==
* {{Patch 3.0.2|note=Removed. Pets now have talents rather than trainable skills.}}
```