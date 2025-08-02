# API C Traits.GetTraitCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns meta information about a TraitCurrency, use {{api|C_Traits.GetTreeCurrencyInfo}} if you're looking for TraitCurrency spent/available instead.
 flags, type, currencyTypesID, icon = C_Traits.GetTraitCurrencyInfo(traitCurrencyID)

==Arguments==
:;traitCurrencyID:{{apitype|number}}

==Returns==
:;flags:{{apitype|number}} - any combination of bit flags of {{apitype|Enum.TraitCurrencyFlag}}
:;type:{{apitype|Enum.TraitCurrencyFlag}} - indicates how the TraitCurrency is sourced
:;currencyTypesID:{{apitype|number?}} - [[CurrencyID]], if non-empty, the TraitCurrency is directly linked to the specified Currency
:;icon:{{apitype|number?}} - IconID


{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | Enum.TraitCurrencyFlag
! Value !! Field !! Description
|-
| 0x1 || ShowQuantityAsSpent || Currently not used by any TraitCurrency
|-
| 0x2 || TraitSourcedShowMax|| Currently not used by any TraitCurrency
|-
| 0x4 || UseClassIcon || Currently, all currencies with this flag are TalentTree class talent points
|-
| 0x8 || UseSpecIcon || Currently, all currencies with this flag are TalentTree spec talent points
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | Enum.TraitCurrencyType
! Value !! Field !! Description
|-
| 0 || Gold || Currency used is gold
|-
| 1 || CurrencyTypesBased || TraitCurrencies of this type will spend regular [[CurrencyID]], see currencyTypesID return value
|-
| 2 || TraitSourced || This TraitCurrency can be earned through being above a certain level (e.g. for talent points), earning achievements (e.g. for some profession unlocks,<br>or dragon riding), or by spending points in another TraitNode (e.g. profession unlocks). See {{dbc|traitcurrencysource|TraitCurrencySource.db2}}
|}

{{apinavbox|C_Traits}}
```