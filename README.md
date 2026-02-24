Classical Chinese Rumble Notation (CCRN) is a notation system using classical Chinese to describe [RUMBLE VR](https://store.steampowered.com/app/890550/RUMBLE/) earthbending moves.

## Examples

| Move                    | CCRN Notation          | Meaning                                                                                               |
| ----------------------- | ---------------------- | ----------------------------------------------------------------------------------------------------- |
| Speed disc              | 召皿，擊之。                 | Summon disc, straight it.                                                                             |
| Speed ball with explode | 召石，擊轟之。                | Summon ball, staight explode it.                                                                      |
| Pillar Topple           | 召二木，擊其一。               | Summon two pillars, straight first one.                                                               |
| Slingshot               | 取物，持擊之。                | Take any structure, hold-straight it.                                                                 |
| wUKSUK                  | 召牆，勾揚擊勾揚之。             | Summon wall, uppercut-kick-staight-uppercut-kick it.                                                  |
| Seamless flight         | 取出土之物，扭之，躍，騎之以飛昇。      | Take ungrounded object, flick it, jump, mount it to fly.                                              |
| Wall trampoline         | 召牆，取出土平躺轟爆之牆，擊揚其一以擊其二。 | Summon wall, take ungrounded flat exploded wall, straight-kick the first wall to hit the second wall. |
| High dive               | 二躍，取飛躍之物，扭之，騎之以飛昇。     | Double jump, take flying object, flick it, mount it to fly.                                           |
| Cube waterbend          | 取出土之方，扭持之，以之觸來之物以免破。   | Take ungrounded cube, flick hold it, use it to touch incoming object to avoid destruction.            |

---

## Foreword

### Design Constraints

There are some constraints when designing this notation
1. Use real Chinese characters, grammar, and punctuation.
2. Don't just translate each element of the standard notation into Chinese. It would be boring to just have a 1-to-1 vocab mapping.
3. Play into the strengths of the classical Chinese: Implicity, reliance on context, dense information for each character etc.

### **Warning**: Amateur linguistics ahead

I am not an actual linguist in any sense, and this is very amateur work. As a result, there are probably many inaccuracies. Feel free to give criticism.

This is mostly a project for me to learn more about the grammar of (classical) Chinese and English, as well as to have fun describing rumble moves in an unconventional way.

Also, this notation may sound a bit pretentious or "中二病" to Chinese speakers, which is intended :)

### Issues

As an intermediate player not yet in the comma club, I haven't got experience with many parts of the tech available in RUMBLE. Thus there will be many interactions not included in this version of the notation. Feel free to tell me about things I've missed!

---

## How CCRN works

To describe a move in CCRN, you string together multiple **clauses** that describe the events that happen in the move in sequence using a subset of Chinese characters and phrases.

A clause is nothing but a sentence complete with the verb, an optional object, an optional subject, and other stuff attached to it.

However, you can't just write anything in Chinese and call it CCRN. That would be too much freedom.

Instead, only **4 types of clauses** are allowed to be used to describe moves:

1. **Structure Clauses**: Declares the existence of one or more structures.
	- 召皿: Summon disc
	- 召二石: Summon two balls
	- 取方: Take cube
	- 取入土之木: Take grounded pillar
	- 取出土之轟牆: Take ungrounded exploded wall
2. **Modifier Clauses**: Describes how a structure is modified by a player.
	- 擊之: Straight it
	- 擊勾之: Struppercut it
	- 擊勾揚之: SUK it
	- 擊其一: Straight first one
	- 擊其二: Straight second one
3. **Movement Clauses**: Describes the movement of a player including hand and body movements.
	- 走: Run
	- 待: Wait
	- 備: Return to base pose
	- 躍: Jump
	- 二躍: Jump twice
	- 刺躍: Dash jump
	- 躍刺: Jump dash
4. **Interaction Clauses**: Describes how players or objects interact with each other, usually with the intention of the interaction.
	- 騎之以飛昇: Mount it in order to fly
	- 以其二擊其一以擊敵: Use second structure to hit first structure in order to hit enemy
	- 以之觸前來之物以免破: Use it to touch incoming structure to avoid destruction

