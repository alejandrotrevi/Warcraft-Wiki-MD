# API GetBuildInfo

**Contributor:** Zeal

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the current client build.
 buildVersion, buildNumber, buildDate, interfaceVersion, localizedVersion, buildInfo = GetBuildInfo()  -- Mainline
 buildVersion, buildNumber, buildDate, interfaceVersion, localizedVersion, buildInfo, currentVersion = GetBuildInfo()  -- Classic

==Returns==
:;buildVersion:{{apitype|string}} - Current patch version
:;buildNumber:{{apitype|string}} - Build number
:;buildDate:{{apitype|string}} - Build date
:;interfaceVersion:{{apitype|number}} - [[Getting the current interface number|Interface (.toc) version number]]
:;localizedVersion:{{apitype|string}} - Localized description of the build version
:;buildInfo:{{apitype|string}} - Localized build type and machine architecture
:;{{Wow-inline}} currentVersion:{{apitype|string}} - Current patch version, but formatted similarly to interface version numbers (eg. "11505")

==Details==
* The <code>localizedVersion</code> and <code>buildInfo</code> return values are currently just an empty string and a string with just a space character respectively.

==Example==
<syntaxhighlight lang="lua">
/dump GetBuildInfo() -- "9.0.2", "36665", "Nov 17 2020", 90002
</syntaxhighlight>

==Latest Builds==
<onlyinclude>{| class="darktable zebra col1-left col3-left" style="text-align:center;"
! Client !! colspan=2 | Expansion !! Version !! Number !! Date !! Interface
|-
| Mainline Test || {{#listsort:|list={{LatestPatchInfo|test}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Mainline || {{#listsort:|list={{LatestPatchInfo}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Classic Beta || {{#listsort:|list={{LatestPatchInfo|classic-beta}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Classic Test || {{#listsort:|list={{LatestPatchInfo|classic-test}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Classic || {{#listsort:|list={{LatestPatchInfo|classic}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Classic (China) || {{#listsort:|list={{LatestPatchInfo|classic-china}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| TBC || {{#listsort:|list={{LatestPatchInfo|tbc}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Vanilla Test || {{#listsort:|list={{LatestPatchInfo|vanilla-test}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|-
| Vanilla || {{#listsort:|list={{LatestPatchInfo|vanilla}}|insep=\!\!|outsep=\!\!|token=@value@|indextoken=@index@|pattern=<esc>{{#switch:@index@|4=6|5=4|6=5|@index@}}</esc>|sortoptions=numeric}}
|}</onlyinclude>

==Patch changes==
* {{Patch 10.1.0|note=Added <code>localizedVersion</code> and <code>buildInfo</code> return values.}}
* {{Patch 1.10.0|note=Added. Prior to this patch this function was only ever exposed to the glue environment.}}
<!-- {{Patch 1.3.0|note=Removed {{api|GetBuildVersion}}()}}
* {{Patch 1.0.0|note=Added <code>GetBuildInfo()</code> as a glue function.}}
-->

==See also==
* [[Public client builds]] - List of documented builds
* https://wow.tools/builds/ - List of datamined builds
* https://www.townlong-yak.com/framexml/builds - List of FrameXML builds and TOC numbers

{{apinavbox|Authoring}}

==References==
```