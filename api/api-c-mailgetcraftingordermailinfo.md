# API C Mail.GetCraftingOrderMailInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Mail|system=MailInfo}}
Needs summary.
 info = C_Mail.GetCraftingOrderMailInfo(inboxIndex)

==Arguments==
:;inboxIndex:{{apitype|number}}

==Returns==
:;info:{{apitype|CraftingOrderMailInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| reason || {{apitype|Enum.RcoCloseReason}} || 
|-
| recipeName || {{apitype|string}} || 
|-
| commissionPaid || {{apitype|number?}} || 
|-
| crafterNote || {{apitype|string?}} || 
|-
| crafterGUID || {{apitype|string?}} || 
|-
| crafterName || {{apitype|string?}} || 
|-
| customerGUID || {{apitype|string?}} || 
|-
| customerName || {{apitype|string?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.RcoCloseReason
! Value !! Field !! Description
|-
| 0 || RcoCloseFulfill || 
|-
| 1 || RcoCloseExpire || 
|-
| 2 || RcoCloseCancel || 
|-
| 3 || RcoCloseReject || 
|-
| 4 || RcoCloseGmCancel || 
|-
| 5 || RcoCloseCrafterFulfill || 
|-
| 6 || RcoCloseInvalid || 
|}
```