# API C Traits.GetLoadoutSerializationVersion

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns the version of the Talent Build String format.
 serializationVersion = C_Traits.GetLoadoutSerializationVersion()

==Returns==
:;serializationVersion:{{apitype|number}}

==Details==
The Talent Build String is encoded with a header, this header contains the version of the format. If the build string's version doesn't match the return from this API, the game will not attempt to parse the string any further.

Currently this is simply <code>1</code>, it is assumed that blizzard will increase the version number to 2, if they make any changes to the format of their Talent Build Strings.

{{apinavbox|C_Traits}}
```