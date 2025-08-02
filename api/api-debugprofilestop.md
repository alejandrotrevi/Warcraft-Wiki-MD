# API debugprofilestop

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time in milliseconds since the last debugprofilestart call.
 elapsedMilliseconds = debugprofilestop()

==Returns==
:;elapsedMilliseconds:{{apitype|number}} - Time since profiling was started in milliseconds.

==Details==
* Debug profiling provides a high-precision timer that can be used to profile code.
* Calling this function, despite its name, does NOT stop the timer. It simply returns the time since the previous debugprofilestart() call!
* Note that if you are simply using this to profile your own code, it is preferable to NOT keep re-starting the timer since it will interfere with other addons doing the same. Instead, do this:
  local beginTime = debugprofilestop()
  -- do lots of stuff
  -- that takes lots of time
  
  local timeUsed = debugprofilestop()  -beginTime
  print("I used "..timeUsed.." milliseconds!")

==See also==
* {{api|debugprofilestart}}
```