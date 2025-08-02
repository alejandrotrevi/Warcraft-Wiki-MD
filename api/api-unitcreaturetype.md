# API UnitCreatureType

**Contributor:** GjfLeo

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the creature classification type of the unit (e.g. Beast).
 name, id = UnitCreatureType(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;name:{{apitype|string}} - the ''localized'' creature type of the unit, or <code>nil</code> if the unit does not exist, or if the unit's creature type isn't available.
:;id:{{apitype|number}} : {{dbc|CreatureType}}

==Details==
* The default Blizzard UI displays an empty string instead of "Not specified" for units with that creature type. {{SITENAME}} refers to these units as [[Uncategorized creature|"Uncategorized"]].

==Values==
{| class="darktable zebra sortable col1-center"
! ID !! enUS !! deDE !! esES !! esMX !! frFR !! itIT !! ptBR !! ruRU !! koKR !! zhCN !! zhTW
|-
| 1 || Beast || Wildtier || Bestia || Bestia || Bête || Bestia || Fera || Животное || 야수 || 野兽 || 野獸
|-
| 2 || Dragonkin || Drachkin || Dragon || Dragón || Draconien || Dragoide || Dracônico || Дракон || 용족 || 龙类 || 龍類
|-
| 3 || Demon || Dämon || Demonio || Demonio || Démon || Demone || Demônio || Демон || 악마 || 恶魔 || 惡魔
|-
| 4 || Elemental || Elementar || Elemental || Elemental || Élémentaire || Elementale || Elemental || Элементаль || 정령 || 元素生物 || 元素生物
|-
| 5 || Giant || Riese || Gigante || Gigante || Géant || Gigante || Gigante || Великан || 거인 || 巨人 || 巨人
|-
| 6 || Undead || Untoter || No-muerto || No-muerto || Mort-vivant || Non Morto || Renegado || Нежить || 언데드 || 亡灵 || 不死族
|-
| 7 || Humanoid || Humanoid || Humanoide || Humanoide || Humanoïde || Umanoide || Humanoide || Гуманоид || 인간형 || 人型生物 || 人型生物
|-
| 8 || Critter || Kleintier || Alma || Alma || Bestiole || Animale || Bicho || Существо || 동물 || 小动物 || 小動物
|-
| 9 || Mechanical || Mechanisch || Mecánico || Mecánico || Machine || Meccanico || Mecânico || Механизм || 기계 || 机械 || 機械
|-
| 10 || Not specified || Nicht spezifiziert || No especificado || Sin especificar || Non spécifié || Non Specificato || Não especificado || Не указано || 기타 || 未指定 || 不明
|-
| 11 || Totem || Totem || Tótem || Totém || Totem || Totem || Totem || Тотем || 토템 || 图腾 || 圖騰
|-
| 12 || Non-combat Pet || Haustier || Mascota no combatiente || Mascota mansa || Familier pacifique || Animale Non combattente || Mascote não-combatente || Спутник || 애완동물 || 非战斗宠物 || 非戰鬥寵物
|-
| 13 || Gas Cloud || Gaswolke || Nube de Gas || Nube de Gas || Nuage de gaz || Nube di Gas || Gasoso || Газовое облако || 가스 || 气体云雾 || 氣體雲
|-
| 14 || Wild Pet || Ungezähmtes Tier ||  ||  || Mascotte sauvage ||  ||  ||  ||  || 野生宠物 || 
|-
| 15 || Aberration || ||  ||  ||  ||  ||  ||  ||  || 畸变怪 || 
|}

==Patch changes==
* {{Patch 11.1.5|note=Added <code>id</code> return value. [https://github.com/Stanzilla/WoWUIBugs/issues/118 WoWUIBugs#118]}}

==See also==
* https://www.wowace.com/projects/libbabble-creaturetype-3-0

{| {{apitable}}
{{apirow | Related API | {{api|UnitCreatureFamily}} }}
|}
```