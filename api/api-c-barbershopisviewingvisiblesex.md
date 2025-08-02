# API C BarberShop.IsViewingVisibleSex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_BarberShop|system=BarberShop}}
Returns whether the currently visible body type at the barber shop is the same as '''sexId'''
 isVisibleSex = C_BarberShop.IsViewingVisibleSex(sex)

==Arguments==
:;sex:{{apitype|number}} - Ranging from <code>0</code> for body type 1 (masculine/male) to <code>1</code> for body type 2 (feminine/female)

==Returns==
:;isVisibleSex:{{apitype|boolean}} - <code>true</code> if the visible body type at barber shop UI matches '''sex''', otherwise <code>false</code>
```