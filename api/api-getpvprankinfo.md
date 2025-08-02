# API GetPVPRankInfo

**Contributor:** Surafbrov

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a specific PvP rank.
 rankName, rankNumber = GetPVPRankInfo(rankID [, faction])

==Arguments==
:;rankID:{{apitype|number}} - The PvP rank ID as returned by {{api|UnitPVPRank}}()
:;faction:{{apitype|number?}} - 0 for Horde, 1 for Alliance. Defaults to the player's faction. Previously accepted a [[UnitId]] but now takes a faction ID.<sup>[https://github.com/Gethe/wow-ui-source/blob/163ac1f68d1026f4faad2eb27a54838f080bc21a/FrameXML/WorldStateFrame.lua#L188]</sup>

==Returns==
:;rankName:{{apitype|string}} - The localized name of the PvP rank.
:;rankNumber:{{apitype|number}} - The PvP rank number.

==Values==
<onlyinclude>Dishonorable ranks like "Pariah" exist but were never used in Vanilla.
{| class="sortable darktable zebra col1-center""
|-
! Rank ID !! Alliance !! Horde !! Rank Number
|-
| 0 || || || <center>0</center>
|-
| 1 || Pariah || Pariah || <center>-4</center>
|-
| 2 || Outlaw || Outlaw || <center>-3</center>
|-
| 3 || Exiled || Exiled || <center>-2</center>
|-
| 4 || Dishonored || Dishonored || <center>-1</center>
|-
| 5 || [[Private (Legacy)|Private]] || [[Scout (Legacy)|Scout]] || <center>1</center>
|-
| 6 || [[Corporal (Legacy)|Corporal]] || [[Grunt (Legacy)|Grunt]] || <center>2</center>
|-
| 7 || [[Sergeant (legacy)|Sergeant]] || [[Sergeant (legacy)#Horde|Sergeant]] || <center>3</center>
|-
| 8 || [[Master Sergeant (Legacy)|Master Sergeant]] || [[Senior Sergeant (Legacy)|Senior Sergeant]] || <center>4</center>
|-
| 9 || [[Sergeant Major (Legacy)|Sergeant Major]] || [[First Sergeant (Legacy)|First Sergeant]] || <center>5</center>
|-
| 10 || [[Knight (Legacy)|Knight]] || [[Stone Guard (Legacy)|Stone Guard]] || <center>6</center>
|-
| 11 || [[Knight-Lieutenant (Legacy)|Knight-Lieutenant]] || [[Blood Guard (Legacy)|Blood Guard]] || <center>7</center>
|-
| 12 || [[Knight-Captain (Legacy)|Knight-Captain]] || [[Legionnaire (Legacy)|Legionnaire]] || <center>8</center>
|-
| 13 || [[Knight-Champion (Legacy)|Knight-Champion]] || [[Centurion (Legacy)|Centurion]] || <center>9</center>
|-
| 14 || [[Lieutenant Commander (Legacy)|Lieutenant Commander]] || [[Champion (Legacy)|Champion]] || <center>10</center>
|-
| 15 || [[Commander (Legacy)|Commander]] || [[Lieutenant General (Legacy)|Lieutenant General]] || <center>11</center>
|-
| 16 || [[Marshal (Legacy)|Marshal]] || [[General (Legacy)|General]] || <center>12</center>
|-
| 17 || [[Field Marshal (Legacy)|Field Marshal]] || [[Warlord (Legacy)|Warlord]] || <center>13</center>
|-
| 18 || [[Grand Marshal (Legacy)|Grand Marshal]] || [[High Warlord (Legacy)|High Warlord]] || <center>14</center>
|}</onlyinclude>

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
* {{Patch 1.4.0|note=Added.}}
```