# API GetNumShapeshiftForms

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of shapeshift buttons (stances for Warriors, auras for Paladins, forms for Druids, etc) the player currently has.  
 numForms = GetNumShapeshiftForms()

==Returns==
:;numForms:{{apitype|number}} - Number of abilities to be presented on the stance/shapeshift bar

==Details==
The function might return 0 if called before the event UNIT_AURA has fired off.
```