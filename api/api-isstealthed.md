# API IsStealthed

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns true if the character is currently stealthed.
 stealthed = IsStealthed()

==Returns==
:;stealthed:{{apitype|boolean}} - true if stealthed, otherwise false

==Details==
* [[Stealth (mechanic)|Stealth]] includes [[Stealth]], [[Prowl]], [[Camouflage]] and [[Shadowmeld]]

==See also==
* {{api|t=e|UPDATE_STEALTH}} - Fires when a player enters or leaves stealth.
* [[Macro conditionals]] - <code>stealth</code> or <code>nostealth</code> may be used in macros or with a [[SecureStateDriver]].
```