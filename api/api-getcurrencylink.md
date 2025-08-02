# API GetCurrencyLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get the currencyLink for the specified currencyID.
 currencyLink = GetCurrencyLink(currencyID,currencyAmount)

== Arguments ==
; currencyID : Integer - currency index - see table at {{api|GetCurrencyInfo}} for a list
; currencyAmount : Integer - currency amount

== Return values ==
; currencyLink : String - The currency link (similar to [[itemLink]]) for the specified index (e.g. "|cffa335ee|Hcurrency:396:0|h[Valor Points]|h|r" for Valor Points) or nil if the index is for a header.

== See also ==
*{{api|GetCurrencyListLink}} (for currencies visible in the currency tab)
```