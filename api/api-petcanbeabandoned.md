# API PetCanBeAbandoned

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the pet can be abandoned.

 canAbandon = PetCanBeAbandoned()

==Returns==
:;canAbandon:{{apitype|boolean}} - <code>true</code> if the player's pet can be abandoned.

==Example==
<syntaxhighlight lang="lua">
if ( PetCanBeAbandoned() ) then PetAbandon(); end
</syntaxhighlight>
```