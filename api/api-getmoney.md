# API GetMoney

**Contributor:** Kaydeethree

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the amount of money the player character owns.
 money = GetMoney()

==Returns==
:;money:{{apitype|number}} - The amount of money the player's character has.

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|PLAYER_MONEY}} }}
{{apirow | Available after | {{api|t=e|PLAYER_ENTERING_WORLD}} (on login) }}
|}

==Example==

The players money is stored as a series of numbers in the form 1234567.

Some examples:
{| class="darktable zebra"
|+ Examples
|-
! # || Displayed Money !! Stored As
|-
| 1 || 1 Copper || 1 
|-
| 2 || 1 Silver 2 Copper || 102 
|-
| 3 || 1 Silver 23 Copper || 123 
|-
| 4 || 12 Silver 3 Copper || 1203
|-
| 5 || 12 Silver 34 Copper || 1234
|-
| 6 || 1 Gold 2 Silver 3 Copper || 10203
|-
| 7 || 12 Gold 34 Silver 56 Copper || 123456
|-
| 8 || 298 Gold 72 Silver 6 Copper || 2987206
|}


<onlyinclude>* <code>{{api|GetMoney}}()</code>
<syntaxhighlight lang="lua">
local money = GetMoney()
local gold = floor(money / 1e4)
local silver = floor(money / 100 % 100)
local copper = money % 100
print(("You have %dg %ds %dc"):format(gold, silver, copper))
-- You have 10851g 62s 40c
</syntaxhighlight>


* <code>{{api|GetCoinText}}(amount [, separator])</code>
<syntaxhighlight lang="lua">
print(GetCoinText(GetMoney()))    -- "10851 Gold, 62 Silver, 40 Copper"
print(GetCoinText(12345678, " ")) -- "1234 Gold 23 Silver 45 Copper"
print(GetCoinText(12345678, "X")) -- "1234 GoldX23 SilverX45 Copper"
</syntaxhighlight>


* <code>[https://www.townlong-yak.com/framexml/go/GetMoneyString GetMoneyString](amount [, separateThousands])</code>
<syntaxhighlight lang="lua">
print(GetMoneyString(12345678))
print(GetMoneyString(12345678, true))
</syntaxhighlight>
 {{cost|1234|56|78}}
 {{cost|1,234|56|78}}


* <code>{{api|GetCoinTextureString}}(amount [, fontHeight])</code>
<syntaxhighlight lang="lua">
print(GetCoinTextureString(1234578))
print(GetCoinTextureString(1234578, 24))
</syntaxhighlight>
 {{cost|1234|56|78}}
 1234[[File:Gold.png|24px|link=]] 56[[File:Silver.png|24px|link=]] 78[[File:Copper.png|24px|link=]] 
</onlyinclude>
```