# API ChangeActionBarPage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}}
Changes the current action bar page.
 ChangeActionBarPage(page)

==Arguments==
:;page:{{apitype|number}} - Which page of your action bar to switch to. Expects an integer 1-6.

==Details==
* Notifies the UI that the current action button set has been updated to the current value of the CURRENT_ACTIONBAR_PAGE global variable.
* Will cause an {{api|t=e|ACTIONBAR_PAGE_CHANGED}} event to fire only if there was actually a change (tested in 9.0.5).
```