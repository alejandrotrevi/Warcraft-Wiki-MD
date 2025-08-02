# API SendMail

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|noscript}}
Sends in-game mail.
 SendMail(recipient, subject [, body])

==Arguments==
:;recipient:{{apitype|string}} - Intended recipient of the mail.
:;subject:{{apitype|string}} - Subject of the mail. Cannot be an empty string or <code>nil</code>, but may be whitespace, e.g. <code>" "</code>
:;body:{{apitype|string?}} - Body of the mail.

==Details==
* Triggers {{api|t=e|MAIL_SEND_SUCCESS}} if mail was sent to the recipient's inbox, or {{api|t=e|MAIL_FAILED}} otherwise. Repeated calls to SendMail() are ignored until one of these events fire.

==Example==
Assuming a friendly player named Bob exists on your server:
<syntaxhighlight lang="lua">
SendMail("Bob", "Hey Bob", "Hows it going, Bob?")
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
```