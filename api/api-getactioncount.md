# API GetActionCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the available number of uses for an action.
 text = GetActionCount(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - An [[action slot]] ID.

==Returns==
:;text:{{apitype|number}} - How often an item-based action (see details) may be performed; or always zero for other action types.

==Details==
* Use with {{api|IsConsumableAction()}} and {{api|IsStackableAction()}} to confirm that 'zero' is due to having zero uses of an item-based action, rather than always returning zero.
* In Classic, use with {{api|IsItemAction()}} to ignore abilities that require a reagent; or alternatively use with {{api|GetItemCount(itemID)}} if the itemID of a reagent is known.
* In Retail, use with {{api|GetActionCharges()}} for abilities with multiple charges.

==Example==
The following example originates from an older version of [https://www.townlong-yak.com/framexml/5.0.4/ActionButton.lua#404 FrameXML/ActionButton.lua] to display a number on each action button if applicable.
<syntaxhighlight lang="lua">
function ActionButton_UpdateCount (self)
	local text = _G[self:GetName().."Count"];
	local action = self.action;
	if ( IsConsumableAction(action) or IsStackableAction(action) or (not IsItemAction(action) and GetActionCount(action) > 0) ) then
		local count = GetActionCount(action);
		if ( count > (self.maxDisplayCount or 9999 ) ) then
			text:SetText("*");
		else
 			text:SetText(count);
		end
	else
		local charges, maxCharges, chargeStart, chargeDuration = GetActionCharges(action);
		if (maxCharges > 1) then
			text:SetText(charges);
		else
			text:SetText("");
		end
	end
end
</syntaxhighlight>

==Patch changes==
====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.3|note=Now returns zero for spells that require a reagent from your inventory; but still returns the normal value for consumables.}}
```