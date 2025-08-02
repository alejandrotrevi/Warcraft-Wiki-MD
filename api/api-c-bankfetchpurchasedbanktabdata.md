# API C Bank.FetchPurchasedBankTabData

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Bank|system=Bank}}
Needs summary.
 purchasedBankTabData = C_Bank.FetchPurchasedBankTabData(bankType)

==Arguments==
:;bankType:{{apitype|Enum.BankType}}
{{:Enum.BankType|nocaption=1}}

==Returns==
:;purchasedBankTabData:{{apitype|BankTabData[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|ID}} || {{apitype|number}} || 
|-
| {{apiname|bankType}} || {{apitype|Enum.BankType}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|icon}} || {{apitype|fileID}} || 
|-
| {{apiname|depositFlags}} || {{apitype|Enum.BagSlotFlags}} || 
|-
| {{apiname|tabCleanupConfirmation}} || {{apitype|string}} || <font color="green">11.2.0</font>
|-
| {{apiname|tabNameEditBoxHeader}} || {{apitype|string}} || <font color="green">11.2.0</font>
|}

{{:Enum.BankType}}

{{:Enum.BagSlotFlags}}
```