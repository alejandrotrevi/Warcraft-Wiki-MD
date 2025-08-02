# API C LFGList.CreateListing

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Creates a group finder listing.
 success = C_LFGList.CreateListing(createData)

==Arguments==
:;createData:{{apitype|LfgListingCreateData}}
{{:Struct LfgListingCreateData|nocaption=1}}

==Returns==
:;success:{{apitype|boolean}} - Generally returns true if there was a valid group title.
<!-- 
==Example==
Creates a group listing for "Custom PvE". <font color="#4ec9b0">Requires the title of the listing to have been typed manually, otherwise it silently fails. Setting the title is explicitly protected.</font><sup>[https://github.com/Gethe/wow-ui-source/blob/9.0.2/FrameXML/LFGList.xml#L1687]</sup>
 /run C_LFGList.CreateListing(16, 0, 0)
-->
==Patch changes==
* {{Patch 11.1.0|note=Now returns a structured table.}}
* {{Patch 7.2.0|note=Hardware event protected (build 24015)<sup>[https://us.battle.net/forums/en/wow/topic/20754326419]</sup>}}
* {{Patch 6.0.2|note=Added.}}
```