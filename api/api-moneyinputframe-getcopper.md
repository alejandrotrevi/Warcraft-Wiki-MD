# API MoneyInputFrame GetCopper

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Returns the amount of money entered in a MoneyInputFrame in copper pieces.

 copper = MoneyInputFrame_GetCopper(moneyFrame)

==Arguments==
:(moneyFrame)

:;moneyFrame:Frame - The money frame, to calculate the copper pieces for.

==Returns==
:;copper:{{apitype|number}} - The amount of money in the specified money frame in copper pieces.
::: 0, if nothing was entered in the money frame (i.e. all editboxes are empty).
```