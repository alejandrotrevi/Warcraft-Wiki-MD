# API GetBindingAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the binding name for a key (combination).
 action = GetBindingAction(binding[, checkOverride])

==Arguments==
:;binding:{{apitype|string}} - The name of the key (eg. "BUTTON1", "1", "CTRL-G")
:;checkOverride:{{apitype|boolean?}} - if true, override bindings will be checked, otherwise, only default (bindings.xml/SetBinding) bindings are consulted.

==Returns==
:;action:{{apitype|string}} - action command performed by the binding. If no action is bound to the key, an empty string is returned.

==See also==
* {{api|GetBindingByKey}}
```