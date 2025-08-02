# API GetCurrencyListLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get the currencyLink for the specified currency list index.
 currencyLink = GetCurrencyListLink(index)

== Arguments ==
; index : Integer - index, ascending from 1 to {{api|GetCurrencyListSize}}().

== Return values ==
; currencyLink : String - The currency link (similar to [[itemLink]]) for the specified index (e.g. "|cffa335ee|Hcurrency:396|h[Valor Points]|h|r" for Valor Points) or nil if the index is for a header.
```