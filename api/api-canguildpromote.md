# API CanGuildPromote

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player can promote guild members.
 canPromote = CanGuildPromote()

==Returns==
:;canPromote:{{apitype|boolean}} - Returns 1 if the player can promote, nil if not.

==Example==
 if( CanGuildPromote() ) then
   -- do stuff
 end
```