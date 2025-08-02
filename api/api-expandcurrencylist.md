# API ExpandCurrencyList

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Alters the expanded state of a currency list header.
 ExpandCurrencyList(id, expanded)

== Arguments ==
; id : Number - Index of the header in the currency list to expand/collapse.
; expanded : Number - 0 to set to collapsed state; 1 to set to expanded state.

== Notes ==
* This function affects the isExpanded return value of the {{api|GetCurrencyListInfo}} API function, but has no immediate impact on the currency UI (which caches the expanded state when it is shown).
* Currencies under collapsed headers are still available to {{api|GetCurrencyListInfo}}, so this is a purely visual switch.
```