By stringing clauses together, moves can be described one step at a time.

### Example with syntax tree

```
Seamless flight (with cube)
取出土之方，扭之，躍，騎之以飛昇。
Take ungrounded cube, flick it, jump, mount it to fly.

- 取出土之方 (Structure clause): Take ungrounded cube
	- 取 (Verb): Take
		- 取 (Structure source verb): Take pre-existing structure
	- 出土之 (Attribute phrase): Ungrounded
		- 出土 (Attribute word): Ungrounded
		- 之 (Preposition)
	- 方 (Noun phrase as object): Cube
		- 方 (Structure type word): Cube
- 扭之 (Modifier clause): Flick it
	- 扭 (Modifier verb): Flick
	- 之 (Noun phrase as object): it
		- 之 (Object pronoun): The last referenced structure
- 躍 (Movement clause): Jump
	- 躍 (Verb): Jump
- 騎之以飛昇 (Interaction clause): Mount it in order to fly
	- 騎 (Verb): Mount
	- 之 (Noun phrase as object): it
		- 之 (Object pronoun): The last referenced structure
	- 以飛昇 (Resultative phrase): to fly
		- 以 (Preposition): to, in order to
		- 飛昇 (Verb Phrase): fly
			- 飛昇 (Verb): fly
```

Every clause is a complete sentence using an SVO structure.
- Subject: The subject is usually not mentioned, and is implicitly the person doing the move.
- Verb: The verb is mandatory, describing what's happening.
- Object: The object is only mandatory if the verb needs it.

Clauses are separated by full size commas (，) and moves are ended with full size periods. (。)
These punctuations can be omitted to make the notation shorter, but harder to read.

Within a clause, more phrases can be attached to give more information about the clause.

Don't worry about it right now. I'll explain the extra phrases when we need them.

```
There are these types of phrases
1. Attribute phrase: Describes the attribute of structures. (Ungrounded, airbourne...)
2. Quantifying phrase: Describes how many structures or how many times to do something.
3. Positional phrase: Describes the position of structures or players relative to other objects.
4. Resultative phrase: Describes the result of an event e.g. flying, hitting enemy. It is not an event in of itself.
5. Symbol assignement phrase: Explicitly assigns a symbol to a structure for reference later.
6. Symbol reference phrase: References a structure by symbol.
```


### Example 2

```
High Dive
召方，使方飛躍，二躍，扭之，騎之以飛昇。
Summon cube, to make cube fly in air, jump twice, flick it, mount it to fly.
```

- 召方 (Structure clause): Summon cube
	- 召 (Source word): Summon
	- 方 (Type word): Cube
- 使方飛躍 (Interaction clause): To make (another) cube fly in air
	- 使 (Interaction word): To make
	- 方 (Structre clause): (any) cube
		- 方 (Type word): Cube
	- 飛躍 (Interaction result): Fly in air
		- 飛躍 (Interaction word): Fly in air
- 二躍 (Movement clause): Jump twice
	- 二 (Number): Two
	- 躍 (Movement word): Jump
- 扭之 (Modifier clause): Flick it (the cube in air)
	- 扭 (Modifier word): Flick
	- 之 (Reference): The previous mentioned structure
		- 之 (Reference word): The previous mentioned structure
- 騎之以飛昇 (Interaction clause): Mount it in order to fly
	- 騎 (Verb): Mount
	- 之 (Noun phrase as object): it
		- 之 (Object pronoun): The last referenced structure
	- 以飛昇 (Resultative phrase): to fly
		- 以 (Preposition): to, in order to
		- 飛昇 (Verb Phrase): fly
			- 飛昇 (Verb): fly

---

### The Sequential Rule

In CCRN, clauses must be strung together in the same order as they are performed.

Example

```
For the move bSE...

(Legal) 召一石，擊轟之。-> Summon one ball, straight explode it.
- 召一石 (Structure phrase): Summon one ball
- 擊轟之 (Modifier phrase): Straight explode the previously mentioned structure.

(Illegal) 擊轟召之一石 -> (lit.) Straight explode a summoned ball
This is grammatical Chinese but is illegal for CCRN because it violates the sequential rule: ball is summoned before being straighted, but it was not notated in the correct order.
```

