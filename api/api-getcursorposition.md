# API GetCursorPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the cursor's position on the screen.
 x, y = GetCursorPosition()

==Returns==
:;x:{{apitype|number}} - x coordinate unaffected by UI scale; 0 at the left edge of the screen.
:;y:{{apitype|number}} - y coordinate unaffected by UI scale; 0 at the bottom edge of the screen.

==Details==
* Returns scale-independent coordinates similar to Cursor:GetCenter() if 'Cursor' was a valid frame not affected by scaling.
* Assuming UIParent spans the entire screen, you can convert these coordinates to UIParent offsets by dividing by its effective scale. The following snippet positions a small texture at the cursor's location.
 local uiScale, x, y = UIParent:GetEffectiveScale(), GetCursorPosition()
 local tex = UIParent:CreateTexture()
 tex:SetTexture(1,1,1)
 tex:SetSize(4,4)
 tex:SetPoint("CENTER", nil, "BOTTOMLEFT", x / uiScale, y / uiScale)
```