# API IsVoiceChatAllowed

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

isallowed = IsVoiceChatAllowed();

----
;''Arguments''

:''none''

----
;''Returns''

:;isallowed:{{apitype|boolean}} - 1 (true) if Voice Chat is enabled on the server, nil (false) otherwise.

----
;''Example''
  isallowed = IsVoiceChatAllowed();
  if (isallowed) then
     message("Voice Chat is enabled on the server.");
   end
  else
     message("Voice Chat isn't enabled on the server.");
  end
```