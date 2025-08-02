# API C CurrencyInfo.GetFactionGrantedByCurrency

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the faction ID for currency that is immediately converted into reputation with that faction instead.
 factionID = C_CurrencyInfo.GetFactionGrantedByCurrency(currencyID)

==Arguments==
:;[[CurrencyID|currencyID]]:{{apitype|number}}

==Returns==
:;[[FactionID|factionID]]:{{apitype|number?}}

==Values==
{{i-note|This list is up to date as of patch 9.0.1}}
{| class="sortable darktable zebra"
! CurrencyID !! FactionID !! Name
|-
| 1579 || 2164 || [[:Champions of Azeroth]]
|-
| 1592 || 2161 || [[:Order of Embers]]
|-
| 1593 || 2160 || [[:Proudmoore Admiralty]]
|-
| 1594 || 2162 || [[:Storm's Wake]]
|-
| 1595 || 2156 || [[:Talanji's Expedition]]
|-
| 1596 || 2158 || [[:Voldunai]]
|-
| 1597 || 2103 || [[:Zandalari Empire]]
|-
| 1598 || 2163 || [[:Tortollan Seekers]]
|-
| 1599 || 2159 || [[:7th Legion]]
|-
| 1600 || 2157 || [[:Honorbound]]
|-
| 1738 || 2373 || [[:Unshackled]]
|-
| 1739 || 2400 || [[:Ankoan]]
|-
| 1740 || 2391 || [[:Rustbolt Resistance (Hidden)]]
|-
| 1742 || 2391 || [[:Rustbolt Resistance]]
|-
| 1745 || 2389 || [[:Nazjatar Ally - Neri Sharpfin]]
|-
| 1746 || 2390 || [[:Nazjatar Ally - Vim Brineheart]]
|-
| 1747 || 2388 || [[:Nazjatar Ally - Poen Gillbrack]]
|-
| 1748 || 2377 || [[:Nazjatar Ally - Bladesman Inowari]]
|-
| 1749 || 2375 || [[:Nazjatar Ally - Hunter Akana]]
|-
| 1750 || 2376 || [[:Nazjatar Ally - Farseer Ori]]
|-
| 1752 || 2395 || [[:Honeyback Hive]]
|-
| 1757 || 2417 || [[:Uldum Accord]]
|-
| 1758 || 2415 || [[:Rajani]]
|-
| 1804 || 2407 || [[:Ascended]]
|-
| 1805 || 2410 || [[:Undying Army]]
|-
| 1806 || 2422 || [[:Wild Hunt]]
|-
| 1807 || 2413 || [[:Court of Harvesters]]
|-
| 1837 || 2445 || [[:The Ember Court]]
|-
| 1838 || 2449 || [[:The Countess]]
|-
| 1839 || 2453 || [[:Rendle and Cudgelface]]
|-
| 1840 || 2460 || [[:Stonehead]]
|-
| 1841 || 2455 || [[:Cryptkeeper Kassir]]
|-
| 1842 || 2446 || [[:Baroness Vashj]]
|-
| 1843 || 2461 || [[:Plague Deviser Marileth]]
|-
| 1844 || 2457 || [[:Grandmaster Vole]]
|-
| 1845 || 2450 || [[:Alexandros Mograine]]
|-
| 1846 || 2459 || [[:Sika]]
|-
| 1847 || 2458 || [[:Kleia and Pelegos]]
|-
| 1848 || 2452 || [[:Polemarch Adrestes]]
|-
| 1849 || 2448 || [[:Mikanikos]]
|-
| 1850 || 2454 || [[:Choofa]]
|-
| 1851 || 2456 || [[:Droman Aliothe]]
|-
| 1852 || 2451 || [[:Hunt-Captain Korayn]]
|-
| 1853 || 2447 || [[:Lady Moonberry]]
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```