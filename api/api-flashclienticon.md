# API FlashClientIcon

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Flashes the game client icon in the Operating System.
 FlashClientIcon([briefly])

==Arguments==
:;briefly:{{apitype|boolean?|default=false}}

==Example==
* Flashes the client icon after 5 seconds.
 /run C_Timer.After(5, function() FlashClientIcon() end)

* Prevents flashing the client icon by NOP'ing it.
<syntaxhighlight lang="lua">
FlashClientIcon = function() end
</syntaxhighlight>

==Patch changes==
* {{Patch 11.1.5|note=Added <code>briefly</code> argument.}}
* {{Patch 6.2.0|note=Added.}}
```