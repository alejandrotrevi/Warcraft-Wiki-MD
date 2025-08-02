# API GetLFGProposal

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the current LFD group invite.
 proposalExists, id, typeID, subtypeID, name, texture, role, hasResponded, totalEncounters, completedEncounters, numMembers, isLeader, isHoliday, proposalCategory = GetLFGProposal()

==Returns==
:;proposalExists:{{apitype|boolean}} - true if your character has a pending LFD invitation, nil otherwise.
:;id:{{apitype|number}} - dungeonID (?)
:;typeID:{{apitype|number}} - LFG type ID - one of <code>TYPEID_DUNGEON</code> (1), <code>TYPEID_RANDOM_DUNGEON</code> (6).
:;subtypeID:{{apitype|number}} - One of the <code>LFG_SUBTYPEID_*<code> values:
:* LFG_SUBTYPEID_DUNGEON = 1
:* LFG_SUBTYPEID_HEROIC = 2
:* LFG_SUBTYPEID_RAID = 3
:* LFG_SUBTYPEID_SCENARIO = 4
:* LFG_SUBTYPEID_FLEXRAID = 5
:;name:{{apitype|string}} - Instance name (unless the invitation is to a random dungeon).
:;texture:{{apitype|string}} - Invitation background texture name (appended to "Interface\\LFGFrame\\UI-LFG-BACKGROUND-").
:;role:{{apitype|string}} - Proposed player role; one of "HEALER", "TANK", "DAMAGER", or "NONE".
:;hasResponded:{{apitype|boolean}} - true if your character has already accepted/rejected the invitation, false otherwise.
:;totalEncounters:{{apitype|number}} - total number of bosses in the dungeon.
:;completedEncounters:{{apitype|number}} - number of bosses in the dungeon already killed.
:;numMembers:{{apitype|number}} - number of members in the proposed party.
:;isLeader:{{apitype|boolean}} - true if your character is selected to be the party leader, false otherwise.
:;isHoliday:{{apitype|boolean}} - true if the proposal is for a holiday event queue, false otherwise.
:;proposalCategory:{{apitype|number}} - queue category; one of the <code>[[LE_LFG_CATEGORY]]</code> constants.

==See also==
* {{api|AcceptProposal}}
* {{api|RejectProposal}}
```