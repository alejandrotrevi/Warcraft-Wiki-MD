# API ClearOverrideBindings

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}}
Removes all override bindings owned by a specific frame.
 ClearOverrideBindings(owner)

==Arguments==
:;owner:{{apitype|Frame}} - The frame to clear override bindings for.

==Details==
* The client will automatically restore overridden bindings once override bindings are cleared.
```