# API DeclineGroup

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Declines an invitation to a group.
 DeclineGroup()

==Example==
The following snippet auto-declines invitations from characters whose names contain Ghost.
<syntaxhighlight lang="lua">
local frame = CreateFrame("FRAME")
frame:RegisterEvent("PARTY_INVITE_REQUEST")
frame:SetScript("OnEvent", function(self, event, sender)
	if sender:match("Ghost") then
	     DeclineGroup()
	end
end)
</syntaxhighlight>

==Details==
*You can use this after recieving the {{api|t=e|PARTY_INVITE_REQUEST}} event. If there is no invitation to a party, this function doesn't do anything.
*Calling this function does NOT cause the "accept/decline dialog" to go away. Use {{api|StaticPopup_Hide}}("PARTY_INVITE") to hide the dialog.
*:Depending on the order events are dispatched in, your event handler may run before UIParent's, and therefore attempt to hide the dialog before it is shown. Delaying the attempt to hide the popup until {{api|t=e|PARTY_MEMBERS_CHANGED}} resolves this.
```