An exception is that for **pre-existing structures**, they should be mentioned **near the first time they are used in the move**, instead of being declared at the beginning.

Example

```
(Legal) 召方，持擊勾之，取來之方，持擊勾之。

- 召方 (Structure phrase): Summon cube
- 持擊勾之 (Modifier phrase): Hold straight uppercut it (the summoned cube)
- 取來之方 (Structure phrase): Take incoming cube
- 持擊勾之 (Modifier phrase): HSU it (the incoming cube)

(Legal but confusing) 取來之方，召方，持擊勾其二，持擊勾其一。
- 取來之方 (Structure phrase): Take incoming cube (implicitly assigned as 一)
- 召方 (Structure phrase): Summon a cube (implicitly assigned as 二)
- 持擊勾其二 (Modifier phrase): HSU the second one (summoned cube)
- 持擊勾其一 (Modifier phrase): HSU the first one (incoming cube)
```

---

## Structure Clauses

Structure clauses declare the existence of structures in the move. They describe how the structure came to be, as well as its attributes.

The core of a structure clause is the **source verb** and the **structure phrase**.
- **Source Word**: A verb describing whether the structure is *summoned* or *taken*.
- **Structure Phrase**: An object phrase describing the structure

### Source word: 召 or 取 -> Summon or take.

Structure phrases must start with the source word, which notates how the structure is acquired.

There are only two source words: "召" and " 取"

| Source Word | Pronunciation | Meaning | Implication                                                                                                                  | Example                      |
| ----------- | ------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| 召           | zhao4         | Summon  | The player should summon the structure at this step                                                                          | 召皿 -> Summon Disc            |
| 取           | qu3           | Take    | The structure should already exist in the game. It could be summoned by the player or the opponent at any point in the past. | 取牆 -> Take pre-existing wall |

### Structure Phrases

Structure phrases are noun phrases that describe structures. They consist of at least the **type word**, the noun, and a bunch of adjectives.

### Type word (Noun)

Let's set the adjective aside for now, and just focus on the noun.
Type word describes what type of structure is being declared.
These are all of the possible type words:

| Structure<br>   | Type Word | Pronunciation | Literal Meaning |
| --------------- | --------- | ------------- | --------------- |
| (Any) Structure | 物         | wu4           | object          |
| Disc            | 皿         | min3          | disc, plate     |
| Pillar          | 木         | mu4           | wood, tree      |
| Ball            | 石         | shi2          | rock            |
| Cube            | 方         | fang1         | square          |
| Wall            | 牆/爿       | qiang2        | wall            |
| Boulder         | 巨石        | ju4 shi2      | huge rock       |

### Putting them together: V + O

At this point, you can describe basics structure summons by putting the verb and object together.

- `召石` -> Summon Ball
- `取方` -> Take cube

### Adding phrases to the structure phrase

Now for the fun part, we can add words and phrases to the basic VO structure to be more specific about the structure being described.

These include:
- **Number words**: Describes multiple summons
- **Attribute phrases**: Describes the state of taken structures. Only valid for "取" (take).
- **Symbol assignment phrases**: Assigns a symbol to the structure for reference later. (Think varaible name assignment)
- **Positional phrases**: Describes position of the structure, usually relative to a player or **another structure phrase**. (Nested structure phrases go brrrrr)
- **Intent phrases**: Describes why the structure is summoned or taken.

They **must** be put together in this sequence

```
1. Structure source word (Verb)
2. Number word
3. Attributes phrase
4. Structure type word (Object)
5. Positional phrase
6. Symbol assignment phrase
7. Intent phrase
```

#### Number words: Multiple summons

If and only if multiple structures **of the same type and attribute** are summoned or taken in a row, then a number can be used to notate the number of structures being sourced.

```
取一方 -> Take one cube
召二牆 -> Summon two walls in a row
召五皿 -> Summon five discs in a row
取二入土之方 -> Take two grounded cubes
```

