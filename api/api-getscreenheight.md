# API GetScreenHeight

**Contributor:** AlternativeTheory

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the height of the window measured at [[UIParent]] scale (effectively the same as UIParent:GetHeight().
 screenHeight = GetScreenHeight()

==Returns==
:;screenHeight:{{apitype|number}} - Height of window at [[UIParent]] scale

==Example==
<syntaxhighlight lang="lua">
-- Note that the return value does not match the screen resolution set in the Video Options, but will instead represent a dimension with the same aspect ratio.
 DEFAULT_CHAT_FRAME:AddMessage( ( GetScreenWidth() * UIParent:GetEffectiveScale() ).."x"..( GetScreenHeight() * UIParent:GetEffectiveScale() ) )
</syntaxhighlight>
```