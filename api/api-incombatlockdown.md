# API InCombatLockdown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the combat lockdown restrictions are active.
 inLockdown = InCombatLockdown()

==Returns==
:;inLockdown:{{apitype|boolean}} - true if lockdown restrictions are currently in effect, false otherwise.

==Details==
* Combat lockdown begins ''after'' the {{api|t=e|PLAYER_REGEN_DISABLED}} event fires, and ends ''before'' the {{api|t=e|PLAYER_REGEN_ENABLED}} event fires.

===Restrictions===
While in combat:
*Programatic modification of macros or bindings is not allowed.
*Some things can't be done on "Protected" frames, their parents, or any frame they are anchored to. These include, but are not restricted to:
**Hiding the frame using Hide widget method.
**Showing the frame using Show widget method.
**Changing the frame's attributes (custom attributes are used by Blizzard secure templates to set up their behavior).
**Moving the frame by resetting frame's points or anchors (movements initiated by user are still allowed while in combat).
```