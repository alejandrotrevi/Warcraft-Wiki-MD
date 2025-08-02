# API RandomRoll

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Performs a random roll between two values.
 RandomRoll([low, [high]])

==Parameters==
<big>'''Arguments'''</big>
:;low:{{apitype|number}} - lowest number (default 1)
:;high:{{apitype|number}} - highest number (default 100)

==Example==
  RandomRoll(1, 10)

'''Yield:''' ''<Your name>'' rolls. ''<number>'' (1-10)

==Details==
:*If only ''low'' is provided, it is taken as the highest number
:*Does the same as '''[[MACRO random|/random low high]]'''
```