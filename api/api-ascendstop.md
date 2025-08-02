# API AscendStop

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Called when the player releases the jump key.
 AscendStop()

==Details==
* This doesn't appear to affect the actual jump at all, but may be hooked to monitor when the jump key is released.
* Called as the jump key is released, regardless if you are in the middle of the jump or held it down until the jump finished.

==Example==
Prints "Jump Released" when releasing the jump key.
<syntaxhighlight lang="lua">
hooksecurefunc("AscendStop", function()
	DEFAULT_CHAT_FRAME:AddMessage( "Jump Released" )
end)
</syntaxhighlight>

==See also==
* {{api|JumpOrAscendStart}}
```