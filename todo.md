Remove SLEX
Fix error logs
# priorize mining/science stations over other if budget higher
remove mining station cap ?
Nerf snowballing? Boost midgame powerup?
Make a "help" interface (why no fleets, why low fleets, how much does it bring, how to get more corps, ...)
Give sensors
Add buy/sell stations
Add lease fleets
Fix convoy (no class name ?)
Fix construction going into marauder ???
Add a monthly event which sets aggressivity to  other countries that aren't in war?
Make convoy depop if no path
add new leader traits
[*] Corps leaders gain passive xp (around 36 per year)
Update loc

To test:
Fix convoys going into hostile capital ???
Added a check for corps not having overlords when processing fleet AI, now it will just wait an iisc tick (30-60 days)
Fixed corp science ships being in evasive stance instead of passive
Fix corp names
Make corps go into overlord war
Leader gaining xp on surveying

Done:
Watch agreement contract changing
Prevent builders choosing same destination
Fix set_name convoy
Remove inherent +100% station production
Improve performance and code for taxes deposits
Add loc iisc_agreement_preset

TEST recruit scientists
more custom diplomacy
Check when overlord becomes vassal (make sure nothing breaks when referencing overlord)
spawn military ships
add supply lines (from a country or from a corp) => event on arrival for remuneration
add technologies for military ships
make convoys head back
check fleet names
change a bit iisc_should_create_military_fleet and reinforce
add passive repair

[19:16:49][trigger_impl.cpp:847]: Script Error: Invalid context switch[event_target:iisc_escort_target.solar_system], file:  file:  file: events/iisc_military_events.txt line: 13 line: 1 line: 1, Scope: 
ancient_mining_expansion_barge


use is_species intermediate for supply?
use mining operations entity
supply cost less
supply provide more
more/less taxes
more profit from surveys

Military fleet actions:
0 - idle
1 - patrolling
2 - escorting
3 - temporary escorting (builder/science ships/...)
4 - awaiting reinforcement (before striking ennemy)
5 - attacking a target
8 - going to repair
9 - going to naval shipyard

when escorting, special flag => separate event loop (old one stops)

Space corp budget: (default)
Military ships 25%
Convoys 20%
Supply 10%
Builder 5%
Science ships 5% 
Mining stations 15%
Research stations 15%
Colonization 5%

Modification on budget
xenophile: higher convoy and science ships
xenophobe: higher colonization, lower science ships
egalitarian: higher colo and military
authoritarian: higher mining stations, builder and military
materialist: higher science ships, science stations, lower convoys and supply
spiritualist: higher convoys, colonization, lower science ships, research stations
militarist: higher military and supplies
pacifist: higher convoys, colonization, stations, lower military

Ideas
xenophile: more profit from trade
xenophobe: more profit from intra trade, intra trade more often
egalitarian: leader bonus, profit from specialists/rulers?
authoritarian: more profit from pops
materialist: science ships/research station cost less, research techs faster
spiritualist: construction ships/mining stations cost less, add spirit influence on trade partner
militarist: more military ships, unhappier, firerate
pacifist: happier

Implemented
xenophile:
xenophobe: 
egalitarian: 
authoritarian: 
materialist: techs cost less (90%)
spiritualist:
militarist: 
pacifist: 

Passive income
xenophile: +0.3EC per free not-purged organics pop of different species on HQ
xenophobe: +/-0.3 EC per same/different free species pops on HQ
egalitarian: +0.2EC per free (not purged either) pops on HQ
authoritarian: +0.5EC per slaves on HQ
materialist: +0.5EC per robot pops on HQ
spiritualist: +0.3EC per spirit pops on HQ
militarist: +1EC per army on HQ
pacifist: +0.5EC per years of peace from the overlord (up to 25 for 50 years, per 10 years intervals)
gestalt: +5EC flat
