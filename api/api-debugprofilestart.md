# API debugprofilestart

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Starts a timer for profiling. The final time can be obtained by calling debugprofilestop.
 debugprofilestart()

==Details==
* Note that the timer does not actually need to be started. This is more of a global "reset" of the timer.
* Since it is global, it is probably best to '''never call this function'''. Rather just call debugprofilestop() 2 times and compare the difference.

==See also==
* {{api|debugprofilestop}}
```