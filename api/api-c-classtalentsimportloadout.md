# API C ClassTalents.ImportLoadout

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Needs summary.
 success, importError = C_ClassTalents.ImportLoadout(configID, entries, name)

==Arguments==
:;configID:{{apitype|number}}
:;entries:{{apitype|ImportLoadoutEntryInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| nodeID || {{apitype|number}} || 
|-
| ranksPurchased || {{apitype|number}} || 
|-
| selectionEntryID || {{apitype|number}} || 
|}
:;name:{{apitype|string}}

==Returns==
:;success:{{apitype|boolean}}
:;importError:{{apitype|string}}

{{apinavbox|C_Traits}}
```