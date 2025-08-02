# API TakeInboxMoney

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Take the attached money from the mailbox message at index.
 TakeInboxMoney(index)

==Arguments==
:;index:{{apitype|number}} - a number representing a message in the inbox

==Example==
 for i=GetInboxNumItems(), 1, -1 do 
   TakeInboxMoney(i); -- BUG IN CHINA GAME. if number > 1, takeInboxMoney(N) = InboxMoney(1);
 end;
```