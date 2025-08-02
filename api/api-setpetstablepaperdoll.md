# API SetPetStablePaperdoll

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__


Sets the paperdoll model in the pet stable to a new player model.
 SetPetStablePaperdoll(modelObject)


==Arguments==
:;modelObject : [[UIOBJECT PlayerModel|PlayerModel]] - The model of the pet to display.


==Returns==
:None


==Details==

: This method does not cause the model to be shown. The model still needs its Show() method called afterward.
```