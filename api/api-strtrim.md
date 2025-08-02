# API strtrim

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Trim characters (''chars''), off the left and right of ''str''
 local newstr = strtrim(str[, chars])

==Arguments==
:(str[, chars])

:;str:{{apitype|string}} - The input string.
:;chars:{{apitype|string}} - A list of characters to remove from the left and right of ''str''.
::: If left off, it defaults to " \t\r\n" (<nowiki>[space][tab][return][newline]</nowiki>).
::: If adding this argument, please note that spaces will not be trimmed unless you include one with the other characters ("123" is not the same as " 123").

==Returns==
:;newstr:{{apitype|string}} - The modified string.


==Example==
 str = "///All debug and no play, make Eric go crazy.\n\n"
 a = strtrim(str, "/\n");
 DEFAULT_CHAT_FRAME:AddMessage(a);

<big>'''Result'''</big>
 All debug and no play, make Eric go crazy.
```