# API DoEmote

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Performs an emote.
 restricted = DoEmote(token [, unit, hold])

==Arguments==
:;token:{{apitype|string}} : [[#Emotes|EmoteToken]] - The emote to perform.
:;unit:{{apitype|UnitToken?}} : - Who the emote will be performed on. Defaults to the current target.
:;hold:{{apitype|boolean?}} - Supposedly holds the emote animation until canceled, like for the /read emote.

==Returns==
:;restricted:{{apitype|boolean}} - If an emote is restricted this tells the UI to show it as an unrecognized chat command.<sup>[https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/FrameXML/ChatFrame.lua#L5192]</sup> For example <code>DoEmote("FORTHEHORDE")</code> while being alliance.

==Details==
*  The list of emotes is in [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/FrameXML/ChatFrame.lua#L424 ChatFrame.lua] and [https://www.townlong-yak.com/framexml/9.2.0/GlobalStrings.lua#5188 GlobalStrings.lua]
* Does not require a hardware event. There is a ~0.25 second server-side throttle on performing an emote, since somewhere in 2011 when it was abused.
* Quirk: UnitIDs like "target" do not appear to work on NPCs, but it works while omitting the param.

==Example==
Similar to <code>/hello</code>, if you are targeting something <font color="#dda0dd">''"You greet %s with a hearty hello!"''</font>, otherwise <font color="#dda0dd">''"You greet everyone with a hearty hello!"''</font>
<syntaxhighlight lang="lua">
DoEmote("HELLO")
</syntaxhighlight>
To ensure an emote is not aimed at a target.
<syntaxhighlight lang="lua">
DoEmote("HELLO", "none")
</syntaxhighlight>

==Emotes==
[[List of emotes|List of emote]] tokens in {{dbc|EmotesText}} and {{dbc|EmotesTextData}}
<!-- https://github.com/Ketho/WowpediaDoc/blob/master/Pages/API_DoEmote.lua -->

{{i-note|This list is up to date as of PTR Patch 10.1.7 (50587) Jul 23 2023}}
{| class="sortable darktable zebra col3-center col4-center"
! Token !! Slash Command !! Anim !! Voice !! No Target Text !! Targeted Text !! Patch
|-
| AGREE || /agree ||  ||  || You agree. || You agree with %s. || 
|-
| AMAZE || /amaze ||  ||  || You are amazed! || You are amazed by %s! || 
|-
| ANGRY || /angry /mad || <span title="ID 73">✔️</span> ||  || You raise your fist in anger. || You raise your fist in anger at %s. || 
|-
| APOLOGIZE || /apologize /sorry ||  || ✔️ || You apologize to everyone. Sorry! || You apologize to %s. Sorry! || 
|-
| APPLAUD || /applaud /bravo /applause || <span title="ID 80">✔️</span> || ✔️ || You applaud. Bravo! || You applaud at %s. Bravo! || 
|-
| BASHFUL || /bashful || <span title="ID 83">✔️</span> ||  || You are bashful. || You are so bashful...too bashful to get %s's attention. || 
|-
| BECKON || /beckon ||  ||  || You beckon everyone over to you. || You beckon %s over. || 
|-
| BEG || /beg || <span title="ID 79">✔️</span> || ✔️ || You beg everyone around you. How pathetic. || You beg %s. How pathetic. || 
|-
| BITE || /bite ||  ||  || You look around for someone to bite. || You bite %s. Ouch! || 
|-
| BLEED || /bleed /blood ||  ||  || Blood oozes from your wounds. ||  || 
|-
| BLINK || /blink ||  ||  || You blink your eyes. || You blink at %s. || 
|-
| BLUSH || /blush || <span title="ID 83">✔️</span> ||  || You blush. || You blush at %s. || 
|-
| BONK || /bonk /doh ||  ||  || You bonk yourself on the noggin. Doh! || You bonk %s on the noggin. Doh! || 
|-
| BORED || /bored ||  || ✔️ || You are overcome with boredom.  Oh the drudgery! || You are terribly bored with %s. || 
|-
| BOUNCE || /bounce ||  ||  || You bounce up and down. || You bounce up and down in front of %s. || 
|-
| BRB || /brb ||  ||  || You let everyone know you'll be right back. || You let %s know you'll be right back. || 
|-
| BOW || /bow || <span title="ID 66">✔️</span> ||  || You bow down graciously. || You bow before %s. || 
|-
| BURP || /burp /belch ||  ||  || You let out a loud belch. || You let out a loud belch. || 
|-
| BYE || /bye /goodbye /farewell || <span title="ID 67">✔️</span> || ✔️ || You wave goodbye to everyone. Farewell! || You wave goodbye to %s. Farewell! || 
|-
| CACKLE || /cackle || <span title="ID 70">✔️</span> || ✔️ || You cackle maniacally at the situation. || You cackle maniacally at %s. || 
|-
| CHEER || /cheer /woot || <span title="ID 68">✔️</span> || ✔️ || You cheer! || You cheer at %s. || 
|-
| CHICKEN || /chicken /flap /strut || <span title="ID 78">✔️</span> || ✔️ || With arms flapping, you strut around. Cluck, Cluck, Chicken! || With arms flapping, you strut around %s. Cluck, Cluck, Chicken! || 
|-
| CHUCKLE || /chuckle || <span title="ID 70">✔️</span> || ✔️ || You let out a hearty chuckle. || You chuckle at %s. || 
|-
| CLAP || /clap || <span title="ID 80">✔️</span> ||  || You clap excitedly. || You clap excitedly for %s. || 
|-
| CONFUSED || /confused || <span title="ID 65">✔️</span> ||  || You are hopelessly confused. || You look at %s with a confused look. || 
|-
| CONGRATULATE || <small>/congratulate /congrats /cong /grats</small> || <span title="ID 68">✔️</span> || ✔️ || You congratulate everyone around you. || You congratulate %s. || 
|-
| COUGH || /cough ||  ||  || You let out a hacking cough. || You let out a hacking cough. || 
|-
| COWER || /cower /fear || <span title="ID 225">✔️</span> ||  || You cower in fear. || You cower in fear at the sight of %s. || 
|-
| CRACK || /crack /knuckles ||  ||  || You crack your knuckles. || You crack your knuckles while staring at %s. || 
|-
| CRINGE || /cringe ||  ||  || You cringe in fear. || You cringe away from %s. || 
|-
| CRY || /cry /sob /weep || <span title="ID 77">✔️</span> || ✔️ || You cry. || You cry on %s's shoulder. || 
|-
| CURIOUS || /curious || <span title="ID 65">✔️</span> ||  || You express your curiosity to those around you. || You are curious what %s is up to. || 
|-
| CURTSEY || /curtsey || <span title="ID 66">✔️</span> ||  || You curtsey. || You curtsey before %s. || 
|-
| DANCE || /dance || <span title="ID 69">✔️</span> ||  || You burst into dance. || You dance with %s. || 
|-
| DRINK || /drink /shindig || <span title="ID 61">✔️</span> || ✔️ || You raise a drink in the air before chugging it down. Cheers! || You raise a drink to %s. Cheers! || 
|-
| DROOL || /drool ||  ||  || A tendril of drool runs down your lip. || A tendril of drool runs down your lip. || 
|-
| EAT || /eat /chew /feast || <span title="ID 61">✔️</span> || ✔️ || You begin to eat. || You begin to eat in front of %s. || 
|-
| EYE || /eye ||  ||  || You cross your eyes. || You eye %s up and down. || 
|-
| FART || /fart ||  ||  || You fart loudly.  Whew...what stinks? || You fart loudly.  Whew...what stinks? || 
|-
| FIDGET || /fidget /impatient ||  ||  || You fidget. || You fidget impatiently while waiting for %s. || 
|-
| FLEX || /flex /strong || <span title="ID 82">✔️</span> ||  || You flex your muscles. Oooooh so strong! || You flex at %s. Oooooh so strong! || 
|-
| FROWN || <small>/frown /disappointed /disappointment</small> ||  ||  || You frown. || You frown with disappointment at %s. || 
|-
| GASP || /gasp || <span title="ID 64">✔️</span> ||  || You gasp. || You gasp at %s. || 
|-
| GAZE || /gaze ||  ||  || You gaze off into the distance. || You gaze longingly at %s. || 
|-
| GIGGLE || /giggle || <span title="ID 70">✔️</span> || ✔️ || You giggle. || You giggle at %s. || 
|-
| GLARE || /glare ||  ||  || You glare angrily. || You glare angrily at %s. || 
|-
| GLOAT || /gloat || <span title="ID 70">✔️</span> || ✔️ || You gloat over everyone's misfortune. || You gloat over %s's misfortune. || 
|-
| GREET || /greet /greetings || <span title="ID 67">✔️</span> ||  || You greet everyone warmly. || You greet %s warmly. || 
|-
| GRIN || /grin /wicked /wickedly ||  ||  || You grin wickedly. || You grin wickedly at %s. || 
|-
| GROAN || /groan ||  ||  || You begin to groan in pain. || You look at %s and groan in pain. || 
|-
| GROVEL || /grovel /peon || <span title="ID 79">✔️</span> ||  || You grovel on the ground, wallowing in subservience. || You grovel before %s like a subservient peon. || 
|-
| GUFFAW || /guffaw || <span title="ID 70">✔️</span> || ✔️ || You let out a boisterous guffaw! || You take one look at %s and let out a guffaw! || 
|-
| HAIL || /hail || <span title="ID 67">✔️</span> ||  || You hail those around you. || You hail %s. || 
|-
| HAPPY || /happy /glad /yay ||  ||  || You are filled with happiness! || You are very happy with %s! || 
|-
| HELLO || /hello /hi || <span title="ID 67">✔️</span> || ✔️ || You greet everyone with a hearty hello! || You greet %s with a hearty hello! || 
|-
| HUG || /hug ||  ||  || You need a hug! || You hug %s. || 
|-
| HUNGRY || /hungry /food /pizza ||  ||  || You are hungry! || You are hungry. Maybe %s has some food... || 
|-
| KISS || /kiss /blow || <span title="ID 76">✔️</span> || ✔️ || You blow a kiss into the wind. || You blow a kiss to %s. || 
|-
| KNEEL || /kneel || <span title="ID 0">✔️</span> ||  || You kneel down. || You kneel before %s. || 
|-
| LAUGH || /laugh /lol || <span title="ID 70">✔️</span> || ✔️ || You laugh. || You laugh at %s. || 
|-
| LAYDOWN || /laydown /liedown /lay /lie || <span title="ID 0">✔️</span> ||  || You lie down. || You lie down before %s. || 
|-
| MASSAGE || /massage ||  ||  || You need a massage! || You massage %s's shoulders. || 
|-
| ❌ MOAN || /moan ||  ||  ||  ||  || 
|-
| MOON || /moon ||  ||  || You drop your trousers and moon everyone. || You drop your trousers and moon everyone. || 
|-
| MOURN || /mourn || <span title="ID 77">✔️</span> || ✔️ || In quiet contemplation, you mourn the loss of the dead. || In quiet contemplation, you mourn the death of %s. || 
|-
| NO || /no || <span title="ID 186">✔️</span> || ✔️ || You clearly state, NO. || You tell %s NO. Not going to happen. || 
|-
| NOD || /nod /yes || <span title="ID 185">✔️</span> || ✔️ || You nod. || You nod at %s. || 
|-
| NOSEPICK || /nosepick /pick ||  ||  || With a finger deep in one nostril, you pass the time. || You pick your nose and show it to %s. || 
|-
| PANIC || /panic ||  ||  || You run around in a frenzied state of panic. || You take one look at %s and panic. || 
|-
| PEER || /peer ||  ||  || You peer around, searchingly. || You peer at %s searchingly. || 
|-
| PLEAD || /plead || <span title="ID 79">✔️</span> ||  || You drop to your knees and plead in desperation. || You plead with %s. || 
|-
| POINT || /point || <span title="ID 84">✔️</span> ||  || You point over yonder. || You point at %s. || 
|-
| POKE || /poke ||  ||  || You poke your belly and giggle. || You poke %s. Hey! || 
|-
| PRAY || /pray || <span title="ID 75">✔️</span> ||  || You pray to the Gods. || You say a prayer for %s. || 
|-
| ROAR || /roar /rawr || <span title="ID 74">✔️</span> || ✔️ || You roar with bestial vigor. So fierce! || You roar with bestial vigor at %s. So fierce! || 
|-
| ROFL || /rofl || <span title="ID 70">✔️</span> || ✔️ || You roll on the floor laughing. || You roll on the floor laughing at %s. || 
|-
| RUDE || /rude || <span title="ID 73">✔️</span> || ✔️ || You make a rude gesture. || You make a rude gesture at %s. || 
|-
| SALUTE || /salute || <span title="ID 113">✔️</span> ||  || You stand at attention and salute. || You salute %s with respect. || 
|-
| SCRATCH || /scratch /cat /catty ||  ||  || You scratch yourself. Ah, much better! || You scratch %s. How catty! || 
|-
| SEXY || /sexy ||  ||  || You're too sexy for your tunic...so sexy it hurts. || You think %s is a sexy devil. || 
|-
| ❌ SHAKE || /shake /rear ||  ||  ||  ||  || 
|-
| SHOUT || /shout /holler || <span title="ID 81">✔️</span> ||  || You shout. || You shout at %s. || 
|-
| SHRUG || /shrug || <span title="ID 65">✔️</span> ||  || You shrug. Who knows? || You shrug at %s. Who knows? || 
|-
| SHY || /shy || <span title="ID 83">✔️</span> ||  || You smile shyly. || You smile shyly at %s. || 
|-
| SIGH || /sigh ||  || ✔️ || You let out a long, drawn-out sigh. || You sigh at %s. || 
|-
| SIT || /sit || <span title="ID 0">✔️</span> ||  ||  ||  || 
|-
| SLEEP || /sleep || <span title="ID 0">✔️</span> ||  || You fall asleep.  Zzzzzzz. ||  || 
|-
| SNARL || /snarl ||  ||  || You bare your teeth and snarl. || You bare your teeth and snarl at %s. || 
|-
| SPIT || /spit ||  ||  || You spit on the ground. ||  || 
|-
| STARE || /stare ||  ||  || You stare off into the distance. || You stare %s down. || 
|-
| SURPRISED || /surprised ||  ||  || You are so surprised! || You are surprised by %s's actions. || 
|-
| SURRENDER || /surrender || <span title="ID 79">✔️</span> ||  || You surrender to your opponents. || You surrender before %s. Such is the agony of defeat... || 
|-
| TALK || /talk || <span title="ID 60">✔️</span> ||  || You talk to yourself since no one else seems interested. || You want to talk things over with %s. || 
|-
| TALKEX || /talkex /excited || <span title="ID 64">✔️</span> ||  || You talk excitedly with everyone. || You talk excitedly with %s. || 
|-
| TALKQ || /talkq /question || <span title="ID 65">✔️</span> ||  || You want to know the meaning of life. || You question %s. || 
|-
| TAP || /tap ||  ||  || You tap your foot.  Hurry up already! || You tap your foot as you wait for %s. || 
|-
| THANK || /thank /thanks /ty || <span title="ID 60">✔️</span> || ✔️ || You thank everyone around you. || You thank %s. || 
|-
| THREATEN || <small>/threaten /doom /threat /wrath</small> ||  || ✔️ || You threaten everyone with the wrath of doom. || You threaten %s with the wrath of doom. || 
|-
| TIRED || /tired ||  ||  || You let everyone know that you are tired. || You let %s know that you are tired. || 
|-
| VICTORY || /victory || <span title="ID 68">✔️</span> ||  || You bask in the glory of victory. || You bask in the glory of victory with %s. || 
|-
| WAVE || /wave || <span title="ID 67">✔️</span> ||  || You wave. || You wave at %s. || 
|-
| WELCOME || /welcome || <span title="ID 67">✔️</span> || ✔️ || You welcome everyone. || You welcome %s. || 
|-
| WHINE || /whine ||  ||  || You whine pathetically. || You whine pathetically at %s. || 
|-
| WHISTLE || /whistle ||  || ✔️ || You let forth a sharp whistle. || You let forth a sharp whistle. || 
|-
| WORK || /work ||  ||  || You begin to work. || You work with %s. || 
|-
| YAWN || /yawn ||  || ✔️ || You yawn sleepily. || You yawn sleepily at %s. || 
|-
| BOGGLE || /boggle || <span title="ID 65">✔️</span> ||  || You boggle at the situation. || You boggle at %s. || 
|-
| CALM || /calm ||  ||  || You remain calm. || You try to calm %s down. || 
|-
| COLD || /cold ||  ||  || You let everyone know that you are cold. || You let %s know that you are cold. || 
|-
| COMFORT || /comfort ||  ||  || You need to be comforted. || You comfort %s. || 
|-
| CUDDLE || /cuddle /spoon ||  ||  || You need to be cuddled. || You cuddle up against %s. || 
|-
| DUCK || /duck ||  ||  || You duck for cover. || You duck behind %s. || 
|-
| INSULT || /insult || <span title="ID 73">✔️</span> ||  || You think everyone around you is a son of a motherless ogre. || You think %s is the son of a motherless ogre. || 
|-
| INTRODUCE || /introduce ||  ||  || You introduce yourself to everyone. || You introduce yourself to %s. || 
|-
| JK || /jk ||  ||  || You were just kidding! || You let %s know that you were just kidding! || 
|-
| LICK || /lick ||  ||  || You lick your lips. || You lick %s. || 
|-
| LISTEN || /listen ||  ||  || You are listening! || You listen intently to %s. || 
|-
| LOST || /lost || <span title="ID 65">✔️</span> ||  || You are hopelessly lost. || You want %s to know that you are hopelessly lost. || 
|-
| MOCK || /mock ||  ||  || You mock life and all it stands for. || You mock the foolishness of %s. || 
|-
| PONDER || /ponder || <span title="ID 65">✔️</span> ||  || You ponder the situation. || You ponder %s's actions. || 
|-
| POUNCE || /pounce ||  ||  || You pounce out from the shadows. || You pounce towards %s. || 
|-
| PRAISE || /praise /lavish ||  ||  || You praise the Light. || You lavish praise upon %s. || 
|-
| PURR || /purr ||  ||  || You purr like a kitten. || You purr at %s. || 
|-
| PUZZLE || /puzzled || <span title="ID 65">✔️</span> ||  || You are puzzled. What's going on here? || You are puzzled by %s. || 
|-
| RAISE || /raise /volunteer ||  ||  || You raise your hand in the air. || You look at %s and raise your hand. || 
|-
| READY || /ready /rdy ||  ||  || You let everyone know that you are ready! || You let %s know that you are ready! || 
|-
| SHIMMY || /shimmy ||  ||  || You shimmy before the masses. || You shimmy before %s. || 
|-
| SHIVER || /shiver ||  ||  || You shiver in your boots. Chilling! || You shiver beside %s. Chilling! || 
|-
| SHOO || /shoo /pest ||  ||  || You shoo the measly pests away. || You shoo %s away. Be gone pest! || 
|-
| SLAP || /slap ||  ||  || You slap yourself across the face. Ouch! || You slap %s across the face. Ouch! || 
|-
| SMIRK || /smirk ||  ||  || A sly smirk spreads across your face. || You smirk slyly at %s. || 
|-
| SNIFF || /sniff || <span title="ID 506">✔️</span> ||  || You sniff the air around you. || You sniff %s. || 
|-
| SNUB || /snub ||  ||  || You snub all of the lowly peons around you. || You snub %s. || 
|-
| SOOTHE || /soothe ||  ||  || You need to be soothed. || You soothe %s. There, there...things will be ok. || 
|-
| ❌ STINK || /stink /smell ||  ||  ||  ||  || 
|-
| TAUNT || /taunt || <span title="ID 78">✔️</span> || ✔️ || You taunt everyone around you. Bring it fools! || You make a taunting gesture at %s. Bring it! || 
|-
| TEASE || /tease ||  ||  || You are such a tease. || You tease %s. || 
|-
| THIRSTY || /thirsty ||  ||  || You are so thirsty. Can anyone spare a drink? || You let %s know you are thirsty. Spare a drink? || 
|-
| VETO || /veto ||  ||  || You veto the motion on the floor. || You veto %s's motion. || 
|-
| SNICKER || /snicker ||  ||  || You quietly snicker to yourself. || You snicker at %s. || 
|-
| STAND || /stand || <span title="ID 0">✔️</span> ||  ||  ||  || 
|-
| TICKLE || /tickle ||  ||  || You want to be tickled. Hee hee! || You tickle %s. Hee hee! || 
|-
| VIOLIN || /violin || <span title="ID 77">✔️</span> || ✔️ || You begin to play the world's smallest violin. || You play the world's smallest violin for %s. || 
|-
| SMILE || /smile ||  ||  || You smile. || You smile at %s. || 
|-
| RASP || /rasp || <span title="ID 73">✔️</span> || ✔️ || You make a rude gesture. || You make a rude gesture at %s. || 0.5.5
|-
| PITY || /pity ||  ||  || You pity those around you. || You look down upon %s with pity. || 0.5.5
|-
| GROWL || /growl || <span title="ID 74">✔️</span> ||  || You growl menacingly. || You growl menacingly at %s. || 0.5.5
|-
| BARK || /bark ||  ||  || You bark. Woof woof! || You bark at %s. || 0.5.5
|-
| SCARED || /scared || <span title="ID 225">✔️</span> ||  || You are scared! || You are scared of %s. || 0.5.5
|-
| FLOP || /flop ||  ||  || You flop about helplessly. || You flop about helplessly around %s. || 0.5.5
|-
| LOVE || /love ||  ||  || You feel the love. || You love %s. || 0.5.5
|-
| MOO || /moo ||  || ✔️ || Mooooooooooo. || You moo at %s. Mooooooooooo. || 0.5.5
|-
| COMMEND || /commend || <span title="ID 80">✔️</span> ||  || You commend everyone on a job well done. || You commend %s on a job well done. || 0.7.0
|-
| TRAIN || /train || <span title="ID 195">✔️</span> || ✔️ ||  ||  || 1.0.0
|-
| HELPME || /helpme || <span title="ID 81">✔️</span> || ✔️ || You cry out for help! ||  || 1.1.2
|-
| INCOMING || /incoming /inc || <span title="ID 84">✔️</span> || ✔️ || You warn everyone of incoming enemies! || You point out %s as an incoming enemy! || 1.1.2
|-
| CHARGE || /charge || <span title="ID 84">✔️</span> || ✔️ || You start to charge. ||  || 1.1.2
|-
| FLEE || /retreat /flee || <span title="ID 81">✔️</span> || ✔️ || You yell for everyone to flee! || You yell for %s to flee! || 1.1.2
|-
| ATTACKMYTARGET || /attacktarget || <span title="ID 74">✔️</span> || ✔️ || You tell everyone to attack something. || You tell everyone to attack %s. || 1.1.2
|-
| OOM || /oom || <span title="ID 60">✔️</span> || ✔️ || You announce that you have low mana! ||  || 1.1.2
|-
| FOLLOW || /followme || <span title="ID 60">✔️</span> || ✔️ || You motion for everyone to follow. || You motion for %s to follow. || 1.1.2
|-
| WAIT || /wait || <span title="ID 60">✔️</span> || ✔️ || You ask everyone to wait. || You ask %s to wait. || 1.1.2
|-
| HEALME || /healme || <span title="ID 60">✔️</span> || ✔️ || You call out for healing! ||  || 1.1.2
|-
| OPENFIRE || /openfire || <span title="ID 84">✔️</span> || ✔️ || You give the order to open fire. ||  || 1.1.2
|-
| FLIRT || /flirt || <span title="ID 83">✔️</span> || ✔️ || You flirt. || You flirt with %s. || 1.1.2
|-
| JOKE || /silly || <span title="ID 60">✔️</span> || ✔️ || You tell a joke. || You tell %s a joke. || 1.1.2
|-
| GOLFCLAP || /golfclap || <span title="ID 80">✔️</span> ||  || You clap half-heartedly, clearly unimpressed. || You clap for %s, clearly unimpressed. || 2.0.0
|-
| WINK || /wink ||  ||  || You wink slyly. || You wink slyly at %s. || 2.0.0
|-
| PAT || /pat ||  ||  || You need a pat. || You gently pat %s. || 2.0.0
|-
| SERIOUS || ❌ ||  ||  || You think this is serious business. || You think %s is serious. || 2.0.0
|-
| MOUNTSPECIAL || /mountspecial || <span title="ID 94">✔️</span> ||  ||  ||  || 2.0.0
|-
| GOODLUCK || ❌ ||  ||  || You wish for some good luck. || You wish %s good luck. || 2.4.3
|-
| BLAME || /blame || <span title="ID 84">✔️</span> ||  || You blame yourself for what happened. || You blame %s for everything. || 2.4.3
|-
| BLANK || /blank ||  ||  || You stare blankly at your surroundings. || You stare blankly at %s. || 2.4.3
|-
| BRANDISH || /brandish ||  ||  || You brandish your weapon fiercely. || You brandish your weapon fiercely at %s. || 2.4.3
|-
| BREATH || /breath ||  ||  || You take a deep breath. || You tell %s to take a deep breath. || 2.4.3
|-
| DISAGREE || /disagree || <span title="ID 186">✔️</span> ||  || You disagree. || You disagree with %s. || 2.4.3
|-
| DOUBT || /doubt || <span title="ID 186">✔️</span> ||  || You doubt the situation will end in your favor. || You doubt %s. || 2.4.3
|-
| EMBARRASS || /embarrass ||  ||  || You flush with embarrassment. || You are embarrassed by %s. || 2.4.3
|-
| ENCOURAGE || /encourage ||  ||  || You encourage everyone around you. || You encourage %s. || 2.4.3
|-
| ENEMY || /enemy ||  ||  || You warn everyone that an enemy is near. || You warn %s that an enemy is near. || 2.4.3
|-
| EYEBROW || /eyebrow /brow ||  ||  || You raise your eyebrow inquisitively. || You raise your eyebrow inquisitively at %s. || 2.4.3
|-
| TOAST || ❌ || <span title="ID 61">✔️</span> ||  || You raise a drink in the air before chugging it down. Cheers! || You raise a drink to %s. Cheers! || 2.4.3
|-
| FAIL || ❌ || <span title="ID 77">✔️</span> ||  || You have failed. || You think %s has failed. || 3.0.1
|-
| HIGHFIVE || /highfive ||  ||  || You put up your hand for a high five. || You give %s a high five! || 3.0.1
|-
| ABSENT || /absent ||  ||  || You look absent-minded. || You look at %s absently. || 3.0.1
|-
| ARM || /arm ||  ||  || You stretch your arms out. || You put your arm around %s's shoulder. || 3.0.1
|-
| AWE || /awe ||  ||  || You look around in awe. || You stare at %s in awe. || 3.0.1
|-
| BACKPACK || /backpack /pack ||  ||  || You dig through your backpack. ||  || 3.0.1
|-
| BADFEELING || /badfeeling /bad ||  ||  || You have a bad feeling about this... || You have a bad feeling about %s. || 3.0.1
|-
| CHALLENGE || /challenge ||  ||  || You put out a challenge to everyone. Bring it on! || You challenge %s to a duel. || 3.0.1
|-
| CHUG || /chug ||  ||  || You take a mighty quaff of your beverage. || You encourage %s to chug. CHUG! CHUG! CHUG! || 3.0.1
|-
| DING || /ding ||  ||  || You reached a new level. DING! || You congratulate %s on a new level. DING! || 3.0.1
|-
| FACEPALM || /facepalm /palm ||  ||  || You cover your face with your palm. || You look at %s and cover your face with your palm. || 3.0.1
|-
| FAINT || /faint ||  ||  || You faint. || You faint at the sight of %s. || 3.0.1
|-
| GO || /go ||  ||  || You tell everyone to go. || You tell %s to go. || 3.0.1
|-
| GOING || /going ||  ||  || You must be going. || You tell %s that you must be going. || 3.0.1
|-
| GLOWER || /glower ||  ||  || You glower at averyone around you. || You glower at %s. || 3.0.1
|-
| HEADACHE || /headache ||  ||  || You are getting a headache. || You are getting a headache from %s's antics. || 3.0.1
|-
| HICCUP || /hiccup ||  ||  || You hiccup loudly. ||  || 3.0.1
|-
| HISS || /hiss ||  ||  || You hiss at everyone around you. || You hiss at %s. || 3.0.1
|-
| HOLDHAND || /holdhand ||  ||  || You wish someone would hold your hand. || You hold %s's hand. || 3.0.1
|-
| HURRY || /hurry ||  ||  || You try to pick up the pace. || You tell %s to hurry up. || 3.0.1
|-
| IDEA || /idea ||  ||  || You have an idea! ||  || 3.0.1
|-
| JEALOUS || /jealous ||  ||  || You are jealous of everyone around you. || You are jealous of %s. || 3.0.1
|-
| LUCK || /luck ||  ||  || You wish everyone good luck. || You wish %s the best of luck. || 3.0.1
|-
| MAP || /map ||  ||  || You pull out your map. ||  || 3.0.1
|-
| MERCY || /mercy || <span title="ID 79">✔️</span> ||  || You plead for mercy. || You plead with %s for mercy. || 3.0.1
|-
| MUTTER || /mutter ||  ||  || You mutter angrily to yourself. Hmmmph! || You mutter angrily at %s. Hmmmph! || 3.0.1
|-
| NERVOUS || /nervous ||  ||  || You look around nervously. || You look at %s nervously. || 3.0.1
|-
| OFFER || /offer ||  ||  || You want to make an offer. || You attempt to make %s an offer they can't refuse. || 3.0.1
|-
| PET || /pet ||  ||  || You need to be petted. || You pet %s. || 3.0.1
|-
| PINCH || /pinch ||  ||  || You pinch yourself. || You pinch %s. || 3.0.1
|-
| PROUD || /proud ||  ||  || You are proud of yourself. || You are proud of %s. || 3.0.1
|-
| PROMISE || /promise ||  ||  ||  || You make %s a promise. || 3.0.1
|-
| PULSE || /pulse ||  ||  || You check your own pulse. || You check %s for a pulse. Oh no! || 3.0.1
|-
| PUNCH || /punch ||  ||  || You punch yourself. || You punch %s's shoulder. || 3.0.1
|-
| POUT || /pout ||  ||  || You pout at everyone around you. || You pout at %s. || 3.0.1
|-
| REGRET || /regret ||  ||  || You are filled with regret. || You think that %s will regret it. || 3.0.1
|-
| REVENGE || /revenge ||  ||  || You vow you will have your revenge. || You vow revenge on %s. || 3.0.1
|-
| ROLLEYES || /rolleyes /eyeroll ||  ||  || You roll your eyes. || You roll your eyes at %s. || 3.0.1
|-
| RUFFLE || /ruffle ||  ||  || You ruffle your hair. || You ruffle %s's hair. || 3.0.1
|-
| SAD || /sad ||  ||  || You hang your head dejectedly. ||  || 3.0.1
|-
| SCOFF || /scoff ||  ||  || You scoff. || You scoff at %s. || 3.0.1
|-
| SCOLD || /scold ||  ||  || You scold yourself. || You scold %s. || 3.0.1
|-
| SCOWL || /scowl ||  ||  || You scowl. || You scowl at %s. || 3.0.1
|-
| SEARCH || /search ||  ||  || You search for something. || You search %s for something. || 3.0.1
|-
| SHAKEFIST || /shakefist /fist ||  ||  || You shake your fist. || You shake your fist at %s. || 3.0.1
|-
| SHIFTY || /shifty ||  ||  || Your eyes shift back and forth suspiciously. || You give %s a shifty look. || 3.0.1
|-
| SHUDDER || /shudder ||  ||  || You shudder. || You shudder at the sight of %s. || 3.0.1
|-
| SIGNAL || /signal ||  ||  || You give the signal. || You give %s the signal. || 3.0.1
|-
| SILENCE || /silence /shush ||  ||  || You tell everyone to be quiet. Shhh! || You tell %s to be quiet. Shhh! || 3.0.1
|-
| SING || /sing || <span title="ID 60">✔️</span> ||  || You burst into song. || You serenade %s with a song. || 3.0.1
|-
| SMACK || /smack ||  ||  || You smack your forehead. || You smack %s upside the head. || 3.0.1
|-
| SNEAK || /sneak ||  ||  || You try to sneak away. || You try to sneak away from %s. || 3.0.1
|-
| SNEEZE || /sneeze ||  ||  || You sneeze. Achoo! || You sneeze on %s. Achoo! || 3.0.1
|-
| SNORT || /snort ||  ||  || You snort. || You snort derisively at %s. || 3.0.1
|-
| SQUEAL || /squeal ||  ||  || You squeal like a pig. || You squeal at %s. || 3.0.1
|-
| STOPATTACK || ❌ ||  ||  || You tell everyone to stop attacking. || You tell %s to stop attacking. || 3.0.1
|-
| SUSPICIOUS || /suspicious ||  ||  || You narrow your eyes in suspicion. || You are suspicious of %s. || 3.0.1
|-
| THINK || /think ||  ||  || You are lost in thought. || You think about %s. || 3.0.1
|-
| TRUCE || /truce ||  ||  || You offer a truce. || You offer %s a truce. || 3.0.1
|-
| TWIDDLE || /twiddle ||  ||  || You twiddle your thumbs. ||  || 3.0.1
|-
| WARN || /warn ||  ||  || You warn everyone. || You warn %s. || 3.0.1
|-
| SNAP || /snap ||  ||  || You snap your fingers. || You snap your fingers at %s. || 3.0.1
|-
| CHARM || /charm ||  ||  || You put on the charm. || You think %s is charming. || 3.0.1
|-
| COVEREARS || /coverears ||  ||  || You cover your ears. || You cover %s's ears. || 3.0.1
|-
| CROSSARMS || /crossarms ||  ||  || You cross your arms. || You cross your arms at %s. Hmph! || 3.0.1
|-
| LOOK || /look ||  ||  || You look around. || You look at %s. || 3.0.1
|-
| OBJECT || /object /objection /holdit || <span title="ID 84">✔️</span> ||  || You OBJECT! || You object to %s. || 3.0.1
|-
| SWEAT || /sweat ||  ||  || You are sweating. || You sweat at the sight of %s. || 3.0.1
|-
| YW || /yw || <span title="ID 60">✔️</span> || ✔️ || You were happy to help. || You were happy to help %s. || 3.3.5
|-
| READ || /read || <span title="ID 520">✔️</span> ||  ||  ||  || 4.x
|-
| BOOT || ❌ || <span title="ID 95">✔️</span> ||  ||  ||  || 6.0.1
|-
| FORTHEALLIANCE || /forthealliance || <span title="ID 68">✔️</span> || ✔️ || You cheer for the Alliance! || You cheer for the Alliance! || 6.x / 7.x
|-
| FORTHEHORDE || /forthehorde || <span title="ID 68">✔️</span> || ✔️ || You cheer for the Horde! || You cheer for the Horde! || 6.x / 7.x
|-
| WHOA || /whoa || <span title="ID 64">✔️</span> || ✔️ || You are blown away. || You are blown away by %s. || 6.x / 7.x
|-
| OOPS || /oops || <span title="ID 65">✔️</span> || ✔️ || You made a mistake. || You made a mistake. || 6.x / 7.x
|-
| ALLIANCE || ❌ || <span title="ID 68">✔️</span> || ✔️ ||  || You cheer for the Alliance! || 6.x / 7.x
|-
| HORDE || ❌ || <span title="ID 68">✔️</span> || ✔️ ||  || You cheer for the Horde! || 6.x / 7.x
|-
| MEOW || /meow ||  ||  || You meow. || You meow at %s. || 8.0.1
|-
| BOOP || /boop || <span title="ID 84">✔️</span> ||  || You boop your own nose. Boop! || You boop %s's nose. || 8.0.1
|-
| WINCE || /wince ||  ||  || You wince sympathetically. || You wince sympathetically at %s. That looked like it hurt! || 9.1.5
|-
| HUZZAH || /huzzah || <span title="ID 68">✔️</span> ||  || You cheer boisterously! Huzzah! || You cheer boisterously for %s! Huzzah! || 9.1.5
|-
| IMPRESSED || /impressed || <span title="ID 80">✔️</span> ||  || You clap vigorously, clearly impressed. || You clap vigorously for %s, clearly impressed. || 9.1.5
|-
| MAGNIFICENT || /magnificent || <span title="ID 185">✔️</span> ||  || You nod approvingly. Magnificent job! || You nod approvingly at %s. Magnificent job! || 9.1.5
|-
| QUACK || /quack || <span title="ID 78">✔️</span> ||  || You pretend to be a duck. Quack! || You quack at %s. Quack! || 10.0.2
|}

==See also==
* {{api|SendChatMessage}}() for sending custom emote text similar to <code>/emote</code> or <code>/me</code>
<!-- luals
---@param token EmoteToken
---@param unit? UnitToken
---@param hold? boolean
---@return boolean? restricted
function DoEmote(token, unit, hold) end
-->
```