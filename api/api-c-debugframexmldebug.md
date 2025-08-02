# API C Debug.FrameXMLDebug

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Queries or sets the FrameXML debug logging flag.
 result = C_Debug.FrameXMLDebug([newDebugLevel])

==Arguments==
:;newDebugLevel:{{apitype|number?}} - <code>0</code> to disable debug logging, or <code>1</code> to enable it. If not specified, the logging flag will not be modified.

==Returns==
:;result:{{apitype|number}} - The applied logging flag value.

==Details==
* When FrameXML debugging is enabled extensive information about the load process is written to <code>World of Warcraft/.../Logs/FrameXML.log</code> and <code>GlueXML.log</code>. This information includes addon and file load order, as well as the names of all created frames and templates.
<!-- * The default value of '''C_Debug.FrameXMLDebug()''' seems to be <code>0</code>, different from <code>1</code> for '''FrameXML_Debug()'''. -->
```