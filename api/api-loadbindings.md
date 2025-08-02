# API LoadBindings

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Loads default, account or character specific key bindings.
 LoadBindings(bindingSet)

==Arguments==
:;bindingSet:{{apitype|number}} - Which binding set to load; one of the following three numeric constants:
:* DEFAULT_BINDINGS (0)
:* ACCOUNT_BINDINGS (1)
:* CHARACTER_BINDINGS (2)

==Fires Events==
* {{api|t=e|UPDATE_BINDINGS}} when the binding set has been loaded.

==Details==
* The file it reads from is WTF\Account\ACCOUNTNAME\bindings-cache.wtf.
```