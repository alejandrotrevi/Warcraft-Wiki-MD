# API ItemTextHasNextPage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if there is a page after the current page.
 hasNext = ItemTextHasNextPage()

==Returns==
:;hasNext:{{apitype|boolean}} - Returns true if the there is a page following the currently displayed one, false otherwise.

==Details==
: This is available once the {{api|t=e|ITEM_TEXT_READY}} event has been received.
```