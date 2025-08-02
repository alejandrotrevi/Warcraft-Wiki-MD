# API CloseLoot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Close the loot window.

 CloseLoot([errNum])

==Arguments==
:;errNum:{{apitype|number?}} - A reason for the window closing.  Unsure whether/how the game deals with error codes passed to it.

==Triggers events==
* {{api|t=e|LOOT_CLOSED}}

==Details==
Pretty self-explanatory.  Unless there is some type of error, don't pass the error argument.
```