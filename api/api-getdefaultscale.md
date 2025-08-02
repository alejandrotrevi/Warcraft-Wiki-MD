# API GetDefaultScale

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the default UI scaling value for the current screen size.
 scale = GetDefaultScale()

==Returns==
:;scale:{{apitype|number}} - The default scale for the UI as a floating point value.

==Example==

The below example creates an unparented frame that will always render at a size of 300x300 pixels. The scale of the frame is managed through the inherited DefaultScaleFrame template, which internally uses this API to apply the correct scale to the frame if the screen size changes.

<syntaxhighlight lang="lua">
UnscaledFrame = CreateFrame("Frame", nil, nil, "BackdropTemplate, DefaultScaleFrame")
UnscaledFrame:SetPoint("CENTER")
UnscaledFrame:SetSize(300, 300)
UnscaledFrame:SetBackdrop({ bgFile = [[Interface\Buttons\White8x8]] })
</syntaxhighlight>
```