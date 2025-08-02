# API C CurrencyInfo.FetchCurrencyTransferTransactions

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Needs summary.
 currencyTransferTransactions = C_CurrencyInfo.FetchCurrencyTransferTransactions()

==Returns==
:;currencyTransferTransactions:{{apitype|CurrencyTransferTransaction[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|sourceCharacterGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|sourceCharacterName}} || {{apitype|string?|default=}} || 
|-
| {{apiname|fullSourceCharacterName}} || {{apitype|string?|default=}} || <font color="green">11.0.2</font>
|-
| {{apiname|destinationCharacterGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|destinationCharacterName}} || {{apitype|string?|default=}} || 
|-
| {{apiname|fullDestinationCharacterName}} || {{apitype|string?|default=}} || <font color="green">11.0.2</font>
|-
| {{apiname|currencyType}} || {{apitype|number}} || 
|-
| {{apiname|quantityTransferred}} || {{apitype|number}} || 
|-
| {{apiname|totalQuantityConsumed}} || {{apitype|number}} || 
|-
| {{apiname|timestamp}} || {{apitype|time_t}} || 
|}
```