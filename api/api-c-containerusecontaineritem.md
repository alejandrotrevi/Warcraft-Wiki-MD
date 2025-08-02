# API C Container.UseContainerItem

**Contributor:** Boneshock

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
{{restrictedapi|protected|note=Use the "item" action type of [[SecureActionButtonTemplate]] or the [[MACRO cast|/use]] slash command.}}

Uses an item from a container depending on the situation.
 C_Container.UseContainerItem(containerIndex, slotIndex [, unitToken [, bankType [, reagentBankOpen]]])

==Arguments==
:;containerIndex:{{apitype|Enum.BagIndex}}
{{:Enum.BagIndex|nocaption=1}}
:;slotIndex:{{apitype|number}}
:;unitToken:{{apitype|UnitToken?}}
:;bankType:{{apitype|Enum.BankType?}}
{{:Enum.BankType|nocaption=1}}
:;reagentBankOpen:{{apitype|boolean?|default=false}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>bankType</code> return value.}}
```