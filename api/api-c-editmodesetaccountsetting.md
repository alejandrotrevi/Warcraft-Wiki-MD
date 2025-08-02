# API C EditMode.SetAccountSetting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EditMode|system=EditModeManager}}
Needs summary.
 C_EditMode.SetAccountSetting(setting, value)

==Arguments==
:;setting:{{apitype|Enum.EditModeAccountSetting}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|ShowGrid}} || 
|-
| 1 || {{apiname|GridSpacing}} || 
|-
| 2 || {{apiname|SettingsExpanded}} || 
|-
| 3 || {{apiname|ShowTargetAndFocus}} || 
|-
| 4 || {{apiname|ShowStanceBar}} || 
|-
| 5 || {{apiname|ShowPetActionBar}} || 
|-
| 6 || {{apiname|ShowPossessActionBar}} || 
|-
| 7 || {{apiname|ShowCastBar}} || 
|-
| 8 || {{apiname|ShowEncounterBar}} || 
|-
| 9 || {{apiname|ShowExtraAbilities}} || 
|-
| 10 || {{apiname|ShowBuffsAndDebuffs}} || <font color="green">10.1.0</font> - Renamed from <code>ShowBuffFrame</code> 
|-
| 11 || {{apiname|DeprecatedShowDebuffFrame}} || <font color="green">10.1.0</font> - Renamed from <code>ShowDebuffFrame</code> 
|-
| 12 || {{apiname|ShowPartyFrames}} || 
|-
| 13 || {{apiname|ShowRaidFrames}} || 
|-
| 14 || {{apiname|ShowTalkingHeadFrame}} || 
|-
| 15 || {{apiname|ShowVehicleLeaveButton}} || 
|-
| 16 || {{apiname|ShowBossFrames}} || 
|-
| 17 || {{apiname|ShowArenaFrames}} || 
|-
| 18 || {{apiname|ShowLootFrame}} || 
|-
| 19 || {{apiname|ShowHudTooltip}} || 
|-
| 20 || {{apiname|ShowStatusTrackingBar2}} || <font color="green">10.1.0</font> - Renamed from <code>ShowReputationBar</code> 
|-
| 21 || {{apiname|ShowDurabilityFrame}} || <font color="green">10.0.5</font>
|-
| 22 || {{apiname|EnableSnap}} || 
|-
| 23 || {{apiname|EnableAdvancedOptions}} || 
|-
| 24 || {{apiname|ShowPetFrame}} || 
|-
| 25 || {{apiname|ShowTimerBars}} || 
|-
| 26 || {{apiname|ShowVehicleSeatIndicator}} || 
|-
| 27 || {{apiname|ShowArchaeologyBar}} || 
|-
| 28 || {{apiname|ShowCooldownViewer}} || <font color="green">11.1.5</font>
|}
:;value:{{apitype|number}}
```