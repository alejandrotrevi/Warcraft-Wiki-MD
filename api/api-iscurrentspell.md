# API IsCurrentSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified spell ID is currently being casted or queued.
If spell is current then action bar indicates its slot with highlighted frame.
 isCurrent = IsCurrentSpell(spellID)

==Arguments==
:;spellID:{{apitype|number}} - spell ID to query.

==Returns==
:;isCurrent:{{apitype|boolean}} - true if currently being casted or queued, false otherwise.
```