# API OfferPetition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Offers a petition to your target.
 OfferPetition()

==Macro==
You can efficiently ask for peition signatures with a macro like this one:
 #showtooltip
 /use item:5863
 /run local s,t={},UnitName("target")for i=1,GetNumPetitionNames()do s[GetPetitionNameInfo(i)]=1 end if GetPetitionInfo()and t and not s[t]then OfferPetition()end
```