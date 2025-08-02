# API seterrorhandler

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the error handler to the given function.
 seterrorhandler(errFunc)

==Arguments==
:;errFunc:{{apitype|function}} - The function to call when an error occurs. The function is passed a single argument containing the error message.

==Example==
If you wanted to print all errors to your chat frame, you could do:
 seterrorhandler(print);
Alternatively, the following would also perform the same task:
 seterrorhandler(function(msg)
  print(msg);
 end);
```