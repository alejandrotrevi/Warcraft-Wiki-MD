# API C ClassTalents.HasUnspentTalentPoints

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Returns whether the player has any unspent talent points in their class or spec talent trees.
 hasUnspentPoints, numClassPoints, numSpecPoints = C_ClassTalents.HasUnspentTalentPoints()

==Returns==
:;hasUnspentPoints:{{apitype|boolean}}
:;numClassPoints:{{apitype|number}}
:;numSpecPoints:{{apitype|number}}

==Details==
* If <code>hasUnspentPoints</code> is true, the number of unspent points for at least one of the trees will be greater than zero.
* Hero talent points are not included by this function.

{{apinavbox|C_Traits}}
```