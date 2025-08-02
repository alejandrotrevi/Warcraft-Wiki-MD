# API GetQuestTimers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all of the quest timers currently in progress.
 questTimers = GetQuestTimers()

==Parameters==
===Arguments===

:''none''

===Returns===

:;questTimers:Strings : Values in seconds of all quest timers currently in progress

==Example==
 QuestTimerFrame_Update(GetQuestTimers());

 function QuestTimerFrame_Update(...)
  for i=1, arg.n, 1 do
   SecondsToTime(arg[i]);
  end
 end

===Result===
 "300", "240", "100"
```