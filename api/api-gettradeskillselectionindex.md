# API GetTradeSkillSelectionIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the currently selected trade skill.
 local tradeSkillIndex = GetTradeSkillSelectionIndex()

==Parameters==
===Returns===
:;tradeSkillIndex:{{apitype|number}} -  The index of the currently selected trade skill, or 0 if none selected.

==Example==
 if ( GetTradeSkillSelectionIndex() > 1 ) then
   TradeSkillFrame_SetSelection(GetTradeSkillSelectionIndex());
 else
   if ( GetNumTradeSkills() > 0 ) then
     TradeSkillFrame_SetSelection(GetFirstTradeSkill());
   end;
 end;
```