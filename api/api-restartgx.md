# API RestartGx

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Restarts the graphics engine.
 RestartGx()

----
;''Example''
  SetCVar("gxResolution","1024x768")
  RestartGx()

;''Result''
 ''-- Graphical engine is restarted in 1024x768 resolution.''

----
;''Description''

: Primarily necessary for editing various display settings on the fly. Will not circumvent options that request you restart WoW for them to take effect.
```