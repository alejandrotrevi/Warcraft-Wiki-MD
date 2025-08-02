# API UnitIsTapDenied

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Indicates a mob is no longer eligible for [[tap]].
 unitIsTapDenied = UnitIsTapDenied(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;unitIsTapDenied:{{apitype|boolean}}

==Example==
The following code in FrameXML {{elinks-api/Inline|tly-go=TargetFrame_CheckFaction}} grays out the target frame when the target is tap denied:
<syntaxhighlight lang="lua">
function TargetFrame_CheckFaction (self)
	if ( not UnitPlayerControlled(self.unit) and UnitIsTapDenied(self.unit) ) then
		self.nameBackground:SetVertexColor(0.5, 0.5, 0.5);
		if ( self.portrait ) then
			self.portrait:SetVertexColor(0.5, 0.5, 0.5);
		end
	else
		self.nameBackground:SetVertexColor(UnitSelectionColor(self.unit));
		if ( self.portrait ) then
			self.portrait:SetVertexColor(1.0, 1.0, 1.0);
		end
	end
    -- the function continues with activities not relevant to this example
end
</syntaxhighlight>

==Patch changes==
* {{Patch 7.0.3|note=Added, replacing {{api|UnitIsTapped}}().}}
```