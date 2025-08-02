# API GetCurrentBindingSet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns if either account or character-specific bindings are active.
 which = GetCurrentBindingSet()

==Returns==
:;which:{{apitype|number}} - One of the following values:
:;ACCOUNT_BINDINGS = 1:indicates that account-wide bindings are currently active.
:;CHARACTER_BINDINGS = 2:indicates that per-character bindings are currently active.

==Details==
* The return value of this function depends on the last call to {{api|SaveBindings}}.
```