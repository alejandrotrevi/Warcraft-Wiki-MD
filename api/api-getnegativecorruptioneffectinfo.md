# API GetNegativeCorruptionEffectInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Produces a table describing all the harmful consequences of wearing [[Corrupted item|corrupted gear]] without resistance.
 corruptionEffects = GetNegativeCorruptionEffectInfo()

==Returns==
:;corruptionEffects:{{apitype|CorruptionEffectInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| minCorruption || {{apitype|number}} || 
|}

==Example==
 /dump GetNegativeCorruptionEffectInfo()
{{example/Begin}}
 Dump: value=GetNegativeCorruptionEffectInfo
 <span style="color:lightblue">[1]</span>={
   <span style="color:lightblue">[1]</span>={
     <span style="color:lightblue">minCorruption</span>=1,
     <span style="color:lightblue">name</span>="Grasping Tendrils",
     <span style="color:lightblue">description</span>="Taking damage has a chance to reduce your movement speed for 5 sec. The magnitute of the snare increases with further Corruption."
   }
   <span style="color:lightblue">[2]</span>={
     (and so on)
   }
 }
{{example/End}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}
```