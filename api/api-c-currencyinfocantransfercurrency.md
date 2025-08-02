# API C CurrencyInfo.CanTransferCurrency

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Needs summary.
 canTransferCurrency, failureReason = C_CurrencyInfo.CanTransferCurrency(currencyID)

==Arguments==
:;currencyID:{{apitype|number}}

==Returns==
:;canTransferCurrency:{{apitype|boolean}}
:;failureReason:{{apitype|Enum.AccountCurrencyTransferResult?}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Success}} || 
|-
| 1 || {{apiname|InvalidCharacter}} || 
|-
| 2 || {{apiname|CharacterLoggedIn}} || 
|-
| 3 || {{apiname|InsufficientCurrency}} || 
|-
| 4 || {{apiname|MaxQuantity}} || 
|-
| 5 || {{apiname|InvalidCurrency}} || 
|-
| 6 || {{apiname|NoValidSourceCharacter}} || 
|-
| 7 || {{apiname|ServerError}} || 
|-
| 8 || {{apiname|CannotUseCurrency}} || 
|}
```