If no number words are mentioned, it is assumed to be one structure that is being sourced.

#### Attribute phrases: Adjectives for structures

When using 取 (taking pre-existing structure), attribute phrases can be added to restrict which structures are appropriate for the move.

They are all adjectives for structures, listed in the table below:

| Attribute word | Lit. Meaning           | Pronunciation  | Meaning in English | Valid for          |
| -------------- | ---------------------- | -------------- | ------------------ | ------------------ |
| 靜止             | Unmoving               | jing4 zhi3     | Unmoving           | Any structure      |
| 前來             | Incoming               | qian2 lai2     | Incoming           | Any structure      |
| 前去             | Outgoing               | qian2 qu4      | Outgoing           | Any structure      |
| 入土             | Into the ground        | ru4 tu3        | Grounded           | Any structure      |
| 出土             | Out of the ground      | chu1 tu3       | Free/ungrounded    | Any structure      |
| 轟爆             | Thundering & exploding | hong1 bau4     | Explosive          | Any structure      |
| 飛躍             | Flying & Jumping       | fei1 yao3      | Flying             | Any structure      |
| 急凍             | Quickly frozen         | ji2 dong4 zhi1 | Hit stopped        | Any structure      |
| 直立             | Standing stright       | zhi2 li4       | Upright            | Disc, pillar, wall |
| 平躺             | Laying flat            | ping2 tang3    | Flat               | Disc, pillar, wall |
| 歪斜             | Skewed                 | wai1 xie2      | Angled             | Disc, pillar, wall |

To construct attribute phrases, string all attribute words together in any order, then add the marker "之" (zhi1) to the end.

```
取入土之牆 -> Take grounded wall
- 取 take
- 入土 grounded
- 之 attribute phrase marker
- 牆 wall

取前來入土轟爆直立之牆 -> Take incoming grounded explosive upright wall
- 取 take
- 前來 incoming
- 入土 grounded
- 轟爆 explosive
- 直立 upright
- 之 attribute phrase marker
- 牆 wall
```

#### Positional Phrase

Positional phrases describe the relative position of the structure being summoned or taken.
They consist of these elements in order:
1. 於 (yu2): Positional phrase marker
2. Object: Another object, which could be one of the following:
	- 己: The player
	- 敵: The opponent
	- Another structure phrase
	- Reference to a structure
3. Relative location
	- 上: Above
	- 下: Under
	- 側: Next to
	- 後: Behind

```
於(obj)(location) -> at (location) relative to (obj) 
```

Examples

```
召方於地之下，揚之 -> Summon cube under opponent, kick it (the cube).
召牆於入土之牆下，擊之。 -> Summon wall under grounded wall, straight it (the previously grounded wall).
```

---

## Modifier Clauses

Modifier clauses are relatively straight forward: use verbs to describe modifiers, and a object phrase to describe the structure being modified.

### Modifier verbs

Modifier verbs are exactly what they sound like: Verbs to describe modifiers you can do in game.

| Verb | Pronunciation | Lit. Meaning | Modifier     |
| ---- | ------------- | ------------ | ------------ |
| 擊    | ji2           | to strike    | Straight     |
| 揚    | yang2         | to lift      | Kick         |
| 勾    | gou1          | hook         | Uppercut     |
| 踏    | ta4           | step on      | Stomp/Ground |
| 擋    | dang3         | to block     | Parry        |
| 持    | chi2          | to hold      | Hold         |
| 扭    | niu3          | to twist     | Flick        |
| 轟    | hong1         | to blast     | Explode      |

### Structure Reference Phrases

Structure reference phrases describe which structure to modify.
There are three different types of references, and the most implicit one should be preferred.
From most implicit to most explicit, they are:

| Reference Type     | Prefix   | Number System         | Example                                        |
| ------------------ | -------- | --------------------- | ---------------------------------------------- |
| Last Mentioned     | 之 (zhi1) | None                  | 擊之 -> Straight last mentioned structure        |
| Implicit Reference | 其 (qi2)  | Standard (一二三四五六七八九十) | 擊其二 -> Straight the second mentioned structure |
| Explicit Reference | None     | 天干 (甲乙丙丁戊己庚辛壬癸)       | 擊甲 -> Straight the structure marked as 甲       |

