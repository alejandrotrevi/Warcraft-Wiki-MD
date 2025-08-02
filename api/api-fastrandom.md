# API fastrandom

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a random number within the specified interval.
 rand = fastrandom([ [low, ] high])

==Arguments==
:;low:{{apitype|number}} - lower integer limit on the returned random value.
:;high:{{apitype|number}} - upper integer limit on the returned random value.

==Returns==
:;rand:{{apitype|number}} - Generated random value. If no arguments were specified, the value is a uniformly-distributed decimal between 0 (inclusive) and 1 (exclusive). Otherwise, returns a uniformly-distributed integer between <code>low</code> (1 if not specified) and <code>high</code>, both bounds inclusive.

==Details==
* This function uses C's <code>rand</code> function as a random number generator, and is not suitable for cryptographically secure use cases.
* Lua's <code>math.randomseed</code> is not available in World of Warcraft; the random number generator is instead seeded by the client at startup.

==See also==
* {{api|random}}

==Patch changes==
* {{Patch 5.4.2|note=Name changed to <code>fastrandom</code>; {{api|random}} and <code>math.random</code> now use a different RNG algorithm.}}
```