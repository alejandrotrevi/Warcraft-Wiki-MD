# API ItemTextGetPage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the page number of the currently displayed page.
 pageNum = ItemTextGetPage()

==Returns==
:;pageNum:{{apitype|number}} - The page number of the currently displayed page, starting at 1.

==Details==
* This is used once the {{api|t=e|ITEM_TEXT_READY}} event has been received for a page.
* Note that there is no function to return the total number of pages of the text, it must be found by iterating through until [[API ItemTextHasNextPage|ItemTextHasNextPage]] returns nil.
```