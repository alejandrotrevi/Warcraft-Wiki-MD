# API GetBonusBarOffset

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current bonus action bar index (e.g. for the Rogue stealth bar).
 offset = GetBonusBarOffset()

==Returns==
:;offset:{{apitype|number}} - The current bonus action bar index.

==Details==
Certain classes have "bonus action bars" for their class-specific actions, e.g. the various [[Stance|Stance Bars]] for the [[Warrior]] class.  GetBonusBarOffset() returns the index of the current action bar that is being displayed.  Note that simply scrolling through the action bar pages won't change the output; only switching to the different bonus bars.  Each class has their own way of indexing their bonus bars.

{| class="darktable" style="margin-left: 3.9em"
|
'''Warrior'''
* Battle Stance: 1
* Defensive Stance: 2
* Berserker Stance: 3

'''Druid'''
* Caster: 0
* Cat: 1
* Tree of Life: 2
* Bear: 3
* Moonkin: 4

'''Rogue'''
* Normal: 0
* Stealthed: 1

'''Priest'''
* Normal: 0
* Shadowform: 1

'''All Characters'''
* When Possessing a Target: 5
|}

==Example==
This will simply print the output of GetBonusBarOffset().  It should change as you change between your bonus bars.
 /script ChatFrame1:AddMessage(GetBonusBarOffset())

Here, slotID will be the action slot number for the first slot of the current bonus bar.  For example, for a Warrior in Defensive Stance, <code>slotID = 85</code>, which is correct. ([[ActionSlot]])
 slotID = (1 + (NUM_ACTIONBAR_PAGES + GetBonusBarOffset() - 1) * NUM_ACTIONBAR_BUTTONS)
```