# API C ContributionCollector.GetContributionAppearance

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns contribution appearance info.
 appearance = C_ContributionCollector.GetContributionAppearance(contributionID, contributionState)

==Arguments==
:;[[ContributionID|contributionID]]:{{apitype|number}}
:;contributionState:<span style="color:#ecbc21">Enum.ContributionState</span>

{{:Enum_ContributionCollector.ContributionState|nocaption=}}

==Returns==
:;appearance:<span class="tttemplatelink"><span style="color:#ecbc21">ContributionAppearance</span>?</span><span style="display:none">Optional, could be <span style="color:#ecbc21">nil</span>.</span>

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| stateName || {{apitype|string}} || 
|-
| stateColor || {{apitype|ColorMixin}} || 
|-
| tooltipLine || {{apitype|string}} || 
|-
| tooltipUseTimeRemaining || {{apitype|boolean}} || 
|-
| statusBarAtlas || {{apitype|string}} || 
|-
| borderAtlas || {{apitype|string}} || 
|-
| bannerAtlas || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```