#### Last mentioned structure

The most common structure to reference is the last one mentioned.
Use "之" (zhi1) to reference the last structure mentioned.

#### Implicit Reference

When describing moves, whenever you describe a structure, a number is implicitly assigned to each structure you mention.
You can use "其" (qi2) followed by a regular number to reference any particular structure.

##### Examples

```
c1c2JSK1 -> 召二方，躍，擊揚其一。
- 召二方 (Structure Clause): Summon two cubes
- 躍 (Movement Clause): Jump
- 擊揚其一 (Modifier clause): Straight-kick the first (cube)
```


```
c1c2.HSU2 -> 召二方，待，持擊勾其二。
- 召二方 (Structure clause): Summon two cubes
- 待 (Movement clause): Wait
- 持擊勾其二 (Modifier clause): Hold, Straight, Uppercut the second (cube)
```

##### Exception: Positional structures are ignored

When implicitly referencing structures using "之" or "其", the structure phrases contained in positional phrases are ignored.

```
取出土之方於出土之方側，扭之。 -> Take ungrounded cube next to ungrounded cube, flick it (the first ungrounded cube).
- 取出土之方於出土之方側: Structure clause
	- 取: Take
	- 出土之方: Ungrounded cube (Implicit assigned as 一)
	- 於出土之方側: Positional phrase
		- 於: at
		- 出土之方: ungrounded cube (Not implicitly assigned)
		- 側: side
- 扭之: Modifier cluase
	- 扭: Flick
	- 之: It (References 一)
```

#### Explicit Reference

If you have explicitly assigned a symbol to a structure, you can use them to explicitly reference them.
Symbols are restricted to the 天干 counting system: one of 甲乙丙丁戊己庚辛壬癸
This is mostly reserved for situations where there are so many structures that implicit references can get too confusing.

```
召二皿，召方為甲，取出土之方，擊之，擊甲。 -> Summon two discs, summon cube as 甲, take ungrounded cube, hit it (ungrounded cube), hit 甲。
```

These rules mean that the maximum number of structures that can be referenced is 20.
If your move uses more than 20 structures, you probably are doing something outside the realm of possibility.

---

## Movement Clauses

> WIP!

Movement clauses describe how a player moves, including body and hand movements.

| Movement Word | Pronunciation | Lit. Meaning    | Meaning        |
| ------------- | ------------- | --------------- | -------------- |
| 待             | dai4          | to wait         | Pause          |
| 備             | bei4          | to prepare      | Base pose      |
| 步             | bu4           | step            | Move/Walk      |
| 走             | zou3          | to walk, to run | Run            |
| 刺             | ci4           | to stab         | Dash           |
| 躍             | yue4          | to jump         | Jump           |
| 轉             | zhuan3        | to turn         | Turn/Pivot     |
| 反             | fan3          | opposite        | U-Turn         |
| 鎖             | suo3          | lock            | Lock-on        |
| 盾             | dun4          | shield          | Guard pose     |
| 換手            | huan4 shou3   | change hands    | Use other hand |

---

## Interaction Clauses

> WIP!

Describes physical interactions between objects and players

---

## Intention phrases

> WIP!

Intention phrases describe the reason of doing a clause.
They can be added to any type of clause, but only at the end.

### Making structures interact

```
以之擊已: To hit oneself
以之擊敵: To hit opponent
以其一擊其二: To make the first structure hit the second structure
以其一觸其二: To make the first structure touch the second structure
```

### Structure launch

To notate structure launching, this clause is used:

```
使(struct)飛躍 -> to make (struct) fly in air
```

Examples

```
召方使方飛躍 -> Cube launch a cube
召柱使地柱飛躍 -> Pillar launch a grounded pillar
```


---

## Vocabulary

To avoid ambiguity, the basic moves are made to have different pronunciations from each other regardless of tone.

The following vocabulary chart is grouped by the type of move or sentence structure.

(This list might be outdated)

