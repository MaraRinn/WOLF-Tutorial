# WOLF Tutorial Notes

## WOLF Tutorial Ships

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
+ 3.75m manufacturing hopper
  + 5 WOLF Material Kit -> 5000 Material Kits/day

### Passengers to Orbit

 54 passengers (6 * 9) requires:

+ 108 extra habitation
+ 108 extra life support
+ 4 food, 4 oxygen, 20 water

### Components

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
