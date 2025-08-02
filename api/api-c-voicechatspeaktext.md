# API C VoiceChat.SpeakText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_VoiceChat|system=VoiceChat}}
Reads text to speech.
 C_VoiceChat.SpeakText(voiceID, text, destination, rate, volume)

==Arguments==
:;voiceID:{{apitype|number}} - Voice IDs from {{api|C_VoiceChat.GetTtsVoices|.GetTtsVoices}} or {{api|C_VoiceChat.GetRemoteTtsVoices|.GetRemoteTtsVoices}}.
:;text:{{apitype|string}} - The message to speak.
:;destination:{{apitype|Enum.VoiceTtsDestination}}
{{:Enum.VoiceTtsDestination|nocaption=1}}
:;rate:{{apitype|number}} - Speech rate; the speed at which the text is read.
:;volume:{{apitype|number}} : <code>[0-100]</code>

==Details==
* Despite the name, nearly-simultaneous queued messages will play out of order; the 'queue' is neither FIFO or LIFO.
* The languages packs installed will vary, and it is possible for none to be installed.  The user's local preferences may be found with {{api|C_TTSSettings.GetVoiceOptionID}}.

==Example==
Speaks a message with Microsoft David (enUS system locale).
<syntaxhighlight lang="lua">
/run C_VoiceChat.SpeakText(0, "Hello world", Enum.VoiceTtsDestination.LocalPlayback, 0, 100)
</syntaxhighlight>

Speaks a message with Microsoft Zira (enUS system locale), with a slower speech rate.
<syntaxhighlight lang="lua">
/run C_VoiceChat.SpeakText(1, "Hello world", Enum.VoiceTtsDestination.LocalPlayback, -10, 100)
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.0|note=Added.}}

{{apinavbox|C_VoiceChat_TextToSpeech}}
```