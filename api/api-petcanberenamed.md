# API PetCanBeRenamed

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.7|removed=11.0.2}}
Returns true if the pet can be renamed.
 canRename = PetCanBeRenamed()

==Returns==
:;canRename:{{apitype|boolean}} - <code>true</code> if the player's pet can be renamed.

==Example==
<syntaxhighlight lang="lua">
if ( PetCanBeRenamed() ) then PetRename("Fuzzy Wuzzy"); end
</syntaxhighlight>
```