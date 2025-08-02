# API C EditMode.GetLayouts

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EditMode|system=EditModeManager}}
Returns the layouts of any custom layouts that exist. It does not return the layouts of the default layouts.
 layoutInfo = C_EditMode.GetLayouts()

==Returns==
:;layoutInfo:{{apitype|EditModeLayouts}}
{{:Struct EditModeLayouts|nocaption=1}}

==Example Layout==
<syntaxhighlight lang="lua">
local layout = {
    layoutName = "CasualUI",
    layoutType = 3,
    systems = {
        [1] = { -- Action Bar 1
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 2,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 10,
                    setting = 4,
                },
                [6] = { -- Hide Bar Art, 0 = false, 1 = true
                    value = 1,
                    setting = 6,
                },
                [7] = { -- Hide Bar Scrolling, 0 = false, 1 = true
                    value = 1,
                    setting = 8,
                },
                [8] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 1, -- Represents Action Bar "1", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [2] = { -- Action Bar 2
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 2,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 10,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 2, -- Represents Action Bar "2", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [3] = { -- Action Bar 3
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 3, -- Represents Action Bar "3", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [4] = { -- Action Bar 4
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 4, -- Represents Action Bar "4", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [5] = { -- Action Bar 5
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 5, -- Represents Action Bar "5", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [6] = { -- Action Bar 6
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 6, -- Represents Action Bar "6", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [7] = { -- Action Bar 7
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 7, -- Represents Action Bar "7", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [8] = { -- Action Bar 8
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- # of Icons, 6 through 12
                    value = 12,
                    setting = 2,
                },
                [4] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [5] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [6] = { -- Bar Visible, 0 = Always Visible, 1 = In Combat, 2 = Out of Combat, 3 = Hidden
                    value = 0,
                    setting = 5,
                },
                [7] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 8, -- Represents Action Bar "8", because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [9] = { -- Stance Bar
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [4] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 11, -- Represents Action Bar "11" (Stance Bar), because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [10] = { -- Pet Bar
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [4] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
                [5] = { -- Always Show Buttons, 0 = false, 1 = true
                    value = 1,
                    setting = 9,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 12, -- Represents Action Bar "12" (Pet Bar), because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [11] = { -- Possess Bar
            settings = {
                [1] = { -- Orientation: 0 = horizontal, 1 = vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- # of Rows, 1 through 4
                    value = 1,
                    setting = 1,
                },
                [3] = { -- Icon Size, 0 = 50%, 15 = 200%, so "50% + (num x 10%)"
                    value = 5,
                    setting = 3,
                },
                [4] = { -- Icon Padding, 2 through 10
                    value = 2,
                    setting = 4,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 13, -- Represents Action Bar "13" (Possess Bar), because there are multiple Action Bars
            system = 0, -- Represents an "ActionBar" type of element within Edit Mode
        },
        [12] = { -- Castbar
            settings = {
                [1] = { -- Bar Size, 0 through 5, 0 = 100%, 5 = 150%, so "100% + (num x 10%)"
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Lock To Player Frame, 0 = false, 1 = true
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Show Cast Time, 0 = false, 1 = true
                    value = 0,
                    setting = 2,
                },
            },
            anchorInfo = {
                point = "CENTER",
                relativeTo = "UIParent",
                relativePoint = "CENTER",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 1, -- Represents a "CastBar" type of element within Edit Mode
        },
        [13] = { -- Minimap
            settings = {
                [1] = { -- Header Underneath, 0 = false, 1 = true
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Rotate Minimap, 0 = false, 1 = true
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Size, "50% + (num x 10%)"
                    value = 5,
                    setting = 2,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 2, -- Represents a "Minimap" type of element within Edit Mode
        },
        [14] = { -- Player Frame
            settings = {
                [1] = { -- Cast Bar Underneath, 0 = false, 1 = true
                    value = 0,
                    setting = 1,
                },
                [2] = { -- Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 1,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [15] = { -- Target Frame
            settings = {
                [1] = { -- Buffs On Top, 0 = false, 1 = true
                    value = 0,
                    setting = 2,
                },
                [2] = { -- Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 2,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [16] = { -- Focus Frame
            settings = {
                [1] = { -- Use Larger Frame, 0 = false, 1 = true
                    value = 0,
                    setting = 2,
                },
                [2] = { -- [Larger Frame] Buffs On Top, 0 = false, 1 = true
                    value = 0,
                    setting = 3,
                },
                [3] = { -- [Larger Frame] Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 265,
                offsetY = 520,
            },
            isInDefaultPosition = true,
            systemIndex = 3,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [17] = { -- Party Frames
            settings = { -- Settings displayed change based on Raid-Style or not
                [1] = { -- Use Raid-Style Party Frames, 0 = false, 1 = true
                    value = 0,
                    setting = 4,
                },
                [2] = { -- [Party Style] Show Background, 0 = false, 1 = true
                    value = 0,
                    setting = 5,
                },
                [3] = { -- [Raid-Style] Use Horizontal Layout, 0 = false, 1 = true
                    value = 0,
                    setting = 6,
                },
                [4] = { -- [Raid-Style] Frame Width, 0 through 72 (Narrow to Wide)
                    value = 0,
                    setting = 10,
                },
                [5] = { -- [Raid-Style] Frame Height, 0 through 36 (Short to Tall)
                    value = 0,
                    setting = 11,
                },
                [6] = { -- [Raid-Style] Display Border, 0 = false, 1 = true
                    value = 1,
                    setting = 12,
                },
                [7] = { -- [Raid-Style] Sort By, 0 = Role, 1 = Group, 2 = Alphabetical
                    value = 1,
                    setting = 14,
                },
                [8] = { -- [Party Style] Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "TOPLEFT",
                relativeTo = "CompactRaidFrameManager",
                relativePoint = "TOPRIGHT",
                offsetX = -7,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 4,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [18] = { -- Raid Frames
            settings = { -- Some settings only appear under certain conditions
                [1] = { -- Raid Size, 0 = 10, 1 = 25, 2 = 40
                    value = 0,
                    setting = 9,
                },
                [2] = { -- Frame Width, 0 through 72 (Narrow to Wide)
                    value = 0,
                    setting = 10,
                },
                [3] = { -- Frame Height, 0 through 36 (Short to Tall)
                    value = 0,
                    setting = 11,
                },
                [4] = { -- Display Border, 0 = false, 1 = true
                    value = 0,
                    setting = 12,
                },
                [5] = { -- Groups, 0 = Separate Groups (Vertical), 1 = Separate Groups (Horizontal), 2 = Combine Groups (Vertical), 3 = Combine Groups (Horizontal)
                    value = 0,
                    setting = 13,
                },
                [6] = { -- [13: Combine Groups] Sort By, 0 = Role, 1 = Group, 2 = Alphabetical
                    value = 0,
                    setting = 14,
                },
                [7] = { -- [13: Combine Groups] Column/Row Size, 5 through 10
                    value = 5,
                    setting = 15,
                },
            },
            anchorInfo = {
                point = "TOPLEFT",
                relativeTo = "CompactRaidFrameManager",
                relativePoint = "TOPRIGHT",
                offsetX = -5,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 5,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [19] = { -- Boss Frames
            settings = {
                [1] = { -- Use Larger Frame, 0 = false, 1 = true
                    value = 0,
                    setting = 3,
                },
                [2] = { -- Cast Bar on Side, 0 = false, 1 = true
                    value = 1,
                    setting = 7,
                },
                [3] = { -- [Larger Frame] Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 6,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [20] = { -- Arena Frames
            settings = {
                [1] = { -- Frame Width, 0 through 72 (Narrow to Wide)
                    value = 0,
                    setting = 10,
                },
                [2] = { -- Frame Height, 0 through 36 (Short to Tall)
                    value = 0,
                    setting = 11,
                },
                [3] = { -- Display Border, 0 = false, 1 = true
                    value = 0,
                    setting = 12,
                },
                [4] = { -- Arena Size, 0 = 2v2, 1 = 3v3
                    value = 0,
                    setting = 17,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 7,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [21] = { -- Pet Frame
            settings = {
                [1] = { -- Frame Size, 0 through 20, "100% + (num * 5%)"
                    value = 0,
                    setting = 16,
                },
            },
            anchorInfo = {
                point = "CENTER",
                relativeTo = "UIParent",
                relativePoint = "CENTER",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 8,
            system = 3, -- Represents a "UnitFrame" type of element within Edit Mode
        },
        [22] = { -- Encounter Bar
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 4, -- Represents a "EncounterBar" type of element within Edit Mode
        },
        [23] = { -- Extra Abilities
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 5, -- Represents a "ExtraAbilities" type of element within Edit Mode
        },
        [24] = { -- Buff Frames
            settings = {
                [1] = { -- Orientation, 0 = Horizontal, 1 = Vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Icon Wrap, 0 = Down / Left, 1 = Up / Right
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Icon Direction 0 = Left / Down, 1 = Right / Up
                    value = 0,
                    setting = 2,
                },
                [4] = { -- Icon Limit, 2 through 32
                    value = 2,
                    setting = 3,
                },
                [5] = { -- Icon Size, 0 through 15, "50% + (num x 10%)"
                    value = 0,
                    setting = 5,
                },
                [6] = { -- Icon Padding, 5 through 15
                    value = 5,
                    setting = 6,
                },
            },
            anchorInfo = {
                point = "TOPRIGHT",
                relativeTo = "UIParent",
                relativePoint = "TOPRIGHT",
                offsetX = -10,
                offsetY = -255,
            },
            isInDefaultPosition = true,
            systemIndex = 1,
            system = 6, -- Represents a "AuraFrame" type of element within Edit Mode
        },
        [25] = { -- Debuff Frame
            settings = {
                [1] = { -- Orientation, 0 = Horizontal, 1 = Vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Icon Wrap, 0 = Down / Left, 1 = Up / Right
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Icon Direction 0 = Left / Down, 1 = Right / Up
                    value = 0,
                    setting = 2,
                },
                [4] = { -- Icon Limit, 2 through 16
                    value = 8,
                    setting = 4,
                },
                [5] = { -- Icon Size, 0 through 15, "50% + (num x 10%)"
                    value = 5,
                    setting = 5,
                },
                [6] = { -- Icon Padding, 5 through 15
                    value = 5,
                    setting = 6,
                },
            },
            anchorInfo = {
                point = "TOPRIGHT",
                relativeTo = "UIParent",
                relativePoint = "TOPRIGHT",
                offsetX = -155,
                offsetY = -270,
            },
            isInDefaultPosition = true,
            systemIndex = 2,
            system = 6, -- Represents a "AuraFrame" type of element within Edit Mode
        },
        [26] = { -- Talking Head Frame
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 7, -- Represents a "TalkingHeadFrame" type of element within Edit Mode
        },
        [27] = { -- Chat Frame
            settings = { -- Width: 250 - 800, Height: 120 - 800
                [1] = { -- Width (hundreds place), 2 through 8
                    value = 8,
                    setting = 0,
                },
                [2] = { -- Width (tens and ones places), 0 through 99
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Height (hundreds place), 1 through 8
                    value = 8,
                    setting = 2,
                },
                [4] = { -- Height (tens and ones places), 0 through 99
                    value = 0,
                    setting = 3,
                },
            },
            anchorInfo = {
                point = "BOTTOMLEFT",
                relativeTo = "UIParent",
                relativePoint = "BOTTOMLEFT",
                offsetX = 50,
                offsetY = 35,
            },
            isInDefaultPosition = true,
            system = 8, -- Represents a "ChatFrame" type of element within Edit Mode
        },
        [28] = { -- Vehicle Exit Button
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 45,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 9, -- Represents a "VehicleLeaveButton" type of element within Edit Mode
        },
        [29] = { -- Loot Frame
            settings = {},
            anchorInfo = {
                point = "TOPLEFT",
                relativeTo = "UIParent",
                relativePoint = "TOPLEFT",
                offsetX = -116,
                offsetY = 16,
            },
            isInDefaultPosition = true,
            system = 10, -- Represents a "LootFrame" type of element within Edit Mode
        },
        [30] = { -- HUD Tooltip
            settings = {},
            anchorInfo = {
                point = "BOTTOMRIGHT",
                relativeTo = "UIParent",
                relativePoint = "BOTTOMRIGHT",
                offsetX = 85,
                offsetY = -9,
            },
            isInDefaultPosition = true,
            system = 11, -- Represents a "HudTooltip" type of element within Edit Mode
        },
        [31] = { -- ObjectiveTracker
            settings = {
                [1] = { -- [When not in default position] Height, 0 through 60, "400 + (num x 10)"
                    value = 40,
                    setting = 0,
                },
                [2] = { -- Opacity, 0 through 100 (background opacity of ObjectiveTracker)
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Text Size, 0 through 8, "12 + num"
                    value = 0,
                    setting = 2,
                },
            },
            anchorInfo = {
                point = "TOPRIGHT",
                relativeTo = "UIParent",
                relativePoint = "TOPRIGHT",
                offsetX = -275,
                offsetY = -110,
            },
            isInDefaultPosition = true,
            system = 12, -- Represents a "ObjectiveTracker" type of element within Edit Mode
        },
        [32] = { -- Micro Menu
            settings = {
                [1] = { -- Orientation, 0 = Horizontal, 1 = Vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Order, 0 = Default, 1 = Reverse
                    value = 0,
                    setting = 1,
                },
                [3] = { -- Menu Size, 0 through 26, "70% + (num x 5%)"
                    value = 6,
                    setting = 2,
                },
                [4] = { -- Eye Size, 0 through 20, "50% + (num x 5%)"
                    value = 10,
                    setting = 3,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 13, -- Represents a "MicroMenu" type of element within Edit Mode
        },
        [33] = { -- Bags
            settings = {
                [1] = { -- Orientation, 0 = Horizontal, 1 = Vertical
                    value = 0,
                    setting = 0,
                },
                [2] = { -- Direction, 0 = Left / Up, 1 = Right / Down
                    value = 0,
                    setting = 0,
                },
                [3] = { -- Size, 0 through 25, "75% + (num x 5%)"
                    value = 5,
                    setting = 2,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 14, -- Represents a "Bags" type of element within Edit Mode
        },
        [34] = { -- Status Bar 1
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 1,
            system = 15, -- Represents a "StatusTrackingBar" type of element within Edit Mode
        },
        [35] = { -- Status Bar 2
            settings = {},
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 17,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            systemIndex = 2,
            system = 15, -- Represents a "StatusTrackingBar" type of element within Edit Mode
        },
        [36] = { -- Durability Frame
            settings = {
                [1] = { -- Size, 0 through 25, "75% + (num x 5%)"
                    value = 5,
                    setting = 0,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 16, -- Represents a "DurabilityFrame" type of element within Edit Mode
        },
        [37] = { -- Duration Bars
            settings = {
                [1] = { -- Size, 0 through 5, "100% + (num x 10%)"
                    value = 0,
                    setting = 0,
                },
            },
            anchorInfo = {
                point = "TOP",
                relativeTo = "UIParent",
                relativePoint = "TOP",
                offsetX = -100,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 17, -- Represents a "TimerBars" type of element within Edit Mode
        },
        [38] = { -- Vehicle Seat Indicator
            settings = {
                [1] = { -- Size, 0 through 10, "50% + (num x 5%)"
                    value = 10,
                    setting = 0,
                },
            },
            anchorInfo = {
                point = "RIGHT",
                relativeTo = "UIParent",
                relativePoint = "RIGHT",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 18, -- Represents a "VehicleSeatIndicator" type of element within Edit Mode
        },
        [39] = { -- Archaeology Bar
            settings = {
                [1] = { -- Size, 0 through 20, "100% + (num x 5%)"
                    value = 0,
                    setting = 0,
                },
            },
            anchorInfo = {
                point = "BOTTOM",
                relativeTo = "UIParent",
                relativePoint = "BOTTOM",
                offsetX = 0,
                offsetY = 0,
            },
            isInDefaultPosition = true,
            system = 19, -- Represents a "ArchaeologyBar" type of element within Edit Mode
        },
    }
}
</syntaxhighlight>
```