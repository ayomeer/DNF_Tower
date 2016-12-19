# DNF - Tower of Death

## Components

### Frontend / View

#### Server plugin messages on event

*Three more victories and thy'll vanquish [rank] master [player] on [map]! Braveth up [player].*

#### Server plugin commands

##### !bo[number]

Challenge for Best of [number] an ingame player.

Both players in warmup should type it before game begins.
If one forfeit/quit/disconnect, abandon bo5 computation.

*You challenged [rank][master][player] in a Bo5 on [map].*

Once the second player does equally:

*[rank][master][player] accepted. Unsheathe thy rail!*

Once master triumphed:

*You triumphed of [rank] master [player] on [map] in Bo5. Hurrah!*

Once defeated:

*One more defeat against [rank] master [player] on [map]. Sir [player], thou shall not despair, tis in doubts one shall find strength.*

##### !rank [player]

*[player] Bloodrun rank: Veteran*

##### !master [player]

*Highest Bloodrun master vanquished: [player] [rank]*

##### !remaining [player]

*Remaining masters for [rank] rank: [player]@Bloodrun | [player]@Aerowalk*

##### !lowest [player]

*Your lowest rank is [rank] on Cure. Try to challenge [player] on Cure.*

##### !highest [player]

*Your highest rank is [rank] on Toxicity*

### Backend / Logic

#### Implementation
This could work as a server plugin: https://github.com/MinoMino/minqlx

#### Data source

##### QLstats.net
Stats could be gotten through <http://qlstats.net>

- how many times [player] played on DNF servers,
- his dmg versus best master of this map he beat,
- w/k ratio versus best master of this map he beat,
- glicko ranking versus best master of this map he beat,

##### a custom database

**Not necessary for making ranks work. Only used to keep track of master per level.**

SQL would be prefered for storing 2D data such as :

| playername(string) | map(string) | level(string) | master(bool) |

Any data that can be harnessed from QLstats.net by request shall not be duplicated here.

This database shall only be used to store specific Tower of Death data.

## Installation

1 - Run a Debian server

2 - Install QL dedicated server

3 - Install https://github.com/MinoMino/minqlx

4 - Install this plugin in [pluginfolder]

5 - ...?

6 - PROFIT.

## FAQ

### How should i feel about that ?

noob

### What is it behind my neck ?

it's a me

### Does Santa Claus exist ?

no
