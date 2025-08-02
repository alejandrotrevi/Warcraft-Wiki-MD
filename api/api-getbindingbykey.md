# API GetBindingByKey

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the binding action performed when the specified key combination is triggered.
 bindingAction = GetBindingByKey(key)

==Arguments==
:;key:{{apitype|string}} - binding key to query, e.g. "G", "ALT-G", "ALT-CTRL-SHIFT-F1".

==Returns==
:;bindingAction:{{apitype|string}} - binding action that will be performed, e.g. "TOGGLEAUTORUN", "CLICK Purrseus:k1", or nil if no action will be performed.

==Details==
* This function takes into account override bindings by default.
* This discards modifiers from the <code>key</code> argument until a binding matches; thus, querying for <code>ALT-CTRL-SHIFT-G</code> can return the action performed due to the simple "G" binding.

==See also==
* {{api|GetBindingAction}}
```