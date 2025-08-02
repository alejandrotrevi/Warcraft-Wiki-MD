# API C CurrencyInfo.FetchCurrencyDataFromAccountCharacters

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Needs summary.
 accountCurrencyData = C_CurrencyInfo.FetchCurrencyDataFromAccountCharacters(currencyID)

==Arguments==
:;currencyID:{{apitype|number}}

==Returns==
:;accountCurrencyData:{{apitype|CharacterCurrencyData[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|characterGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|characterName}} || {{apitype|string}} || 
|-
| {{apiname|fullCharacterName}} || {{apitype|string}} || <font color="green">11.0.2</font>
|-
| {{apiname|currencyID}} || {{apitype|number}} || 
|-
| {{apiname|quantity}} || {{apitype|number}} || 
|}
```