| Vocabulary | Pronunciation (pinyin)  | Literal Meaning in Chinese | Meaning in RUMBLE                                    |
| ---------- | ----------------------- | -------------------------- | ---------------------------------------------------- |
| 擊          | ji2                     | to strike                  | Straight                                             |
| 揚          | yang2                   | to lift                    | Kick                                                 |
| 勾          | gou1                    | hook                       | Uppercut                                             |
| 踏          | ta4                     | step on                    | Stomp/Ground                                         |
| 擋          | dang3                   | to block                   | Parry                                                |
| 持          | chi2                    | to hold                    | Hold                                                 |
| 扭          | niu3                    | to twist                   | Flick                                                |
| 轟          | hong1                   | to blast                   | Explode                                              |
| 盾          | dun4                    | shield                     | Guard pose / Shield                                  |
| 換手         | huan4 shou3             | change hands               | Use other hand                                       |
| 物          | wu4                     | object                     | (Any) Structure                                      |
| 皿          | min3                    | disc, plate                | Disc                                                 |
| 木          | mu4                     | wood, tree                 | Pillar                                               |
| 石          | shi2                    | rock, pebble               | Ball                                                 |
| 方          | fang1                   | square                     | Cube                                                 |
| 牆          | qiang2                  | wall                       | Wall                                                 |
| 巨石         | ju4 shi2                | huge rock                  | Boulder                                              |
| 待          | dai4                    | to wait                    | Pause                                                |
| 備          | bei4                    | to prepare                 | Base pose                                            |
| 步          | bu4                     | step                       | Move/Walk                                            |
| 走          | zou3                    | to walk, to run            | Run                                                  |
| 刺          | ci4                     | to stab                    | Dash                                                 |
| 躍          | yue4                    | to jump                    | Jump                                                 |
| 轉          | zhuan3                  | to turn                    | Turn/Pivot                                           |
| 反          | fan3                    | opposite                   | U-Turn                                               |
| 鎖          | suo3                    | lock                       | Lock-on                                              |
| 立於(物)上     | li4 yu2 (wu4) shang4    | stand above object         | Mount on (object)                                    |
| 推          | tui1                    | push                       | Bump                                                 |
| 己          | ji3                     | self                       | Self                                                 |
| 敵          | di2                     | enemy                      | The opponent / enemy                                 |
| 召(物)       | zhau4 (wu4)             | summon                     | Summon (object)                                      |
| 取(物)       | qu3 (wu4)               | take                       | Take (object)                                        |
| 入土(之物)     | ru2 tu3 (zhi1 wu4)      | put into ground            | Grounded (object)                                    |
| 出土(之物)     | chu1 tu3 (zhi1 wu4)     | come out of ground         | Free/ungrounded (object)                             |
| 前來(之物)     | qian2 lai2 (zhi1 wu4)   | incoming                   | Incoming (object)                                    |
| 飛躍(之物)     | fei1 yao4 (zhi1 wu4)    | flying                     | Airbourne (object)                                   |
| 轟爆(之物)     | hong1 bau4 (zhi1 wu4)   | blasting, rumbling         | Explosive (object)                                   |
| 反覆         | fan3 fu4                | repeatedly                 | Repeatedly (do something)                            |
| (物件詞)為(符)  | (struct) wei2 (fu2)     |                            | Assign (explicit symbol) to (structure phrase)       |
| (操作詞)之     | (mod) zhi1              |                            | (Modify) previously mentioned structure              |
| (操作詞)其(符)  | (mod) qi2 (fu2)         |                            | (Modify) structure with implicit symbol              |
| (操作詞)(符)   | (mod) qi2 (fu2)         |                            | (Modify) structure with explicit symbol              |
| 使(物件詞)飛躍   | shi3 (struct) fei1 yue4 |                            | Structure launch: To make (structure) fly in air     |
| 於(物)(位置)   | yu2 (wu4) (wei4 zhi4)   |                            | Positional clause: At (prep) relative to (structure) |
| 擊(物)於盾     | ji2 (struct) yu2 dun4   |                            | Hit (structure) on guard shield                      |

