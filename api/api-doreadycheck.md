# API DoReadyCheck

**Contributor:** PGSleepy

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Initiates a ready check.
 DoReadyCheck()

==Details==
This function initiates a raid ready check and will cause all raid members to receive a READY_CHECK event. Processing of the ready check results appear to be either server-side or internal to the client and do not seem to be directly available to the scripting system.  

Since there's no event that emits when everyone is ready, you'll have to use CHAT_MSG_SYSTEM events and check if the message contains the string "Everyone is Ready", which is server-sided emitted to the player when everyone is ready in a party.

You can accomplish this by registering the event.
    local frame = CreateFrame("Frame") --Create the frame
    frame:RegisterEvent("CHAT_MSG_SYSTEM") --Register the event
    frame:SetScript("OnEvent", function(self, event, msg) --When the event fires do:
        if strfind(msg, "Everyone is Ready") then --Check if the System Message contains the string "Everyone is Ready".
            --Insert code for when all players are ready!
        end
    end)
```