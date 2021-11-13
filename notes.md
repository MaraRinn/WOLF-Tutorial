# WOLF Tutorial Notes

## WOLF Tutorial Ships

How to keep track of which crew are required for which infrastructure lander?

1. Build in batches. One lander for each biome, record what crew are required for each lander, send all the crew in one batch.
2. Name each lander uniquely, keep a record of which lander is going to which biome and what crew it requires, send crew as required for each lander

Example:

### Crew Transport Pacer

~~Minmus Flats Oxygen~~

+ Medic
+ Scientist

~~Great Flats Silicon~~

+ Geologist x 2
+ Miner
+ Technician

~~Greater Flats Chemicals~~

+ Engineer
+ Miner x 2
+ Technician

### Crew Transport Telpix

N/A

Then send a crew ship to Minmus with those specialists aboard. Build the landers as you get the materials to do so, put the crew on board and land them. Strike the ship off the list as it's connected to the biome depot.

## Preparation

Make sure that the craft can load into the stock game with only Bon Voyage and MKS/WOLF addons.

### Packaging

I'll need a Makefile to prepare a ZIP archive of:

+ Ships
+ Subassemblies
+ Save games

## Plan

+ Produce materials on Kerbin to ship to orbit
  + Material Kits
  + Fuel
  + Food
  + Fertiliser
  + Water
  + Oxygen
+ Build shipyard and send it to orbit
+ With that shipyard, build:
  + another shipyard
  + tanker
  + route builder
+ Add a resource hauler to deliver the materials for a manufacturing hopper and a depot module
+ Send that small fleet to Minmus (note staging orbit for shipyard ~800km)
+ At Minmus establish the orbital depot
+ Build the depot landers and establish all Minmus biome depots
+ Establish routes both ways between orbit and all Minmus biomes
+ Establish Material Kit manufacturing (use imported life support resources)
+ Build up local life support
+ Build up local manufacture of Specialized Parts
+ Build up local manufacture of advanced materials:
  + Alloys
  + Electronics
  + Prototypes
  + Robotics
  + Synthetics

## Shipyard Notes

### Hoppers

+ 2.5m manufacturing hopper
  + 2 WOLF Material Kit -> 2000 Material Kits/day
  + 2 WOLF Specialised Parts -> 529.1 Specialised Parts/day
  + 1 WOLF Alloys -> 128.21 Alloys/day
  + 1 WOLF Electronics -> 264.55 Electronics/day
  + 1 WOLF Prototypes -> 264.55 Prototypes/day
  + 1 WOLF Robotics -> 200.00 Robotics/day
  + 1 WOLF Synthetics -> 500.00 Synthetics/day
+ 3.75m manufacturing hopper
  + 5 WOLF Material Kit -> 5000 Material Kits/day
  + 5 WOLF Specialized Parts -> 1322.75 Specialized Parts/day
  + 1 WOLF Alloys -> 384.62 Alloys/day
  + 1 WOLF Electronics -> 793.65 Electronics/day
  + 1 WOLF Prototypes -> 793.65 Prototypes/day
  + 1 WOLF Robotics -> 600 Robotics/day
  + 1 WOLF Synthetics -> 1500 Synthetics/day

### Components

Note that materials are used in a highly asymmetric ratio something along the lines of:

+ 100,000 Material Kits
+ 100 Specialized Parts
+ 100 Synthetics
+ 10 Alloys
+ 1 Robotics

In terms of hopper output, this means that to maintain production at the appropriate ratios we need the following ratio of 3.75m hoppers:

+ 12,000 Material Kit hoppers (60,000,000/day)
+ 45 Specialized Parts hoppers (60000/day)
+ 40 Synthetics hopper (60000/day)
+ 15 Alloys hoppers (6000/day)
+ 1 Robotics hopper (600/day)
+ 1 Electronics hopper (793/day)

The strategy we'll apply in this walkhrough is to produce Robotics and Alloys at one location and ship them to shipyards around the Kerbol System, while Material Kits need to be produced very close to the point of consumption, for example being connected to the Shipyard itself. We'll produce Specialised Parts and Synthetics at the shipyard too, and just deal with always having a surplus.

The broad strokes of the walkthrough strategy will thus be:

+ Establish Material Kits production
+ Buy the specialized parts and advanced materials required to build Minmus Infrastructure
+ Develop Minmus Infrastructure to produce 5 WOLF Specialized parts and 1 each of the advanced materials

Total production required from Minmus will then be the minimum required to run 1 3.75m hopper of each building material:

1. Specialized Parts x 5
   + 2 Refined Exotics
   + 2 x (2 Exotic Minerals, 3 Rare Metals)
   + 3 Silicon
1. Synthetics x 1
   + Exotic Minerals x 4
   + 1 Polymers
3. Alloys x 1
   + 4 Rare Metals
4. Robotics x 1
   + 5 Alloys
5. Electronics x 1
   + 5 Synthetics
