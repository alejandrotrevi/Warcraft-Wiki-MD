# API SetPVP

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Sets the player's PvP flag.
 SetPVP(flag)

==Arguments==
:;flag:{{apitype|number}}

==Details==
* <code>TogglePVP()</code> is equivalent to <code>SetPVP(not GetPVPDesired())</code>
* This setting is different from war mode.
```