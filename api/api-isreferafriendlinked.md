# API IsReferAFriendLinked

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Determines whether the given unit is linked to the player via the Recruit-A-Friend feature.
 isLinked = IsReferAFriendLinked(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;isLinked:Flag : 1 if the unit is RAF-linked to the player, nil otherwise.

==Example==
 function HasRecruitAFriendBonus()
     local numPartyMembers = GetNumPartyMembers();
     if numPartyMembers > 0 then
         local memberID = 1;
         while memberID <= numPartyMembers do
             if GetPartyMember(memberID) == 1 then
                 local member = "party" .. memberID;
                 if UnitIsVisible(member) and IsReferAFriendLinked(member) then
                     return true;
                 end
             end
             memberID = memberID + 1;
         end
     end
     return false;
 end
```