6. Prototypes x 1
   + 5 Robotics
   + 5 Electronics
   + 5 Specialized Parts

Note that the required production of alloys and synthetics is mostly to support the Prototypes production chain.

This will be enough to support production up until around the point we have a thousand Material Kits hoppers.

#### Shipyard

+ 100,860 Material Kits
+ 111 Specialized Parts
+ 22 Alloys
+ 1 Synthetics

#### MK Hopper

+ 71,532 Material Kits
+ 85 Specialized Parts
+ 73 Synthetics
+ 2 Robotics

#### Sp/Synthetics Hopper

+ 24,092 Material Kits
+ 281 Specialized Parts
+ 78 Alloys
+ 73 Synthetics
+ 10 Robotics

#### LF/OX Hopper

+ 83,442 Material Kits
+ 92 Specialized Parts
+ 28 Alloys
+ 72 Synthetics
+ 2 Robotics

#### Minmus Depot Lander

+ 18,135 Material Kits
+ 74 Specialized Parts
+ 27 Synthetics
+ 1 Robotics

## Planning A New Expansion

I want to produce Robotics, but robotics requires:

+ 5 Alloys
+ 5 Material Kits
+ 2 Lab points
+ 2 Maintenance points
+ 2 Power points
+ 1 engineer Crew point

Each Alloys production requires:

+ 4 Rare Metals
+ 1 Metals
+ 1 Lab point
+ 1 Maintenance point
+ 1 Power point
+ 1 Scientist Crew point

So to start with, where can we source 20 Rare Metals? Check all the depots to make sure we have resources directed to orbit, then check harvestable resources for unexploited deposits. The Great Flats and Greater Flats biomes have Rare Metals and Metallic Ore to spare. I'll put a rare metals extraction facility on the **Great Flats**.

Start with the Fabricators to produce 5 Alloys, then add the extractors to provide the raw materials required. Now add the power, maintenance and other support modules. Then add the crew. If the crew require life support and habitation add those too, and keep going until the requirements are met.

Now record the crew that are required, and save this lander -- I use a folder "WOLF Depot Landers" to help keep my ship designs organised.

We have space on the crew transport, let's set up another lander.

Along with the Great Flats alloys production we'll need more Material Kits.

Each Material Kits fabricator requires:

+ 1 Chemicals
+ 2 Metals
+ 2 Polymers
+ 1 Maintenance
+ 1 Power
+ 1 Technician Crew point

So ideally a biome which already has Metallic Ore or Substrate to exploit (ideally both), and perhaps with some Minerals to turn into Chemicals. It looks like the **Highlands** have the materials we need.

Start with a Minmus Heavy Lander and add the desired output: in this case a Fabricator set to produce Material Kits. Now add the extraction and processing required to take some Minerals, Metallic Ore and Substrate, and turn them into Chemicals, Metals and Polymers. Along the way you'll need more power and maintenance. Then add the crew and you'll find you need more habitation and life support, and so forth. Eventually you'll reach the limit for the lander frame (36 WOLF modules), at which point keep a note of any surplus production (in my case, there's capacity for 2 more Material Kits fabricators).

## Passengers to Orbit

 54 passengers (6 * 9) requires:

+ 108 extra habitation
+ 108 extra life support
+ 4 food, 4 oxygen, 20 water

## Screenshots required

## Locations

+ KSC/right next to Kerbal centre (-0.1, -74.647)
+ KSC/Shores Just north of runway (-0.04, -74.709)
+ Kerbin Shores (0.01,-74.8)
+ Grasslands (0.0 -75.38)
+ Highlands (1.741, -77.339)
+ Mountains (0.637, -78.659)
+ Desert (1.472, -86.435)
+ Ice Caps (71.386, -92.709) which needs a waypoint around (36.898, -63.906) on the way there and back to constrain the route finding

## To Do

+ Extract list of screenshot names from wiki_page.md
+ Figure out a Markdown notation to provide the caption and filename for each screenshot
+ Find or build a tool to build TOC from Markdown headings
+ Find or build a tool to generate table of illustrations
+ Resource conversion table listing the producer that you can get desired materials from (ie: one column for a resource, second column showing which modules have the recipe)

## References

[KSPFORUMMKS]: https://forum.kerbalspaceprogram.com/index.php?/topic/154587-111x-modular-kolonization-system-mks/ "KSP Forum: MKS Announcement Thread"
[WOLFIWPC]: https://github.com/UmbraSpaceIndustries/MKS/wiki/WOLF-%E2%80%94-Industry-without-the-part-count "WOLF: Industry without the part count"
[MRWOLFTS]: https://github.com/MaraRinn/WOLF-Tutorial-Ships "Mara Rinn's WOLF Tutorial Ships repository"
[BCRESDIAG]: https://forum.kerbalspaceprogram.com/index.php?/topic/154587-111x-modular-kolonization-system-mks/&do=findComment&comment=4026544 "bigcalm's resource diagram"
