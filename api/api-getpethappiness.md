# API GetPetHappiness

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the pet's happiness, damage percentage, and loyalty gain rate.
 happiness, damagePercentage, loyaltyRate = GetPetHappiness()

==Returns==
:;happiness:{{apitype|number}} - the numerical happiness value of the pet (1 = unhappy, 2 = content, 3 = happy)
:;damagePercentage:{{apitype|number}} - damage modifier, happiness affects this (unhappy = 75%, content = 100%, happy = 125%) 
:;loyaltyRate:{{apitype|number}} - the rate at which your pet is currently gaining loyalty (< 0, losing loyalty, > 0, gaining loyalty)

==Example==
 local happiness, damagePercentage, loyaltyRate = GetPetHappiness()
 if not happiness then
 	print("No Pet")
 else
 	local happy = ({"Unhappy", "Content", "Happy"})[happiness]
 	local loyalty = loyaltyRate > 0 and "gaining" or "losing"
 	print("Pet is "..happy)
 	print("Pet is doing "..damagePercentage.."% damage")
 	print("Pet is "..loyalty.." loyalty")
 end

==Patch changes==
* {{Patch 4.1.0|note=Removed.}}
```