# API GetNumSavedInstances

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of instances for which the character is locked out.
 numInstances = GetNumSavedInstances()

==Returns==
:;numInstances:{{apitype|number}} - number of instances with available lockouts, 0 if none.

==Details==
* Returns the number of records that can be queried via {{api|GetSavedInstanceInfo}}(...).
* The count returned includes not just locked instances, but expired and extended lockouts as well.
* The count does not include world bosses, which use {{api|GetNumSavedWorldBosses}}().

==Patch changes==
* {{Patch 1.11.0|note=Added.}}

==See also==
* {{api|GetSavedInstanceInfo}}(...) - drills down to a specific saved instance
* {{api|GetNumSavedWorldBosses}}() - same function as this, but for [[world boss]]es
```