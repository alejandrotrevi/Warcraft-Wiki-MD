# API LaunchURL

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Launches an external web browser and navigates to the URL provided.
 LaunchURL(url)

==Arguments==
:;url:{{apitype|string}} - URL of the website to open. Seems to only accept some URLs, works with base URL of the world of warcraft websites (wow-europe.com, worldofwarcraft.com, etc).

==Example==
 <nowiki>LaunchURL("http://www.worldofwarcraft.com")</nowiki>

==Patch changes==
* {{Patch 10.2.0|note=Re-added.}}
* {{Patch 1.10.0|note=Removed. This still exists inside the login lua environment, however not in the addon environment.}}
* {{Patch 1.0.0|note=Added.}}
```