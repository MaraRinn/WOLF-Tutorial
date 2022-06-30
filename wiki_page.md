# WOLF Walkthrough -- Industry Without the Part Count <!-- omit in toc -->

- [WOLF From Scratch: Introducing WOLF Infrastructure on Kerbin](#wolf-from-scratch-introducing-wolf-infrastructure-on-kerbin)
  - [The Plan](#the-plan)
  - [Start a New Sandbox Game](#start-a-new-sandbox-game)
  - [WOLF Biomes](#wolf-biomes)
  - [Surveying Harvestable Biome Resources](#surveying-harvestable-biome-resources)
  - [WOLF Dashboard -- Harvestable Resources and Depots](#wolf-dashboard----harvestable-resources-and-depots)
  - [WOLF Modules](#wolf-modules)
  - [Establish KSC Depot](#establish-ksc-depot)
  - [WOLF Infrastructure Expansion](#wolf-infrastructure-expansion)
  - [Adding Production to WOLF Depots](#adding-production-to-wolf-depots)
  - [WOLF Routes](#wolf-routes)
    - [Route Builder Rover](#route-builder-rover)
  - [WOLF Transfers](#wolf-transfers)
  - [Transport Routes and Transport Credits Costs](#transport-routes-and-transport-credits-costs)
    - [Quick and Dirty Transport Credit Example Flights](#quick-and-dirty-transport-credit-example-flights)
    - [Transport Module for Transport Credits](#transport-module-for-transport-credits)
    - [How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles](#how-to-avoid-transport-credit-costs-of-propellant-consuming-vehicles)
  - [Bootstrapping Kerbin Orbit WOLF Infrastructure](#bootstrapping-kerbin-orbit-wolf-infrastructure)
  - [Commission Kerbin Shipyard](#commission-kerbin-shipyard)
  - [Extracting Resources from WOLF to MKS](#extracting-resources-from-wolf-to-mks)
  - [Establishing the Kerbin Shipyard](#establishing-the-kerbin-shipyard)
- [Minmus Shipyard](#minmus-shipyard)
  - [Minmus Expansion Shipyard](#minmus-expansion-shipyard)
  - [Minmus Expansion](#minmus-expansion)
    - [Minmus CommNet and Skycrane](#minmus-commnet-and-skycrane)
    - [Crew Transport Preparation](#crew-transport-preparation)
    - [Minmus Route Preparation](#minmus-route-preparation)
    - [01 Midlands Exotic Minerals](#01-midlands-exotic-minerals)
    - [02 Greater Flats Synthetics](#02-greater-flats-synthetics)
    - [03 Midlands Agricultural Support](#03-midlands-agricultural-support)
    - [04 Greater Flats Food and Electronics](#04-greater-flats-food-and-electronics)
    - [05 Greater Flats Robotics](#05-greater-flats-robotics)
    - [Maximising Minmus Production](#maximising-minmus-production)
    - [06 Lowlands Polymers](#06-lowlands-polymers)
    - [07 Flats Stage 1](#07-flats-stage-1)
    - [08 Highlands Material Kits (blue)](#08-highlands-material-kits-blue)
    - [09 Greater Flats Material Kits (yellow)](#09-greater-flats-material-kits-yellow)
    - [10 Poles Exotic Minerals (white)](#10-poles-exotic-minerals-white)
    - [11 Midlands Exotics and Food](#11-midlands-exotics-and-food)
    - [12 Great Flats Specialized Parts](#12-great-flats-specialized-parts)
    - [13 Flats Chemicals and Silicon (yellow)](#13-flats-chemicals-and-silicon-yellow)
    - [14 Lesser Flats Rare Metals (blue)](#14-lesser-flats-rare-metals-blue)
    - [15 Highlands Rare Metals](#15-highlands-rare-metals)
    - [16 Greater Flats Industry Park](#16-greater-flats-industry-park)
    - [17 Great Flats Fuel](#17-great-flats-fuel)
    - [18 Flats Fuel (purple)](#18-flats-fuel-purple)
    - [19 Highlands Life Support](#19-highlands-life-support)
  - [Passenger Transport](#passenger-transport)
    - [Passengers from KSC to Kerbin Orbit](#passengers-from-ksc-to-kerbin-orbit)
    - [Passengers from Kerbin Orbit to Minmus Orbit](#passengers-from-kerbin-orbit-to-minmus-orbit)
    - [Transfer Passengers to Depot Expansion](#transfer-passengers-to-depot-expansion)
  - [The Mun Expansion](#the-mun-expansion)
    - [Mun Shipyard](#mun-shipyard)
    - [Mun CommNet](#mun-commnet)
    - [Mun Route Builder Rover](#mun-route-builder-rover)
    - [Mun Depots](#mun-depots)
    - [01 Farside Crater Material Kits](#01-farside-crater-material-kits)
    - [02 Highlands Specialized Parts](#02-highlands-specialized-parts)
    - [03 East Farside Polymers](#03-east-farside-polymers)
    - [04 Twin Craters Polymers](#04-twin-craters-polymers)
    - [05 Canyons Exotic Minerals](#05-canyons-exotic-minerals)
    - [06 Farside Basin Material Kits](#06-farside-basin-material-kits)
    - [07 Canyons Electronics and Robotics](#07-canyons-electronics-and-robotics)
    - [08 Twin Craters Material Kits](#08-twin-craters-material-kits)
    - [09 East Farside Crater Rare Metals](#09-east-farside-crater-rare-metals)
    - [10 Farside Crater Specialized Parts](#10-farside-crater-specialized-parts)
    - [11 Highlands Specialized Parts](#11-highlands-specialized-parts)
    - [12 Polar Crater Exotic Minerals](#12-polar-crater-exotic-minerals)
  - [Duna Expansion](#duna-expansion)
    - [Relay Satellites](#relay-satellites)
    - [01 Midland Sea Material Kits](#01-midland-sea-material-kits)
- [WOLF Walkthrough Conclusion](#wolf-walkthrough-conclusion)

## Goals

The in-game goals for the walkthrough are roughly:

1. Introduce you to WOLF infrastructure on Kerbin
2. Bootstrap WOLF infrastructure on Minmus using resources exported from Kerbin
3. Bootstrap WOLF infrastructure on Mun using resources from Minmus
4. Bootstrap WOLF infrastructure on Duna using resources and advanced materials exported from Kerbin/Minmus/Mun

These stages will go from the basic WOLF industry supported on Kerbin to more advanced industry on Minmus, then expansions to Mun and Duna showing how to start a new mid- to late-game industrial expansion using WOLF.

## WOLF for the Adventurous

RoverDude wrote up [this introduction to WOLF][RDWOLF1] which outlines most of what you need to know to get started. There's also RoverDude's [explanation of transport routes and transport credits][RDTRAN1] which will be expanded upon in this walkthrough. This walkthrough really only restates what is written there with a few step by step examples and an end goal of manufacturing spaceships at an orbital shipyard and expanding infrastructure to Minmus, Mun, and Duna.

## WOLF Resource Conversions

There are a number of differences in the resource chain between MKS and WOLF, check [RoverDude's resource conversion diagram][RDCONV] for the details.

# WOLF From Scratch: Introducing WOLF Infrastructure on Kerbin

WOLF is an industry-focused extension to the industrial activities enabled in the Modular Kolonisation System. In typical mid- to late-game save files using MKS, you will have hundreds of MKS modules scattered about the place, with your planetary maps littered with various mining, refining or manufacturing facilities.  All of these facilities and the per-tick or per-second calculations they require place significant load on the KSP simulation, and loading up the models when they get in physics range can produce significant lag in the graphics engine.

The idea with WOLF is to provide the same industrial capability as MKS without the part count, without the lag, and without endless futzing around with manufacturing lines to get everything working the way you expect it to (including, for example, having to visit each industry site every few days to "catch up" with production that was supposed to happen in the meantime).

WOLF is intended as an enhancement to MKS industry — even if you haven't got enough parts in your infrastructure to invoke the Kraken, WOLF can still be handy for you by providing part-free and attention-free resource production and transfers between biomes on the same planet, between surface and orbit, and between worlds.

## The Plan

For this part of the walkthrough, the focus is on introducing the WOLF components and workflows:

1. Explore WOLF biomes and depots
2. Introduce WOLF transport routes and shipments
3. Prepare the infrastructure to support expansion to Minmus

Throughout this guide you'll see reference to PAW, which is the "Part Action Window" that you typically open up by right-clicking on a part.

## Start a New Sandbox Game

Before you start a new KSP game, you'll need to install the Umbra Space Industries add-ons that make MKS and WOLF work:

1. Download the [Umbra Space Industries add-on collection][USIRELEASES] - this walkthrough is based on the "Unstable Release 112.0.1-bleeding-edge.2" package released 24 October 2021
2. Open that USI archive and copy all the things inside the GameData folder into the KSP GameData folder
3. Also download [Community Resource Pack][CRPRELEASES] - you'll need this for resources to actually be available. Download "Unstable Release 112.0.1-bleeding-edge.1" or "CRP 1.4.2". The "bleeding-edge.2" version is missing all the resource definition files
4. As with the USI collection, open the archive, then move the CommunityResourcePack folder from the GameData folder in the archive to the KSP GameData folder (overwriting the CommunityResourcePack that came with USI)
5. I recommend you install the [Bon Voyage][BonVoyageAddon] addon, it will be very useful for managing rovers later (it will save you hours of driving rovers around, crashing them, and having to reload a save game)

As for where to find the KSP GameData folder, it depends on your platform, and how you installed KSP. Check out the [KSP Wiki page on where to find the "root" directory][KSPROOTDIR] -- the GameData folder is inside that "root" directory (it's not actually called "root" that's just another name for the "top level" directory, which is likely called "Kerbal Space Program").

But ultimately you'll have the KSP GameData folder in front of you, along with the USI and CRP archives open, and all you need to do is copy those add-on folders across:

![The Kerbal Space Program GameData folder is open with the USI archive and the CRP archive open alongside. There are two arrows, the first is labelled 1 and points from the USI archive pointing at the GameData window, and a second arrow labelled 2, pointing from the CRP archive to the GameData window][AddOnInstallation]

If you want to use the tutorial ships, get the [WOLF Tutorial Save][MRWOLFTS] release file and unpack it now. Put put the **Ships** and **Subassemblies** folders into your save directory.

![The Kerbal Space Program saves directory showing the WOLF Tutorial save folder. Alongside that is the WOLF_Tutorial_Ships ZIP file contents. An arrow indicates that the contents of the ZIP file should be dragged directly to the WOLF Tutorial save folder][TutorialShipsInstall]

Let's have a look at how WOLF biomes and production chains work. Create a new sandbox game. Ensure that when you create the game, under _Difficulty Options_ > _Advanced_, you **deselect** _Enable Kerbal Experience_.  This will give all of your Kerbals maximum experience.  Since Kerbal experience affects resource production, the rest of this tutorial will make more sense. For the rest of this walkthrough we'll assume you called your game "WOLF Tutorial".

## WOLF Biomes

The foundation of industry in WOLF is the "WOLF Biome" and its associated depot. The basic idea is that you dedicate a "WOLF Biome" to certain types of activity, and either transfer resources to other biome depots for further processing, or extract resources through WOLF "Hoppers" for use in the MKS industry that you're familiar with.

You can imagine WOLF Biomes as stuff that happens "behind the scenes" in the KSP world. You build up the industrial machinery to produce the goods that you need, hand that assembled factory to WOLF, then WOLF stops rendering those parts. The entire production line becomes an abstraction, with hundreds of parts abstracted away to a handful of numbers.

Where the world of MKS is concerned with resource concentrations, extractor efficiency, engineer multipliers and storage capacity, the world of WOLF is concerned with resource availability, expressed as one single number. Each WOLF biome has a certain availability for each resource. There are no concentrations to worry about, nor are there survey maps to ponder and prime locations to target for resource extraction. There's just a number for each resource in each biome.

The major catch with WOLF is that once you've committed to a certain production chain, there's no taking it back and making changes. With MKS infrastructure you can start producing Transport Credits then pivot to producing Material Kits and Specialised Parts by changing the recipes for a bunch of modules. With WOLF infrastructure, once you start producing something, that production chain will stay in place for the rest of your game.

## Surveying Harvestable Biome Resources

As soon as you start the new sandbox game, head to the SPH and build yourself a survey rover. If you're using the tutorial ships, use the **WOLF Depot Deployer** for this section. You'll need the **Surface Scanning Module** from the stock game. Here's my **WOLF Depot Deployer** which has a **Surface Scanning Module**, the **WOLF Transport Computer** which we'll discuss later, and the **Bon Voyage Autopilot** module (automatically incorporated into the controlling part) which I highly recommend (but more about that later).

![The WOLF Depot Deployer rover with important components marked: surface scanner, transport computer and bon voyage autopilot][WolfDepotDeployerParts]

<!--

+ Place the rover further down the runway from the touchdown markings.
+ Open and pin the PAW for the command seat ("Karibou Expedition Rover") to the left
+ Open and pin the PAW for the WOLF Transport Computer to bottom right
+ Open and pin the PAW for the Surface Scanning Module to top right
+ Aim camera down with front of rover away from camera

-->

Launch this vessel and open the **Surface Scanning Module** PAW (Part Action Window, aka right-click menu). You'll see the usual MKS resource details in the Surface Scanning Module's window. For each resource there's a concentration tagged "[Surf]" (because it's a resource on the surface) which is then combined with harvester efficiency to determine how much of that resource you'll be extracting per second using MKS parts. WOLF doesn't use that data.

Now open the **WOLF Dashboard** and select the _Harvestable Resources_ pane. You'll see that it's empty right now.

![WOLF Dashboard showing no biomes with harvestable resources][WolfDashboardHarvestableResourcesEmpty]

Looking back to the **Surface Scanning Module** PAW, there is one line under the MKS resources list specifying the "WOLF biome". You'll also see the "Survey WOLF Biome" action. Click it!

Recover this vessel.

## WOLF Dashboard -- Harvestable Resources and Depots

Now to check those resources. Switch scenes to the SPH and open the WOLF dashboard, then click the _Harvestable Resources_ button:

![SPH scene showing WOLF Dashboard open to Harvestable Resources pane][WolfDashboardHarvestableResourcesScannedBiome]

You'll have one Body/Biome option: Kerbin:KSC. There are four columns here which help you understand what resources you have access to:

1. Resource name, which represents the WOLF version of resources (as opposed to the "surface" resources)
2. Abundance, which is the WOLF equivalent to surface resource "concentration" (but it works completely differently)
3. Harvested, which is how much of the abundance you are currently extracting
4. Remaining, which is how much of the abundance is left to extract

The _Depots_ pane lists all your active WOLF Depots. Since you have no depots yet, it's empty.

![SPH scene showing WOLF Dashboard open to empty Depots pane][SPHWOLFEMPTY]

Now that the KSC WOLF Biome is surveyed, we need to deploy a WOLF depot. Before we do that though, have a quick look at the modules that make up the WOLF system, then we'll go over the rules of deploying them.

## WOLF Modules

From the SPH scene, start a new ship and open the _Planner_ pane in the **WOLF Dashboard**, and select the "WOLF" parts group in the selection pane on the left, then start planning this depot with a **WOLF Fabricator Module**. Set the **WOLF Fabricator Module** to produce _Material Kits_:

![SPH scene showing WOLF Dashboard open on Planning pane with a WOLF Fabricator Module as the first piece of the vessel under construction. The PAW shows Material Kits as the recipe.][SPHsceneFabricatorModuleWOLFDashboardPlanner]

There are two groups of values in the _Planning_ pane: the first is the _depot summary_ showing resources processed inside your WOLF Depot, the second is the harvestable resource report which shows the same details from the _Harvestable Resources_ pane but limited to those resources that you are actually harvesting with this depot. Since the fabricator you just added has not been configured it will be using the _Material Kits_ recipe. The _Planner_ now shows that you have a deficit of power, maintenance, technician crew point, chemicals, metals and polymers.

Add a _WOLF Maintenance Module_ and a _WOLF Power Module_. Now you'll see that you have surplus maintenance and power, but have incurred a deficit in various crew points. At this point, add a **Karibou Passenger Cabin** onto your WOLF modules to get 10 seats for crew and add an Engineer, Kolonist, Mechanic and Technician to your crew -- each crew member will add 10 crew points for their respective speciality. Add a probe core to the passenger cabin (I tend to use the _Avionics Package_ since it's small and cheap and provides all the necessary functionality). That's the crew points taken care of but now you have habitation and life support to worry about -- that's easily resolved by adding the **WOLF Habitation Module** and **WOLF Life Support Module**, leaving you with a deficit of food, oxygen and water (and the chemicals, metals and polymers for the fabricator).

Oxygen and water are available as _Harvestable Resources_ which means we can supply the depot with those resources using **WOLF MHU-550 Bulk Harvester** modules. Add two of those, configure one to harvest water and the other to harvest oxygen.

In the harvestable resource section of the planner you'll see that the harvesters are using 5 units each of the 1000 abundance of oxygen and 750 abundance of water, leaving 995 and 745 available. Note the numbers in the "Harvested" column: "0 (-5)" means that the KSC Biome Depot is currently harvesting 0 of that resource, and the craft that we are building will be harvesting 5 (thus reducing the abundance by 5).

Food is produced by an agricultural module or bioreactor module. Add a **WOLF Agriculture Module** and set it up to use the _Farm_ recipe. This has now added a demand for a farmer, dirt and fertiliser. Add a farmer to your crew, then you'll need three **WOLF MHU-550 Bulk Harvester** modules to get the dirt you need. To get fertiliser, we'll add a **WOLF MHU-559 Bulk Harvester** to harvest _gypsum_, then add two **WOLF Extractor Module** set to convert the _gypsum_ to _fertiliser_ (technically you only need one to feed the farm, but the harvester can feed two extractors). The two extractor modules have added a deficit for _Lab_ resource which is supplied by a **WOLF Science Module** so add one of those onto your growing pile of infrastructure, then add the scientist and medic crew that are needed for the science module.

Finally, add the harvesters and refineries required for the chemicals (feed stock is minerals), metals (feed stock is metallic ore) and polymers (feed stock is substrates). These modules have added demand for a _Miner_ crew member so recruit one of those and add them to the crew module. To finish off this infrastructure install add another **WOLF Power Module**, and you should no longer have any deficits in the _Planner_. **Note** that some of the _Material Kits_ produced by this infrastructure have immediately been consumed by other parts of the infrastructure (the habitation, life support and maintenance modules each consume 1 _Material Kits_ abundance). From the 5 _Material Kits_ produced by the fabricator, 3 have been consume by the depot infrastructure leaving 2 for use elsewhere.

Before we can deploy this infrastructure we need to establish the depot itself. To do this, add a decoupler and a **WOLF Depot Module** with a probe core. Note that this depot module, probe core and decoupler combination is going to be used so often that I prepared a subassembly for it -- check Subassemblies for _Depot on Decoupler_. When you launch this craft you'll decouple the depot, which needs control in order to be useful.

What a beautiful creation! Did yours turn out like mine?

![SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance][SPHSCENE2MATKITS]

If you're familiar with the production chains from MKS you'll see that this WOLF infrastructure is a lot simpler than what is required in MKS, for example each **WOLF MHU-550 Bulk Harvester** is roughly equivalent to a mining ship with a logistics hub attached to the planetary warehouse -- each of those mining ships will be a dozen parts given the need for drills, ore tanks, radiators, power source, probe core and whatever else you normally put on your mining ships. That part count can severely bulk out your save file size, and slow your game to a crawl any time you load a production facility into physics range. WOLF removes all that complexity from the save file and physics simulation -- including the need to visit facilities every so often to update the resource processing chains.

## Establish KSC Depot

Launch that craft you just created. You're going to separate the depot and immediately hand it over to the WOLF system.

**Warning**: Any other parts attached to the WOLF modules will be consumed along with the WOLF modules when you hand them over to the biome depot, including any crew. In addition the WOLF Depot can not have any other WOLF components attached, _not even the Survey Scanner_.

Now that you have your two-component craft separated (the WOLF Depot Module and a cheap probe core), it's time to establish your KSC Biome Depot:

![WOLF Depot Module with PAW showing "Establish Depot" action.][WOLFDEPOTPAWESTABLISH]

Just select the _Establish Depot_ action for the WOLF Depot Module, and the craft will disappear. It belongs to WOLF now.

That depot has given us 1 Food, 1 Oxygen, 5 Material Kits, 5 Water, and 10 Power. This will significantly reduce the amount of infrastructure we need to get started — but remember that these bonus resources only apply to WOLF biomes on Kerbin.

![Runway scene with WOLF Dashboard showing new production added][RUNWAYWOLFDASHNEWKSCDEPOTPRODUCTION]

## WOLF Infrastructure Expansion

**I highly recommend you get the Bon Voyage add-on**, it makes the process of deploying biome depots much, much easier.

To prepare for the next stage of the tutorial, let's expand the biome depots on Kerbin a little. To do that, we'll build ourselves a rover to help deploy the depot components. Why? Because sometimes the best way to get stuff to where you need it is to stick wheels or rockets on it.

![This assemblage of WOLF modules and wheels will make life easier for us, trust me][RUNWAYDEPOTBONVOYAGE]

The ingredients for this rover are:

- WOLF Depot Deployer Rover (based on the Karibou rover)
- DDR Basic Depot subassembly
  - Karibou Flatbeds containing WOLF modules attached to rover via Clamp-O-Tron Sr
  - WOLF Depot & probe core on a decoupler
- Engineer
- Kolonist
- Mechanic

Assemble those components in the SPH. **Remember to add the Engineer, Kolonist and Mechanic** (mentioned in the subassembly description) to the **Karibou Passenger Cabin in the trailer** before launching. The crew will be no use to you in the Karibou rover command seats.

Once you've launched the rover, activate the parking brake to stop it rolling down the runway, then activate Action Group 10 (press "0" on the keyboard) to turn on the power supply.

Use the **Bon Voyage** autopilot to send the rover to _Kerbin Shores_ (-0.04, -74.9). There is a list of locations like this at the end of this document, you might find it handy to keep a copy on hand. Activate the Bon Voyage autopilot and then change scene to the Space Centre. Wait for the rover to reach its destination -- warp can help here -- and then switch back to the rover.

The process for establishing a depot using this rover is:

1. lock the brakes on
2. scan the WOLF biome with the **Surface Scanning Module**
3. decouple the depot module and establish the depot
4. undock the trailer and connect it to the depot

![Kerbin Shores scene with WOLF Depot Deployer - Depot and trailer are decoupled and Surface Scanner PAW is open. There are numbers 1, 2 and 3 indicating the order of operations.][KERBINSHORESDEPOTDEPLOYMENT]

Once you have completed those operations you should see the new depot established in the **WOLF Dashboard** with the Mechanic, Kolonist and Engineer resources added:

![Kerbin Shores scene with WOLF Dashboard open to Depots pane showing new Kerbin Shores depot][KERBINSHORESDEPOTDASHBOARD]

Repeat this process to deploy this simple infrastructure to:

- Grasslands (0.0 -75.38)
- Highlands (1.741, -77.339)
- Mountains (0.637, -78.659)

Remember you can return to KSC at (-0.1, -74.647). There are more biomes to explore but between KSC, Shores, Grasslands, Highlands and Mountains there's more than enough to complete this walkthrough.

Remember the basic process for establishing a new biome depot is:

- Prepare the WOLF Depot Deployer rover with the DDR Basic Depot subassembly
  - Required crew is Engineer, Kolonist, Mechanic
- On the runway, lock the brakes and start the reactor (AG0)
- Move the rover to the new biome
- Survey the WOLF Biome
- Decouple the **WOLF Depot** component
- Use the _Establish Depot_ action on the **WOLF Depot**
- Undock the **DDR Basic Depot** assembly
- Use the _Connect to depot_ action on the **Tutorial Basic Depot** assembly
- Switch vessels to the rover (your previously active vessel was destroyed as part of establishing the depot)
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer**
- Move the rover back to the KSC
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer**
- Recover the rover

![Use the connect to origin depot action on the WOLF Transport Computer before departing the remote biome][MountainsDepotDeployerConnectOriginDepot]

![Use the connect to destinationi depot action on the WOLF Transport Computer after arriving at KSC][KSCDepotDeployerCoonectDestinationDepot]

If you want to know what's going on with the **WOLF Transport Computer**, check out the section on **WOLF Routes**. The executive summary is that you're setting up routes between depots over which you'll later be establishing resource transfers -- routes are like railways, transfers are the trains.

## Adding Production to WOLF Depots

The aim of our activities here is to establish an orbital ship yard and build spacecraft in orbit to further expand the WOLF infrastructure to other worlds. To build spacecraft at the orbital shipyard, you'll need _Material Kits_, _Specialized Parts_, _Alloys_, _Electronics_, _Prototypes_, _Robotics_ and _Synthetics_.

Let's start with the _Alloys_, building a _WOLF Depot Deployer Rover_ trailer from scratch. To start with just assemble a **Karibou Passenger Cabin** and **Karibou Flatbed Wheel Bay**, add some wheels and an avionics package (this starting trailer is available as **WOLF Depot Deployer Trailer** in the subassemblies listing). Add a **WOLF Fabricator Module** and set its recipe to _Alloys_. Now you have a deficit of _Rare Metals_, which are collected by a harvester module. Add a **WOLF MHU-500 Bulk Harvester** and set its recipe to _Rare Metals_. There's a deficit of _Rare Metals_ in this biome, so check through the remaining depots to see if you can find _Rare Metals_.

Unfortunately, it turns out that _Rare Metals_ are not a thing in Kerbin biomes. Okay, what about the others? _Electronics_ requires _Synthetics_ which in turn requires _ExoticMinerals_ ... which it turns out are not available on Kerbin either. Maybe _Prototypes_ then? No, they require _Electronics_ which we can't manufacture in WOLF on Kerbin. _Robotics_ are in the same boat, requiring _Alloys_. Last on the list are _Specialized Parts_ but it turns out that they require _Refined Exotics_ (_Rare Metals_ and _Exotic Minerals_).

The only spaceship-building things we can make on Kerbin using WOLF infrastructure are _Material Kits_ and _Fuel_. What do we do about the rest? For the boot-strapping stage, any time we need _Specialized Parts_, _Alloys_, _Electronics_, _Prototypes_, _Robotics_ or _Synthetics_ the options are to buy them (create a new craft with a resource container full of the resource we're after), set up WOLF infrastructure where we _can_ find them and transport the supplies to the shipyard, or find some surface resources to extract and perform all the industry using MKS.

For this walkthrough we're not going to go overboard with production, and as far as the other spaceship building materials go we'll simply buy them. Tens of abundance for _Material Kits_ and _Fuel_ will be enough to get us to Minmus where we'll find the resources that Kerbin doesn't have itself. Along the way we'll also produce _Fertilizer_, _Food_, _Oxygen_, and _Water_ to reduce the amount of infrastructure we need to establish on Minmus at the start.

Clear the SPH build area and load up the **WOLF Depot Deployer Rover**, add the **DDR 5 Material Kits** subassembly, put a Miner and a Technician in the passenger cabin (as indicated in the subassembly description), and check the _Planner_ pane of the **WOLF Dashboard** to see which biome will have the most resources left over after we commit to this _Material Kit_ production. For me this is the Mountains biome which had 100 _Minerals_ abundance before this infrastructure took 10 away. Launch the rover and send it to the Mountains biome (0.637, -78.659).

Here's what the **WOLF Depot Deployer Rover** with **DDR 5 material Kits** subassembly and the required crew should look when you're ready to launch:

![SPH scene with DDR rover and attached DDR 5 Material Kits subassembly][SPHDDRMaterialKitsAndCrew]

As is usual with the Depot Deployer Rover:

- move the rover to the destination biome
- undock the trailer and connect that to the depot
- connect the transport computer to the "origin" depot
- send the rover back to KSC
- connect the transport computer to the "destination" depot
- recover the vessel

You should be able to send one of these **DDR 5 Material Kits** trailers to each of the biomes, and a second one to the _Mountains_ biome.

One that is done, send a Depot Deployer rover with the **DDR 20 Fuel** subassembly to the Shores biome and deploy it there.

Now send the **DDR 20 Food** subassembly to the Grasslands biome and deploy that.

Finally send the **DDR Life Support** subassembly to the Shores and deploy that.

To recap:

- DDR 5 Material Kits expansions deployed to
  - KSC
  - Shores (-0.04, -74.9)
  - Grasslands (0.0 -75.38)
  - Highlands (1.741, -77.339)
  - Mountains (0.637, -78.659) (expand to 20 material kits)
- DDR 20 Fuel expansion deployed to Shores
- DDR 20 Food expansion deployed to Grasslands
- DDR Life Support expansion to Highlands

Return the rovers to KSC right next to Kerbal centre (-0.1, -74.647). The extra infrastructure for the Mountains depot will require an extra maintenance module and power module -- I added these by copying the rear-most Karibou Flatbed Wheel Bay, removing the WOLF modules from it then adding the power and maintenance modules on top.

If you have trouble with the rover endlessly bouncing, check out the **Route Builder Rover** section below. There is a trailer subassembly that you can use the same way as the DDR trailers, with a prebuilt subassembly for 20 fuel production (RBR 20 Fuel). The Route Builder Rover is slow, but it will get the job done until you run into issues with Kraken vs Bon Voyage.

After all that effort the _Depots_ tab of your **WOLF Dashboard** should look something like this:

![SPH scene with WOLF Dashboard showing material kits and fuel production from KSC, Shores, Grasslands, Highlands and Mountians][SPHWOLFDASHSTARTERPRODUCTION]

## WOLF Routes

It's all well and good having that _Material Kits_ production chain set up in the mountains, but what do we do with the output? At present all of this work has set up _abundance_ of certain resource types in the invisible world of WOLF. Eventually you'll pull resources out of WOLF into the MKS world.

The next step on the way from WOLF production to MKS extraction is getting those WOLF resources to orbit, where we want to use Material Kits and other resources to build spaceships. The immediate progress we need to make is _transferring__ the resources from the WOLF depots to the KSC and then _transferring_ them to orbit over WOLF _routes_.

WOLF handles transport of resources from one biome to another by way of _routes_ which are paths established for _transfers_ to move over -- conceptually, routes are a railway and transfers are the regular trains on that railway. You establish a route by travelling between biomes using the **WOLF Transport Computer** to connect origin and destination depots, with the capacity of the route determined by the **WOLF Cargo Kontainers** attached to the rover. Moving a rover between origin and destination depots with the transport computer tracking the trip will add _Route_ between the source biome and the destination biome with a certain _cargo space_.

You already have some routes established as part of the initial deployment of WOLF depots with the WOLF Depot Deployer, here's what they look like in the _Routes_ pane of the **WOLF Dashboard**:

![SPH scene with WOLF Dashboard showing the Routes pane][SPHWOLFDASHROUTESPANE]

This panel is showing us that there are routes between specific origin and destination biomes that have a certain capacity in units of _Cargo Space_. You can then create _Transfers_ on that route, which we'll get to in the [WOLF Transfers](#wolf-transfers) section below.

Note that with 20 _Fuel_ abundance we'd have to run the rover back and forth 7 times. That seems a lot like hard work so let's cobble together a rover with three of the largest WOLF payload Kontainers and call it the **WOLF Route Builder Rover**.

### Route Builder Rover

This rover has 45 payload capacity so it'll build these routes quite quickly. It also has a trailer subassembly so if you were having trouble with the **WOLF Depot Deployer** due to the weight of the payloads it was hauling (I sometimes had problems with wheels popping or suspension bouncing) give this route builder rover a try.

![SPH scene with WOLF Route Builder Rover][SPHRouteBuilderRover]

<!--
Label this image with:

1. Nuclear reactor and radiator (AG0)
2. Descent and flight core (AG9)
3. Surface operations core (AG8)
4. Surface Scanning Module
5. Bon Voyage controller
6. WOLF Transport Computer

-->

I put the light mast on top to light up the terrain so that the rover is usable at night (especially useful on Mun where night time lasts 3d), and it helps when landing other spacecraft nearby. The mast has two lights to illuminate the rover itself so you can see the controls at night. It also has landing rockets so you can build this rover in orbit and land it on Minmus, Mun, Duna or Ike (but more about all that later). This rover can not land on Kerbin or Eve without assistance.

Take this **WOLF Route Builder Rover** rover out to each of the biomes to build a route from KSC to the biome, then from the biome back to KSC. That should keep you covered for the entire walkthrough. The procedure for building these routes with the tutorial rovers is:

- Launch the rover from the SPH
- On the runway, lock the brakes (icon in the HUD) and start the reactor (AG0)
- Activate the driving probe core (AG8) -- double-check that the artificial horizon shows the horizon with sky above, ground below
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer**
- Move the rover to the remote biome
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer** to complete this route
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer** to start a new route
- Move the rover back to the KSC
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer** to complete that route
- Repeat this process as often as you need

Here's one I prepared earlier (just a bunch of routes with a decent amount of payload capacity):

![KSC scene with WOLF Dashboard open to the Routes pane][KSCRouteBuilderRoutesBuilt]

## WOLF Transfers

In this walkthrough the main purpose of setting up these biomes is to get Material Kits and Fuel to orbit to start building spaceships. There are no doubt untapped opportunities in your biomes (eg: the ability to send one resource from a biome with excess to another biome with a deficit), but for now we have plenty of output to get to orbit.

To get the food, fuel and material kits from the various biome depots to orbit, first we need to get them to the launch site. This means setting up resource transfers over the established routes. To establish a resource transfer open the **WOLF Dashboard** to the _Routes_ pane. Select the _Manage Transfers_ button which will show you the _Manage Transfers_ interface:

![SPH scene with WOLF Dashboard showing the Manage Transfers interface][SPHWOLFDASHMANAGETRANSFERS]

This dialog is use to set up resource transfers over a route. The numbers visible in this dialog show:

- The resources and their abundance at the source biome depot
- The selected resource
- The abundance of that resource in the source biome depot
- The current available/incoming values of the resource in the destination biome
- The list of resources that you have already selected for transfer on this route
- How much payload capacity is left for transfers
- How much payload capacity has already been used

How much of a resource you can add to transfers on this route is the smaller number of the abundance of the resource or the available payload. In the example above there are 20 Material Kit points available, and the payload of 45 has space for all of them with room to spare.

When you request a new transfer you'll allocate an _abundance_ of resource to a transfer, then the _abundance_ of that resource will be reduced in the source biome and increased in the target biome, and the route will have a new _Transfer_ using up some of its capacity.

To transfer resources select the resource in the top pane, enter the abundance you wish to shift between depots in _Transfer Amount_ then select _Transfer_. Do that now to move 5 Material Kits from the Mountains depot to the KSC depot:

1. Open the **WOLF Dashboard** to the _Routes_ pane
2. Click _Manage Transfers_  to open the _Transfer Resources_ interface from the _Routes_ pane of the **WOLF Dashboard**
3. Select "Kerbin:Mountains => Kerbin:KSC" from the dropdown at the top (the left/right arrows will help when your list is too long to fit on the screen)
4. In the list of resources, select the down-pointing triangle next to _MaterialKits_
5. Set _Transfer Amount_ to 6
6. Click _Transfer_
7. You should see the lower pane update with the new transfer of 6 _MaterialKits_ over this route
8. _Close_ the _Transfer Resources_ window

Here's the _Transfer Resources_ window with the new transfer set up over the Mountains to KSC route:

![KSC scene with Transfer Resources interface showing a new transfer of 6 MaterialKits from Mountains to KSC][KSCTransferMaterialKitsMountainsToKSC]

Set the _Transfer Amount_ to 1, then click _Transfer_. You should notice:

- The "Origin" abundance will drop by 1
- The "Destination" abundance will increase by 1
- The "Available Payload" will drop by 1

You'll see a new row in the bottom table displaying the transfer you've just organised. Add another transfer of 5 _Material Kits_, and you'll see the row in the bottom table updated to show the new _Material Kits_ quantity.

Now click the "X" next to that 6 Material Kits transfer in the lower pane, and the abundance in the source depot will be restored along with the available payload.

Now set up the Material Kits transfer to move:

- 20 Material Kits from the Mountains depot to the KSC depot
- 20 Food from the Grasslands depot to the KSC depot
- 20 Fuel from the Shores depot to the KSC depot
- 20 Water from the HIghlands depot to the KSC depot

Close the _Transfer Resources_ window.

The _Routes_ pane of the **WOLF Dashboard** will now show the resources being transferred between the various biomes and the KSC. In my example I've set up the production, routes and transfers to provide 20 surplus _Material Kits_ and 20 surplus _Fuel_ for the KSC depot. I want to get that _abundance_ to Kerbin orbit, so it's time to talk about transport credits which should be familiar to people who have used MKS in the past, and then we can talk about how to get _abundance_ out of the WOLF system and turn it into materials for MKS activities.

Here's what my transport routes look like with the depots transferring some resources to KSC:

![KSC scene with WOLF Dashboard showing transfers from highlands, mountains and shores to KSC][KSCTransfersFromHighlandsMountainsShores]

If you have more Material Kit, fuel, water and food abundance than will fit in the payload, you can simply connect the route more times with your route-building vehicles to increase the payload size.

The small portions of abundance that we have produced and transferred will be adequate for the rest of the walkthrough. Feel free to expand your depots by adding more production modules, adding more payload capacity to the routes using the route builder rover, and transferring the extra abundance to KSC.

## Transport Routes and Transport Credits Costs

Up till now we've kept the transport routes simple by only connecting biomes that can be reached with electric rovers. It's time to kick it up a notch and learn about Transport Credits, which is an abstraction of the process of building launch vehicles, fuelling them and launching payloads to orbit (or deorbiting payloads to bring them to the surface). Transport Credits also represent an abstraction of building and fuelling tugs and freighters that operate between worlds -- basically any transfer that involves the consumption of stuff (rocket stages, propellant, etc) is abstracted to Transport Credits.

The first thing we'll do here is a few test flights to understand how many _Transport Credits_ we'll need for sending supplies to orbit (or roughly, how Transport Credits correlate to delta-v and ship size), and then we'll have a look at an optimisation that will reduce Transport Credit cost to 0. Let's start with a small rocket, a medium sized rocket, a 3t payload SSTO spaceplane, and a 55t payload SSTO spaceplane. With enough Transport Credits each flight will add a certain payload capacity to the available routes from KSC to Kerbin Orbit, with the payload capacity being determined by the _WOLF Cargo Kontainers_ on each launch vehicle. We'll get the gory details soon!

### Quick and Dirty Transport Credit Example Flights

**Save your game here**, give it a name like "Before Transport Credits". Skip ahead to the next section (_Extracting Resources from WOLF to MKS_) if you don't want to learn about transport costs and how to avoid them. You're going to be restoring to this point after experimenting with _Transport Credits_, and through the rest of the walkthrough there will be no transport costs other than the time it takes to set them up.

In the VAB, put together a rocket that can carry a single 3t **2.5m WOLF Cargo Kontainer** to orbit using 2.5m parts. The *_WOLF Tutorial 2.5m SSTO_ contains:

- 2.5m WOLF Cargo Kontainer
- RC-001S Remote Guidance Unit
- Protective Rocket Nosecone Mk7
- Rockomax Jumbo-64 Fuel Tank
- RE-I5 "Skipper" Liquid Fuel Engine
- WOLF Transport Computer

Send that to the launch pad, select the _Connect to Origin Depot_ action on the **WOLF Transport Computer**, and launch the rocket to a 80km orbit.

![Connect the WOLF Transport Computer to the origin depot before launch][SmallSSTORocketStartRouteAtLaunch]

Once in orbit, check the "Route cost" reported by the **WOLF Transport Computer**.

If you try to use the **Connect to Destination Depot** action, you should get an error message about needing more Transport Credits to complete that operation. Revert to launch, and run it a few times just to see that the "Route cost" is predictable. My flights came up with a route cost of 30 _Transport Credits_ which works out to a _Credits/Payload_ cost of 10.

![Sample flight of 2.5m rocket showing a route cost of 30][SmallSSTORocketRouteCost30]

Revert to vehicle assembly and do the same thing with a 3.75m rocket. The _WOLF Tutorial 3.75m SSTO_ is roughly:

- 2 x 3.75m WOLF Cargo Kontainer
- Protective Rocket Nosecone Mk7
- RC-L01 Remote Guidance Unit
- Advanced Reaction Wheel Module, Large
- WOLF Transport Computer
- Kerbodyne S3-14400 Tank
- S3 KS-24x4 "Mammoth" Liquid Fuel Engine

Send that to the launch pad, select the "connect to origin depot" on the WOLF Transport Computer, and launch the rocket to an 80km orbit. As before, check the "route cost", revert to launch and run the process again to show that the "route cost" is predictable. My flights came up with a route cost of 80-ish, giving a _Transport Credit Per Unit_ cost of around 6. Revert to vehicle assembly when done.

![Sample flight of 3.75m rocket showing a route cost of over 80][KERB375ROCKETCREDITS]

Now do the same thing with spaceplanes. The two I use are the **WOLF SSTO** and the [ES-96 Python by Juggernoob](https://steamcommunity.com/sharedfiles/filedetails/?id=1722161481) which I find to be aesthetically pleasing and easy-to-fly SSTO spaceplanes.

**Instructions:** for both these spaceplanes the procedure to get to orbit is:

- set throttle to maximum
- turn SAS on to stability assist
- stage once to light the engines
- rotate off the runway to 10 degrees at about 140m/s and immediately retract landing gear
- hold the nose at 10 degrees for the whole flight through the atmosphere
- when the airbreathing mode is insufficient to keep accelerating, switch to closed cycle (Action Group 1)
- push the apoapsis to 80km and cut the throttle
- cruise to the top of the atmosphere, plot a circularisation burn at apoapsis
- execute that burn.

My flights with **WOLF SSTO** ended up producing routes with a cost of 9 for 3t cargo, or about 3 credits/unit.

![Sample flight of WOLF SSTO showing route cost of 8 for 3t cargo][SSTORTCOST8]

The **ES-96 Python** got to orbit in the order of 80 to 90 Credits for 42t. The **WOLF ES-96 Python** in the tutorial ships package has already been modified and will automatically start the transport route when you stage to launch (the **Transport Computer** is in the cargo bay with the _Connect to origin depot_ action linked to the _stage_ action group).

![Sample flight of WOLF ES-96 PYTHON showing route cost of over 80 for 42t][ES96RTCOST85]

### Transport Module for Transport Credits

How do we produce Transport Credits? The short version is that _Transport Credits_ are produced by the _WOLF Transport Module_. By now you should be familiar with the drill: start assembling a new WOLF infrastructure component with the WOLF Dashboard open to the Planning pane, beginning with the WOLF Transport Module. Fuel is produced by the Fuel(Ore) or Fuel(H2O) recipes in the WOLF Refinery Module — each recipe will take 5 points of input availability and provide 2 points of Fuel availability. As usual one harvester will provide sufficient Ore or Water for two refineries.

The "atomic" component of a Transport Credit production line is 1 Transport Module (producing 10 _Transport Credits_ from 10 _Fuel_), 3 MHU-500 harvesters (_Water_), and 6 Refinery Modules (producing 2 _Fuel_ from 5 _Water_) this needs to be supplemented with 1 abundance of _Material Kits_. To produce the target of 100 Transport Credits to get our _Fuel_ and _Material Kits_ to orbit we need to start off with:

- 10 x WOLF Transport Module
- 30 x MHU-500 harvesters (harvesting water)
- 60 x WOLF Refinery Module (producing fuel from water)
- local or imported abundance of 10 x Material Kits

Then you add all the habitation, power, maintenance and other infrastructure required to support this.

![VAB showing the ridiculous WOLF infrastructure required to produce 100 transport credits][VABWOLFTutorial100TransportCredits]

One catch with _Transport Credits_ is that you can't deliver them elsewhere: they can only support the establishment of routes from the biome which they're produced in. Thus to use _Transport Credits_ to fund transfers from KSC to Kerbin Orbit, you need to deploy this infrastructure at KSC.

### How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles

Now that you've gone to the effort of figuring out that Transport Credit infrastructure, I have a confession to make: you can make the system work to your advantage and completely eliminate the Transport Credit cost of these route-building flights.

How? Put a propellant depot in orbit, fly your transport vehicle to that depot and refuel before connecting the **WOLF Transport Computer** to the destination depot. Because the transport cost is calculated based on the difference in mass between the start and the end of the transport route, if you can restore all the consumed mass you can get a transport route that costs 0 _Transport Credits_. This is how you'd do it if you had an established MKS or stock infrastructure (for example exporting propellant from Minmus to Kerbin orbit), flying your freighter to the destination and refuelling to get it back to the origin port.

Here's the **WOLF SSTO** at the end of a 3t haul to orbit having just refuelled. How many transport credits to fly 3t to orbit? 0. Let's make this work for you!

![WOLF SSTO in Kerbin orbit with Kerbin Shipyard in background and WOLF Transport Computer action window showing route cost 0 and route payload 3][WOLFSSTO0CREDITS]

**Go back and load your "Before Transport Credits" save game**.

## Bootstrapping Kerbin Orbit WOLF Infrastructure

Load the **WOLF Shipyard Launcher** that you'll find in the VAB from the tutorial ships package, under the **WOLF Tutorial Shipyard** folder. Launch that shipyard to an 80km orbit, undock the **WOLF Depot** component and establish the orbital depot.

Now to expand on this shipyard to provide a propellant supply and the ability to construct spacecraft for the expansion to Minmus and Mun. To start with, let's add a propellant supply to the shipyard. To accomplish this:

- supply the 4000 Material Kits required to deploy the shipyard
- supply the MKS resources (other than Material Kits) required to build the _Fuel Hopper_ shipyard component
- supply the propellant required to refuel a route builder
- build a route to provide WOLF MaterialKits that the shipyard
- extract the WOLF Material Kits to MKS Material Kits that the shipyard can use (this will be the focus of the following section)

The WOLF ES-96 Python will need around 15,000 fuel and oxidizer to replenish at the end of its run. One option is to send up a large tanker with the required propellant. Check out the **Shipyard Bootstrap** vessel under the **WOLF Tutorial Shipyard** folder. This will bootstrap the Kerbin Shipyard, and allow you to establish a route from KSC to Orbit:

1. Launch **Shipyard Bootstrap**
7. Rendezvous **Shipyard Bootstrap** with **Kerbin Shipyard**
8. Transfer propellant to the shipyard
9. Send **Shipyard Bootstrap** to a parking orbit, you can use it to top up the shipyard later
10. Launch the **WOLF ES-96 Python**
11. Rendezvous **WOLF ES-96 Python** with the **Kerbin Shipyard** and refuel it
12. Establish route to orbit
13. Transfer propellant back to the **Kerbin Shipyard** and leave the Python only enough propellant to de-orbit and fly back to KSC (about 300m/s)
14. Return WOLF ES-96 Python to KSC (you can build a route on the way back, as long as you have a way to refuel after landing)

The shipyard will also need advanced MKS materials which we are not producing yet. As you might expect, there's already a craft available to deliver the advanced construction materials that will be required. Look at the **Advanced Materials Delivery** craft, which will deliver the following in about the proportions required:

- Specialized Parts
- Alloys
- Synthetics
- Robotics
- Electronics

One of these will bootstrap the Kerbin shipyard, then a second will bootstrap the Minmus shipyard later. After that all the resources will be produced through WOLF infrastructure and expansion to other worlds becomes much easier. For the immediate mission:

1. Launch the **Advanced Materials Delivery** rocket
2. Rendezvous **Advanced Materials Delivery** with **Kerbin Shipyard**
3. Transfer the resources from **Advanced Materials Delivery** to **Kerbin Shipyard**
4. Deorbit **Advanced Materials Delivery**.

With all that work taken care of, it's time to commission the shipyard!

## Commission Kerbin Shipyard

To commission the Kerbin Shipyard, you need to complete these tasks:

1. Transfer Material Kits and Fuel from KSC depot to Kerbin Orbit depot
2. Connect the Material Kit hoppers on the shipyard to the depot
3. Build the **Fuel Hopper** expansion for the shipyard
4. Connect the **Fuel Hopper** to the depot

With the propellant handling in place, you can rendezvous further route-building craft with this shipyard to refuel (for example the **WOLF SSTO** or **WOLF ES-96 Python**), and start building your orbital industry from there.

 ![WOLF ES-96 Python in Kerbin orbit with just-launched Kerbin Shipyard in background, WOLF Transport Computer action windows showing route cost 0]()

Keep expanding the route between KSC and Kerbin Orbit to 100 units. Three flights of the Python should be plenty:

- 20 fuel
- 20 material kits
- 20 water
- 20 oxygen
- 20 food

As you did the last time when setting up transfers over a route:

1. Open the **WOLF Dashboard** to the _Routes_ pane
2. Click _Manage Transfers_  to open the _Transfer Resources_ interface from the _Routes_ pane of the **WOLF Dashboard**
3. Select "Kerbin:KSC => Kerbin:Orbit" from the dropdown at the top (the left/right arrows will help when your list is too long to fit on the screen)
4. In the list of resources, select the down-pointing triangle next to _MaterialKits_
5. Set _Transfer Amount_ to 20
6. Click _Transfer_
7. You should see the lower pane update with the new transfer of 20 _MaterialKits_ over this route
8. Repeat steps 4-6 for fuel, water and food
9. _Close_ the _Transfer Resources_ window

![WOLF Dashboard open to the Routes pane. Transfer Resources dialog is open, showing a transfer of material kits and fuel from the KSC depot to the Kerbin Orbit depot][KERBYARDTRANSFERS]

With those transfers organised, it's time to extract the WOLF resources into the MKS industry system. This is done using the various hoppers on the Kerbin Shipyard.

## Extracting Resources from WOLF to MKS

Now open the **WOLF Dashboard** to the _Depots_ pane, expand the _Kerbin: Orbit_ depot so you can watch the figures while we configure the propellant depot, and set the hopper up:

 1. Open a _Material Kits_ Manufacturing Hopper's PAW (for this we want the PAW and the WOLF Dashboard open)
 2. Click _Connect to depot_
 3. Click _Start hopper_

Observe that the abundance of a resource will be reduced the moment you connect the hopper to the depot, regardless of whether or not the hopper is running. Here's what it should look like for you now:

![At the shipyard in orbit, WOLF Dashboard is open to the Depots pane and the Kerbin: Orbit depot is expanded to show the incoming/outgoing/available resources. There are Material Kits outgoing to service the connected manufacturing hopper. The PAW for the manufacturing hopper is open showing the "Disconnect from depot" and "Stop hopper" buttons.][KERBYARDMATKITHOPPERSTART]

While you are here, keep the **WOLF Dashboard** open and see what happens when you stop the hopper and disconnect it from the depot. What you should see happen is that the local resource production will stop when you stop the hopper, and the abundance of the resource in the Kerbin Orbit depot of the **WOLF Dashboard** _Depots_ pane will be deducted from _Outgoing_ and added to _Available_. When you're ready, reconnect the hopper and start it up again.

Now connect and start the other _Material Kits_ hoppers. The combined output of three 3.75m Manufacturing Hoppers will be 15,000 _Material Kits_ a day. We'll need 34,782 for the next step. The fourth hopper is configured for Specialized Parts, which are not available yet.

## Establishing the Kerbin Shipyard

Now that resources are flowing to the shipyard, wait until there are 35,000 _Material Kits_ available and build a _Fuel Hopper_ which you will find in the _WOLF Tutorial Shipyard_ folder:

1. Open the Konstructor's PAW (right-click menu)
2. Select _Open Konstructor_
3. From the _Konstructor_ window select _Select a ship_
4. From the vessel selection dialog open the _WOLF Tutorial Shipyard_ folder and select _Fuel Hopper_
5. Verify that you have all the materials required to build the _Fuel Hopper_
6. Select _Build_
7. After a brief delay the _Fuel Hopper_ will pop into existence and control will be transferred to the new vessel
8. Transfer monopropellant from _Kerbin Shipyard_ to the _Fuel Hopper_ using the MKS _Transfer Resources_ window (forklift icon)
9. Dock the _Fuel Hopper_ with the ship yard. The red/green navigation markers are mounted "forward" of the Clamp-O-Tron Sr to help you orient the vessels neatly
10. Open the PAW on one of the WOLF Fuel Hopper modules
11. Click _Connect to depot_
12. Click _Start hopper_

As with the _Material Kits_ in the manufacturing hoppers, you should see the depot's abundance of fuel drop by 5 to service this hopper. Each Manufacturing Hopper configured for Material Kits will produce 5000 Material Kits per day.

Connect the remaining Fuel Hopper modules to the depot and start them. Each Fuel Hopper configured for LF/Ox will produce 450 LF/day and 500 Ox/day.

Here's a finished Kerbin Shipyard, ready to start the next phase of expansion:

![Assembled Kerbin Shipyard showing shipyard component and fuel hopper docked in orbit][KERBYARDCOMPLETE]

# Minmus Shipyard

To establish the Minmus shipyard the basic steps are:

1. Build an **Expansion Shipyard**, fill it with propellant and launch it to Minmus -- on arrival, place it in a 20km circular orbit
2. Launch a new **Advanced Materials Delivery** rocket and send it to Minmus
3. Build the **Orbital Route Builder 15LR** and launch it to Minmus (NB: Transport Computer is on the "top" face of the vessel, only supply 50% propellant load)
4. At Minmus, rendezvous the **Orbital Route Builder 15LR** with the **Expansion Shipyard** and refuel it to complete that route
5. Build a new route from Minmus Orbit to Kerbin orbit using the **Orbital Route Builder 15LR** (keep this craft going back and forth to build up 60 route capacity from Minmus to Kerbin)
6. At Minmus, rendezvous the **Advanced Materials Delivery** with the **Expansion Shipyard** and transfer the resources. Dispose of the **Advanced Materials Delivery** as you see fit.
7. Transfer bootstrap WOLF resources (Fuel, Material Kits, Water, Oxygen, Food) to Minmus over the new routes
9. When **Minmus Shipyard** has 4000 _Material Kits_, deploy the _Konstructor_

Let's go through that now. If this list has enough detail for you, work through it and skip to the section **Minmus Expansion**.

## Minmus Expansion Shipyard

The **Expansion Shipyard** requires approximately the following materials:

- 125,000 Material Kits
- 942 Specialized Parts
- 263 Alloys
- 533 Synthetics
- 63 Robotics

There are sufficient advanced materials remaining from the original delivery, so you'll just have to wait the 10 days for the required quantity of Material Kits to arrive. It will take about 16 days to produce the propellant required for the Expansion Shipyard too. You can speed this up by adding another _Fuel Hopper_ and _Manufacturing Hopper_ assembly to the **Kerbin Shipyard** along with the necessary Kerbin-based production, routes and transfers. For the purpose of the walkthrough, just "warp to next sunrise" 16 times to produce the required material kits and propellant.

Once you have the materials, build the **Expansion Shipyard**, fill it with propellant and send it to **Minmus**.

When the **Expansion Shipyard** arrives at **Minmus**:

- Place the **Expansion Shipyard** in a 20km circular orbit
- Undock the _Depot_ module at the front (it's attached via the Clampotron)
- Switch to the _Depot_ spacecraft
- Select _Establish Depot_ from the depot module's PAW

At this point, return to the KSC and launch the **Advanced Materials Delivery** craft. Send it to Minmus to rendezvous with the **Minmus Shipyard**. Transfer the advanced resources to the shipyard, then land the **Advanced Materials Delivery** on the _Greater Flats_ for use as a fuel depot later.

Now return to the **Kerbin Shipyard** and build the **Orbital Route Builder 15LR**. The **Orbital Route Builder 15LR** requires 31335 _Material Kits_ (2 days production) and 6480 _Liquid Fuel_ (4 days production):

- Start a cargo route and send the **Orbital Route Builder 15LR** to **Minmus**
- At **Minmus**, rendezvous the **Orbital Route Builder 15LR** with **Minmus Shipyard**
- Refuel and complete the route
- Now transfer some basic resources to Minmus for the **Minmus Shipyard**: 5 Fuel and 10 Material Kits
- Start a cargo route and send the **Orbital Route Builder 15LR** back to **Kerbin Shipyard**

The **Orbital Route Builder 15LR** should be sent back and forth a few times to build up around 60 units of route capacity in each direction. This is to cater for some materials that we will be sending to Minmus to bootstrap the infrastructure, and then to cater for resources returning to Kerbin from Minmus as Minmus industry is established.

With 10 Material Kits abundance being extracted, **Minmus Shipyard** will be producing 10,000 _Material Kits_ per day. When there are 4,000 _Material Kits_ available, ,deploy the _Konstructor_.

Now **Minmus Shipyard** has been established, it's time to expand our WOLF infrastructure to **Minmus** itself.

## Minmus Expansion

At this point you should be familiar with:

- Establishing WOLF biome depots
- Establishing routes between WOLF biome depots using a rover
- Configuring resources transfers over routes
- Configuring WOLF resource hoppers to convert WOLF resources to MKS resources

What comes next is learning how to wrangle the armies of Kerbals that will be required to operate the WOLF infrastructure on Minmus. But first, let's find what resources are available on Minmus.

Some things to consider for Minmus: first is that the expansion will be strapped for resources. After this infrastructure is in place we'll have the resources required to bootstrap a new world without any stress. For Minmus we're starting with a fixed amount of resources from one shipment and boot-strapping the infrastructure to support a shipyard.

Secondly, I've found Minmus hostile to rovers. My rovers will slide forever while a regular lander sits a little awkwardly on a slope. There are currently issues with the wheels on the USI rovers (Malemute and Karibou) so you can't manually drive them anywhere, and the same slipping and sliding issues affect them anyway.

What I have found easiest for Minmus is using rockets to drop depot expansions onto the surface from orbit. We'll also be shipping crew in from Kerbin, since WOLF requires a significant investment in infrastructure to transport crew (we'll get to that for the Mun expansion).

Resource production required to supply **Minmus Shipyard** will be the minimum required to run 3 x 3.75m _Material Kits_ hoppers and 1 x 3.75m hopper of each remaining building material excluding Prototypes. Here's a summary list, pardon my shorthand in the brackets. The shorthand "Chemicals x 25 (1 x 25)" means "we need 25 chemicals, which is 1 per Material Kit production, and we're producing 25 Material Kits."

1. Material Kits x 25 (15 for station + 5 for electronics + 5 for robotics)
   - Chemicals x 25 (1 x 25)
   - Metals x 50 (2 x 25)
   - Polymers x 50 (2 x 25)
2. Specialized Parts x 5
   - Refined Exotics x 10 (2 x 5)
     - Exotic Minerals x 20 (2 x 2 x 5)
     - Rare Metals x 30 (3 x 2 x 5)
   - Silicon x 15 (3 x 5)
3. Alloys x 6 (1 for station + 5 for Robotics)
   - Metals x 6 (1 x 6)
   - Rare Metals x 24 (4 x 6)
4. Synthetics x 6 (1 + 5 for Electronics)
   - Exotic Minerals x 24 (4 x 6)
   - Polymers x 6 (1 x 6)
5. Electronics x 1
   - Material Kits x 5
   - Synthetics x 5
6. Robotics x 1
   - Alloys x 5
   - Material Kits x 5

The sum total thus becomes:

- Chemicals x 25 (only for MK)
- Exotic Minerals x 44 (20 for SP + 24 for Synthetics)
- Metals x 56 (50 for MK + 6 for Alloys)
- Polymers x 56 (50 for MK + 6 for Synthetics)
- Rare Metals x 54 (30 SP + 24 for Alloys)
- Silicon x 15 (only for SP)

This will be enough to support production up until around the point we have a thousand Material Kits hoppers.

Later we'll look at producing _Colony Supplies_ at KSC:

1. Colony Supplies x 5 (1 fabricator)
   1. Machinery x 5 (1 fabricator)
      1. MaterialKits x 3
      2. Specialized Parts x 2
   2. MaterialKits x 3
   3. Specialized Parts x 2

This amounts to 6 _material Kits_ and 4 _Specialized Parts_ per batch of 5 _Colony Supplies_.

### Minmus CommNet and Skycrane

- Build **Satellite Bundle** and deploy the relay sats
  - Deployer should go to 357.941km x 534.657km orbit
  - Release one relay satellite just before each periapsis
  - Circularise each relay satellite at periapsis (357.941km circular orbit, 40400s / 1d 5h 13m period, aka 1 Minmus day)
  - Double-check the deployer's orbit between deployments
  - When three relays are deployed, put the deployer into a 200km polar orbit
  - Deploy the scanner and perform an orbital analysis
- Build the Skycrane (WOLF Depot Landers)

For the Greater Flats and Midlands biomes on Minmus:

- Build a Skycrane Depot Box
- Rendezvous Skycrane with the Skycrane Depot Box
- Dock the Skycrane Depot Box with the Skycrane
- Land the Skycrane at the new biome
- Survey the WOLF biome
- Undock the Depot Box
- Switch to the Depot Box
- Select "Establish depot" from the Depot module's PAW
- Switch back to the Skycrane
- Return Skycrane to parking orbit

The remaining biome depots can wait until the Minmus Shipyard is self-sufficient.

Useful Minmus landing sites:

- Midlands (4.390, -86.594 or 4N 86 43'37"W -- flat plateau to the immediate east of Great Flats)
- Greater Flats (0, -7.5 or 0 7 30'00"W)
- Flats (1.5, -40 or 1 30' 0"N 40 0' 0"W -- bottom lobe of the flats just NW of Greater Flats)
- Lesser Flats (9.404, -178.003)
- Great Flats (-10, -92 or 10S 92W)
- Poles (78.045, 164.276) (exotic metals, minerals)
- Lowlands (0.026, -51.516)
- Highlands

### Crew Transport Preparation

- Add Passenger Terminal to Kerbin Shipyard
- Launch **Reactor Maintenance** to rendezvous with Kerbin Shipyard
- Build **Crew Transport**
- Dock **Reactor Maintenance** to **Crew Transport**
- Perform Maintenance on **Crew Transport** (engineer needs to do an EVA)
- Dock **Reactor Maintenance** to **Kerbin Shipyard**

### Minmus Route Preparation

Use **Orbital Route Builder 15LR** to build a route from **Minmus Shipyard** to _Greater Flats_ on **Minmus** and back, and from _Greater Flats_ to _Midlands_ and back:

- Rendezvous **Orbital Route Builder 15LR** with **Minmus Shipyard**
- Move all the propellant from the route builder to the shipyard
- Start the route
- Put enough propellant in the route builder to give ~500m/s delta-v
- Land **Orbital Route Builder 15LR** on _Greater Flats_
- Complete the route (which should be 0 cost)
- Start a new route
- Launch the route builder and rendezvous with **Minmus Shipyard**
- Refuel the route builder
- Complete the route (which should be 0 cost)

### 01 Midlands Exotic Minerals

This first depot expansion is trivial. This is only one harvester, and the just-established Depot has exactly the power required to run this single module.

- Build **01 Midlands Exotic Minerals**
- Rendezvous **Skycrane** with **01 Midlands Exotic Minerals**
- Dock **01 Midlands Exotic Minerals** with **Skycrane**
- Land **Skycrane** in _Midlands_ biome
- Undock **01 Midlands Exotic Minerals**
- Connect **01 Midlands Exotic Minerals** to the Midlands biome depot
- Route the 10 Exotic Minerals production from Midlands to Greater Flats

### 02 Greater Flats Synthetics

Route these resources to Minmus Greater Flats

- 1 Food
- 1 Oxygen
- 5 Water
- 3 Material Kits

Build **02 Greater Flats Specialized Parts** at **Minmus Shipyard**. Fuel it and leave it in a parking orbit (eg: 15km).

Launch a **WOLF Python 95 (Crew Pod)** carrying a **Crew Pod** with the following crew:

- Engineer
- Kolonist
- Mechanic
- Medic
- Miner
- Scientist
- Technician

Now get that crew to the **02 Greater Flats Specialized Parts** vessel:

- Rendezvous **Crew Transport** with **WOLF Python 95 (Crew Pod)**
- Move the crew pod over to dock with **Crew Transport**
- Transfer the Supplies and Fertilizer resources from **WOLF Python 95 (Crew Pod)** to the **Crew Transport**
- Send **Crew Transport** to Minmus
- Return the **WOLF Python 95 (Crew Pod)** to **KSC**
- At Minmus, rendezvous **Crew Transport** with **02 Greater Flats Specialized Parts**
- Detach the **Crew Transfer Pod**
- Dock the **Crew Transfer Pod** with the lander
- Land **02 Greater Flats Specialized Parts** at _Greater Flats_
- Connect the lander to the depot
- transfer 5 Specialized Parts, 2 Alloys, 1 Synthetics from _Greater Flats_ to _Minmus Orbit_
- transfer 1 Alloys from _Minmus Orbit_ to _Kerbin Orbit_
- Connect the Alloys, Synthetics and Specialized Parts hoppers of **Minmus Shipyard** to the depot and start them

### 03 Midlands Agricultural Support

With Specialized Parts and Sythetics being manufactured there's a bit less pressure on resource reserves at **Minmus Shipyard**. Take some time to deploy the remaining Depot modules to the remaining flats, Lowlands, Highlands, and Poles.

Remember to survey the WOLF Biome using the survey scanner nestled in the nose of the **Skycrane**.

From here we're going to work towards producing Electronics and Robotics. To do that we will need to produce material kits to support the Electronics and Robotics production as well as to support maintenance of the depots. There will also be demand for food, water and oxygen.

The immediate next step is to get production of a surplus 5 food, water, oxygen and material kits at Greater Flats, allowing Greater Flats to no longer be dependent on imports of life support from orbit. To produce food at _Greater Flats_ we need to source _Fertilizer_ which means finding _Gypsum_.

After that life support capacity improvement, we'll pursue small increments in Alloys, Synthetics and Material Kits production followed by small increments in Robotics and Electronics production. The main constraint here is going to be limited supplies of those resources at **Minmus Shipyard** -- but this expansion project will be sipping from a very large barrel.

That's the basic road map, now let's get to work!

In the WOLF Tutorial save game, _Midlands_ have 20 abundance of _Gypsum_, 50 abundance of _Hydrates_ but no water. The _Poles_  have 50 _Gypsum_ but no _Water_ or _Hydrates_. So for this fertilizer factory we'll expand the Midlands biome depot.

This depot lander requires the following to be transferred from Greater Flats:

- 1 Food
- 1 Oxygen
- 3 Material Kits

Send this crew as well:

- Engineer
- Kolonist
- Mechanic
- Medic
- Scientist

### 04 Greater Flats Food and Electronics

This one's pretty straight-forward: just use the water and dirt available in the Greater Flats along with the _Fertilizer_ we just started producing in the Midlands to produce lots of food. This lander will add 60 abundance of _Food_ to _Greater Flats_ which will be sufficient to supply the remaining Minmus depots.

To produce 1 abundance of _Electronics_ we need 5 _Material Kits_ and 5 _Synthetics_.

Arrange for 8 more _Exotic Minerals_ to be transferred to _Greater Flats_ from _Midlands_ if you haven't already taken care of that mountain of exports ready to be transferred.

Send this crew:

- Farmer
- Miner
- Technician

### 05 Greater Flats Robotics

No extra resources required for this one, just the crew:

- Miner
- Scientist
- Technician

### Maximising Minmus Production

With the four advanced materials taken care of, Minmus is now effectively self-sufficient.

From here you can skip to **Mun Expansion**, but you'll need to _disconnect **Minmus Shipyard** from the depot first_, and transfer all Minmus Orbit resources to Kerbin Orbit.

If you want to improve the Mun expansion experience a little, stick around and we'll look at strategies for maximising output from biome depots. Eventually we'll finish expanding Minmus just to have resources to produce _Prototypes_, _Colony Supplies_ and _Machinery_ anyway. _Colony Supplies_ in particular are important since they are required as part of the WOLF passenger transport system. While flying rockets is fun, being a bus service can get tedious.

The immediate goal of this expansion is to produce the resources needed to provide **Mun Shipyard** with 15 _Material Kits_, 5 _Specialized Parts_, and 1 each of _Alloys_, _Electronics_, _Robotics_ and _Synthetics_.

### 06 Lowlands Polymers

_Polymers_ are needed for _Material Kits_ and _Synthetics_. More polymers is good!

Prepare for this depot expansion by transferring these resources to the **Lowlands** biome:

- 2 Fertilizer
- 1 Food
- 3 Material Kits

You'll need these crew for the depot expansion itself:

- Engineer
- Kolonist
- Farmer
- Mechanic
- Medic
- Miner
- Scientist
- Technician

Route the Exotics, Polymers and Synthetics produced by this expansion back to _Greater Flats_.

### 07 Flats Stage 1

This depot will be producing a small quantity of _Material Kits_, a lot of water, and laying the infrastructure for a second depot to produce some more _Material Kits_ as more _Polymers_ become available.

- 1 Food

Crew:

- Engineer
- Kolonist
- Mechanic
- Medic
- Miner
- Scientist
- 2 x Technician

### 08 Highlands Material Kits (blue)

If you are like me and abhor trying to land the **Orbital Route Builder 15LR** on terrain that is rarely ever level, check out the **Orbital Route Builder 75** which not only has a larger, more stable landing footprint but also provides 75 route capacity in each trip. It's massively over-sized for this depot expansion but it's so much easier to land on Minmus Highlands and basiclaly anywhere on Mun. Build it now, you'll really appreciate it later!

While you're at it, check out the Skycrane Propellant Dump which provides a nice reservoir of propellant to help you get those 0-credit routes. Land from orbit with full tanks. Empty the route builder's propellant into the propellant dump, start the transport route, then put enough propellant in the tanks for the trip out and back. Your outbound trip will be 0 credits, your inbound trip can refuel fromm what's left in the propellant dump. The catch with the larger route builder is that it's got about half the delta-v of the 15LR (LR for "Long Range").

- 1 Food

- Engineer
- Kolonist
- Mechanic
- Medic
- Miner
- Scientist
- 2 x Technician

This gives us 7 extra _Material Kits_

### 09 Greater Flats Material Kits (yellow)

- Engineer
- Kolonist
- Miner
- 2 x Technician

This gives us 36 extra _Material Kits_. Between this and the Highlands depot previously deployed, that's a fine pile of _Material Kits_ to be sitting on. A lot of these will be consumed as _Colony Supplies_ which are required for WOLF passenger routes. More about that soon.

This lander requires 237,310 _Material Kits_. If you've followed the walkthrough your **Minmus Shipyard** will be producing 15,000 _Material Kits_ per day. Set an alarm (I use Kerbal Alarm Clock in preference to the built-in alarm clock) for the point in time that there will be enough _Material Kits_ to build this lander. Don't waste time with storage full of _Material Kits_!

### 10 Poles Exotic Minerals (white)

The Poles doesn't have much that will help keep it self-sufficient so import the resources needed, and only build what's required to extract all those _Exotic Minerals_.

Transfer these supplies in:

- 1 Food
- 3 Material Kits
- 1 Oxygen
- 5 Water

The lander will need this crew:

- Engineer
- Kolonist
- Mechanic

Once that depot is established, transfer the _Exotic Minerals_ back to _Greater Flats_.

45,580 _Material Kits_.

### 11 Midlands Exotics and Food

We revisit Midlands to extract the remnant _Exotic Minerals_ and produce some food while we're at it.

Imports:

- 3 Material Kits

Crew:

- Farmer

200,887 _Material Kits_

### 12 Great Flats Specialized Parts

This one uses a heap of imported materials to produce _Specialized Parts_ in situ. It's a toss-up between importing _Exotic Minerals_ versus exporting lots of _Silicon_ and _Rare Metals_.

- 12 Exotic Minerals
- 1 Food
- 3 Material Kits
- 1 Oxygen
- 5 Water

The crew is

- Engineer
- Kolonist
- Mechanic
- Medic
- 2 x Miner
- Scientist
- 2 x Technician

155,580 _Material Kits_.

### 13 Flats Chemicals and Silicon (yellow)

Crew:

- 2 x Miner
- Technician

155,530 _Material Kits_

### 14 Lesser Flats Rare Metals (blue)

Imports:

- 1 Food
- 3 Material Kits
- 1 Oxygen
- 5 Water

Crew:

- Engineer
- Kolonist
- Mechanic
- Miner
- Technician

### 15 Highlands Rare Metals

Nothing required, it's just one extractor using excess power.

Crew:

- Scientist
- Technician

### 16 Greater Flats Industry Park

This depot expansion will produce enough advanced resources (Sp/A/E/R/S) to get the Mun base up and running. There will be leftover Specialized Parts to send back to Kerbin for Colony Supplies.

### 17 Great Flats Fuel

Produce a bunch of fuel. This will contribute to resources for Mun Shipyard establishment.

Imports:

- 1 Material Kits

Crew:

- 3 x Geologist

Use these resources in Minmus Orbit, cancel the various transfers from Kerbin Orbit to Minmus Orbit. Send the excess fuel from Kerbin Orbit to Mun Orbit Then connect Mun Shipyard's fuel hoppers and start them up.

187,280 _Material Kits_

### 18 Flats Fuel (purple)

Produce more fuel. This will contribute to resources for future expansion shipyards.

Imports:

- 1 Material Kits

Crew:

- 3 x Geologist

As before, uses these resources to displace Minmus Orbit imports, then export to Kerbin Orbit, and then Mun Orbit.

187,280 _Material Kits_

### 19 Highlands Life Support

Produce water and oxygen for life support systems.

Export to Kerbin Orbit and from there to expansion depots, in this case Mun Orbit.

## Passenger Transport

### Passengers from KSC to Kerbin Orbit

Creating passenger routes is done similarly to creating cargo routes, but there are extra requirements at the origin depot:

- 2 Colony Supplies per luxury berth (colony supplies require specialized parts)
- 2 habitation per luxury berth for the origin terminal
- 2 life support per luxury berth for the origin terminal
- passenger terminal deployed at origin biome
- passenger terminal deployed at destination biome

To set up a 3.75m Passenger Terminal (maximum capacity 6 passengers) we'll want to set up a 6 luxury passenger route (luxury routes are faster, but consume double the resources of economy routes):

- 12 x _Colony Supplies_
  - 36 x _Material Kits_ (3 x 12)
  - 24 x _Specialized Parts_ (2 x 12)
- 12 x _Habitation_
- 12 x _Life Support_

Prepare 6 Passenger SSTO for launch:

- Transfer propellant to KSC Passenger Terminal
- Start the passenger route
- Transfer propellant back to 6 Passenger SSTO
- Launch to orbit
- Rendezvous with **Kerbin Shipyard**

### Passengers from Kerbin Orbit to Minmus Orbit

### Transfer Passengers to Depot Expansion

- EVA and jetpack
- Dock and transfer crew between modules
- Load crew into Crew Pod and dock crew pod to depot expansion

## The Mun Expansion

The Mun expansion will be a rehearsal for further expansion into the Kerbol system. The basics will be:

- establish a shipyard
- transfer WOLF resources using WOLF cargo routes
- establish communications network
- build a route builder rover (and land it)
- prepare WOLF passenger routes
- build the WOLF infrastructure at the shipyard
- import crew from Kerbin via the WOLF passenger routes

### Mun Shipyard

- Prepare for expansion by building route from _Kerbin Orbit_ to _Mun Orbit_
- Transfer 15 _Material Kits_, 5 _Specialized Parts_, 1 _Alloys_, 1 _Electronics_, 1 _Robotics_ and 1 _Synthetics_ to _the Mun_
- Build **Expansion Shipyard** at **Kerbin Shipyard**
- Rename **Expansin Shipyard** to **Mun Shipyard**
- Provide **Mun Shipyard** with starter resources of _Alloys_, _Electronics_, _Robotics_ and _Prototypes_ (basically enough to build the A/E/R/S Hopper)
  - 94 Alloys
  - 145 Synthetics
  - 20 Robotics
  - 20 Prototypes
  - (No electronics required to bootstrap)
  - (Material Kits and Specialized Parts will arrive via WOLF Transfers)
- Send **Mun Shipyard** to _the Mun_
- Once at _the Mun_ put **Mun Shipyard** into a circular 30km orbit at 0 inclination
- Build the **A/E/R/S Hopper** shipyard component
- Dock the **A/E/R/S Hopper** to the **Mun Shipyard**
- Connect the four WOLF Manufacturing Hoppers to the depot and start them
- Build the **Passenger Terminal** shipyard component
- Dock the **Passenger Terminal** to **Mun Shipyard**

### Mun CommNet

- Build **Satellite Bundle** and deploy the relay sats
  - Deployer should go to 357.941km x 534.657km orbit
  - Release one relay satellite just before each periapsis
  - Circularise each relay satellite at periapsis (357.941km circular orbit, 40400s / 1d 5h 13m period, aka 1 Minmus day)
  - Double-check the deployer's orbit between deployments
  - When three relays are deployed, put the deployer into a 200km polar orbit
  - Deploy the scanner and perform an orbital analysis

### Mun Route Builder Rover

The **Route Builder Rover** has a nuclear power plant. To build it you need to get an Engineer to the **Mun Shipyard** with _Enriched Uranium_ in order to start the reactor.

- Rendezvous the **Reactor Maintenance** craft with **Kerbin Shipyard** and transfer _supplies_
- Rendezvous the **Reactor Maintenance** craft with **Mun Shipyard** and dock
- Build the **Route Builder Rover**
- Transfer propellant from **Mun Shipyard** to **Route Builder Rover**
- Undock **Reactor Maintenance** from **Mun Shipyard**
- Dock **Reactor Maintenance** to **Route Builder Rover**
- Use the engineer in EVA to _Perform Maintenance_ on the **Route Builder Rover**'s nuclear reactor
- Return the engineer from EVA and dock **Reactor Maintenance** with **Mun Shipyard**
- Land the **Route Builder Rover** on **The Mun**
- Undock **Reactor Maintenance** from **Mun Shipyard**
- Transfer **Reactor Maintenance** to a parking orbit

Land the **Route Builder Rover** at **Farside Crater**. Build routes from here to:

- Highlands
- East Farside Crater
- Twin Craters
- Canyons
- (continue to the remaining biomes)

### Mun Depots

Establishing depots will take a few hours. The aim here is the same as for **Minmus**: get the local shipyard to be self-sufficient, get some excess _Specialized Parts_ and _Material Kits_ production to support further expansion of the passenger network, then look at what else can be produced locally to contribute towards _Prototypes_ production back at **Kerbin Shipyard**.

Establish depots in these biomes (locations are flat-ish and level-ish enough to land a rocket or park a rover):

- Canyons (18.150, -50,300) (18.177, -50.448)
- East Crater (-9.746, 84.452)
- East Farside Crater (7.109, -150.838) (7° 6' 32.4"N, 150° 50' 16.8"W)
- Farside Basin (20.618, -93.351) (29 37' 5"N, 93 21' 5"W) or (31.279 96.945) (31 16'44"N 96 53'48"W)
- Farside Crater (-0.247, -58.873) (0 14' 48"N, 58 53' 2"W)
- Highland Craters (64.424, 173.655) (64 25' 41"N 173 40' 3"E)
- Highlands (0.372, -34.280)
- Lowlands (0.305, -0.530)
- Midland Craters
- Midlands (-0.97, 158.681)
- Northern Basin
- Northwest Crater (2.926, 17.980) (2 55'34"N 17 59'9"E)
- Polar Crater (50 52' 4"N 36 32' 59"W)
- Polar Lowlands (79.666, 108.266)
- Poles
- Southwest Crater (-28.202, 8.093) (28 9'55"S 8 14'53"E)
- Twin Craters (-5.916, 139.817) (5 54'56"S, 139 49' 1"E)

Canyons is unique in having Exotic Minerals and Rare Metals in one biome, from this one depot we can develop an abundance of 160 _Specialized Parts_ and 15 _Synthetics_ (ignoring allocaton of rare metals for alloys or polymers for material kits). Canyons can also be expanded to produce food, water and oxygen.

The highest abundance of manufactured items:

- 95 Material Kits from Twin Craters
- 125 Specialized Parts from Highlands

The highest sources of base materials are:

- 96 Chemicals from Canyons
- 130 Exotic Minerals from Polar Crater
- 68 Metals from East Farside Crater
- 52 Polymers from East Farside Crater
- 160 Rare Metals from Farside Basin
- 160 Silicon from Polar Crater

Life support:

- 140 Food, 78 water from Twin Craters
- 100 Food, 118 water from Highlands

For these depots on the Mun the crew are usually 12 kerbals, so two flights from KSC to orbit, then to Mun Orbit. Once there is sufficient supply of Specialized Parts there should be sufficient Colony Supplies to launch the 5m passenger route builder 

### 01 Farside Crater Material Kits

Crew:

- Engineer
- Farmer
- Kolonist
- Mechanic
- Medic
- Miner x 3
- Scientist
- Technician x 3

### 02 Highlands Specialized Parts

Imports:

- 4 x Material Kits

Crew:

- Engineer
- Farmer
- Kolonist
- Mechanic
- Medic
- Miner x 3
- Scientist
- Technician x 3

### 03 East Farside Polymers

Crew:

- Engineer
- Farmer
- Kolonist
- Mechanic
- Medic
- Miner x 3
- Scientist
- Technician x 3

### 04 Twin Craters Polymers

Crew:

- Engineer
- Farmer
- Kolonist
- Mechanic
- Medic
- Miner x 3
- Scientist
- Technician x 3

### 05 Canyons Exotic Minerals

Imports:

- 2 fertilizer
- 4 material kits

Crew:

- Engineer
- Kolonist
- Farmer
- Mechanic
- Medic
- Miner x 2
- Scientist
- Technician x 2

### 06 Farside Basin Material Kits

Imports:

- 1 Food

Crew:

- Engineer
- Kolonist
- Mechanic
- Medic
- Miner x 2
- Scientist
- Technician x 3

Build Cost: 431,820 Material Kits

### 07 Canyons Electronics and Robotics

Imports:

- 11 x Material Kits
- 6 x Metals

Crew:

- 2 x Miner
- Scientist
- 2 x Technician

Build Cost: 159,910 Material Kits

### 08 Twin Craters Material Kits

Imports:

- 12 x Polymers

Crew:

- 2 x Miner
- 4 x Technician

Build Cost: 371820

### 09 East Farside Crater Rare Metals

Prepare 110 route capacity between East Farside Crater and Farside Crater.

Imports:

- 1 x Material Kits

Crew:

- Kolonist
- 2 x Miner
- 2 x Technician

Build Cost: 316,820 Material Kits

### 10 Farside Crater Specialized Parts

Crew:

- Miner
- Technician x 5

Build Cost: 278,395 Material Kits

### 11 Highlands Specialized Parts

Imports:

- Material Kits x 2

Crew:

- Miner x 2
- Technician x 4

Build Cost:

### 12 Polar Crater Exotic Minerals

Imports:

- Fertilizer x 2
- Material Kits x 3

Crew:

- Engineer
- Farmer
- Kolonist
- Mechanic
- Medic
- Scientist

Build Cost: 216600 Material Kits

## Duna Expansion

Build these ships and send them to Duna, try to get them to arrive in this order too:

- Duna Shipyard
- Cargo route builder
- Passenger route builder
- Reactor Maintenance with Engineer and Pilot (if you plan to use the Route Builder Rover)

Remember to add the materials to the shipyard that it will need to build the **A/E/R/S Hopper**:

- 94 Alloys
- 145 Synthetics
- 20 Robotics

Establish the shipyard at a "low" Duna Orbit (100km or less), then:

- connect the cargo route to the Duna:Orbit depot
- transfer 5 x _Material Kits_, 5 x _Specialized Parts_, and 1 each of Alloys, Electronics, Robotics and Synthetics from Kerbin:Orbit to Duna:Orbit
- connect the _Specialized Parts_ hopper and one _Material Kits_ hopper to the depot and start them up
- Deploy the Orbital Shipyard when you have 4000 _Material Kits_ (about 6 hours)
- If you have an engineer available, deconstruct the fuel tanks and engines that were used to deliver the **Duna Shipyard** to Duna (this should produce a reasonable amount of the advanced resources)
- Build the **A/E/R/S Hopper** and attach it to the shipyard (requires about 6 days of resource production)
- Build the **Passenger Terminal** and attach it to the shipyard (requires about 10 days of production)
- connect the passenger route to the Duna:Orbit depot
- set up relay satellites at 60 degrees and 120 degrees from Ike, in circular orbits with the same period
- deploy rover to survey biomes

From here the process is the same as the previous expansions:

1. 5 Fuel to support depot landers
1. 15 Material Kits
1. 5 Fertilizer + 5 Supplies to support passenger terminal
1. 1 each A/E/R/S
1. 5 Specialized Parts

That will conclude this walkthrough, by now you have the idea of how the WOLF infrastructure works and should be able to write your own adventures!

### Relay Satellites

Ike orbital period is 65,766.7s (3d 0h 11m).

### 01 Midland Sea Material Kits

You should now have a passenger route set up between Kerbin Orbit and Duna Orbit. Time to put it to use.

Imports:

- Food
- Oxygen
- 5 x Water

Crew:

- Engineer
- Kolonist
- Mechanic
- Miner
- 2 x Technician

Get that crew transferred to Kerbin Shipyard. Once there, send them off to Duna. This route will take 1y 367d. That's a lot of time to be waiting for things to happen!

Spend the time exploring the other biomes, establishing Depots, and perhaps even sending new shipyards and route builders to Eve, Moho and Jool.

# WOLF Walkthrough Conclusion

This is the end of the walkthrough for now. You have the tools and training required to use the WOLF Industry system. Good luck with your adventures!

[MRWOLFTS]: https://github.com/MaraRinn/WOLF-Tutorial-Ships "Mara Rinn's WOLF Tutorial Ships repository"
[RDWOLF1]: https://docs.google.com/document/d/1zft2Ka9gubOYQf4CQgvReTxpnP8_LQYNyHouEjQZqjw/edit "Roverdude's introduction to WOLF"
[RDCONV]: https://kerbal-forum-uploads.s3.us-west-2.amazonaws.com/monthly_2020_12/wolf.png.53d635bf5f1f4cc0e4e2f6286409d827.png "Roverdude's resource conversion diagram"
[RDTRAN1]: https://docs.google.com/document/d/1BEqW60RrnYiVJKpAIFHAUqhdBrzbwwQ7KsaJ8hZjH4w/edit "Roverdude's introduction to transport credits"
[USIRELEASES]: https://github.com/UmbraSpaceIndustries/UmbraSpaceIndustries/releases "Umbra Space Industries combined package releases"
[CRPRELEASES]: https://github.com/UmbraSpaceIndustries/CommunityResourcePack/releases "Community Resource Pack releases"
[KSPROOT]: https://wiki.kerbalspaceprogram.com/wiki/Root_directory "Where to find the KSP root directory"

[AddOnInstallation]: Screenshots/AddonInstallation.png "Drag the contents of the USI GameData folder to teh KSP GameData folder, then drag the contents of the CRP GameData folder to the KSP GameData folder, overwriting the CommunityResourcePack folder that's already there"
[TutorialShipsInstall]: Screenshots/WOLFTutorialSaveInstall.png "Drag the WOLF Tutorial folder from the WOLF Tutorial package to the Kerba Space Program saves folder, replacing any existing save of the same name"
[WolfDepotDeployerParts]: Screenshots/WOLFDepotDeployerParts.png "Runway scene with Wolf Depot Deployer showing WOLF related parts with PAWs open for Surface Scanner, WOLF Transport Computer and Bon Voyage controller"
[WolfDashboardHarvestableResourcesEmpty]: Screenshots/WolfDashboardHarvestableResourcesEmpty.png "Runway scene with WOLF Dashboard open to Harvestable Resources pane showing no biomes with harvestable resources because they have not been scanned"
[WolfDashboardHarvestableResourcesScannedBiome]: Screenshots/WolfDashboardHarvestableResourcesScannedBiome.png "SPH scene with WOLF Dashboard open to Harvestable Resources pane showing resource abundance for freshly scanned biome"
[SPHWOLFEMPTY]: Screenshots/SPHWOLFEMPTY.png "SPH scene with WOLF Dashboard open to Depots pane showing no depots"
[SPHsceneFabricatorModuleWOLFDashboardPlanner]: Screenshots/SPHsceneFabricatorModuleWOLFDashboardPlanner.png "SPH scene with WOLF Dashboard open to Planner pane and WOLF Fabricator Module as the first part of a new vessel"
[SPHSCENE2MATKITS]: Screenshots/SPHSCENE2MATKITS.png "SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance"
[WOLFDEPOTPAWESTABLISH]: Screenshots/WOLFDEPOTPAWESTABLISH.png "WOLF Depot Module with PAW showing Establish depot action"
[WOLFDASHKERBINDEPOTBONUS]: Screenshots/WOLFDASHKERBINDEPOTBONUS.png "WOLF Dashboard showing the new KSC Biome Depot with bonus resources awarded to Kerbin-based depots"
[RUNWAYWOLFDASHNEWKSCDEPOTPRODUCTION]: Screenshots/RUNWAYWOLFDASHNEWKSCDEPOTPRODUCTION.png "Runway scene with WOLF Dashboard showing new production added"
[RUNWAYDEPOTBONVOYAGE]: Screenshots/RUNWAYDEPOTBONVOYAGE.png "Runway scene with WOLF Depot Deployer Rover PAW and Bon Voyage control panel with destination set"
[KERBINSHORESDEPOTDEPLOYMENT]: Screenshots/KERBINSHORESDEPOTDEPLOYMENT.png "Kerbin Shores scene with WOLF Depot Deployer. The depot and trailer are decoupled and Surface Scanner PAW is open. There are numbers 1, 2 and 3 indicating the order of operations."
[KERBINSHORESDEPOTDASHBOARD]: Screenshots/KERBINSHORESDEPOTDASHBOARD.png "Kerbin Shores scene with WOLF Dashboard open to Depots pane showing new Kerbin Shores depot"
[SPHDDRMaterialKitsAndCrew]: Screenshots/SPHDepotDeployer5MaterialKitsTrailer.png
[MountainsDepotDeployerConnectOriginDepot]: Screenshots/MountainsDepotDeployerConnectOriginDepot.png "Mountains scene with WOLF Depot Deployer rover showing the Transport Computer PAW. The 'connect to origin depot' action is visible."
[KSCDepotDeployerCoonectDestinationDepot]: Screenshots/KSCDepotDeployerCoonectDestinationDepot.png "WOLF Depot Deployer rover at KSC with 'connect to destination depot' action visible in the Transport Computer PAW"
[SPHWOLFDASHSTARTERPRODUCTION]: Screenshots/SPHWOLFDASHSTARTERPRODUCTION.png "SPH scene with WOLF dashboard showing starter depots expanded with completed production of material kits, fuel, food, oxygen, water and fertilizer"
[SPHWOLFDASHROUTESPANE]: Screenshots/SPHWOLFDASHROUTESPANE.png "SPH scene with WOLF dashboard open to routes pane showing starter routes established during depot construction"
[SPHWOLFDASHMANAGETRANSFERS]: Screenshots/SPHWOLFDASHMANAGETRANSFERS.png "SPH scene with WOLF Dashboard showing the Manage Transfers interface"
[KSCTransferMaterialKitsMountainsToKSC]: Screenshots/KSCTransferMaterialKitsMountainsToKSC.png "KSC scene with Transfer Resources interface showing a new transfer of 6 MaterialKits from Mountains to KSC"
[KSCTransfersFromHighlandsMountainsShores]: Screenshots/KSCTransfersFromHighlandsMountainsShores.png "KSC scene with WOLF Dashboard showing transfers from highlands, mountains and shores to KSC"
[SPHRouteBuilderRover]: Screenshots/SPHRouteBuilderRover.png "SPH scene showing Route Builder Rover"
[KSCRouteBuilderRoutesBuilt]: Screenshots/KSCRouteBuilderRoutesBuilt.png "KSC scene with WOLF Dashboard open to the Routes pane. There are a number of routes built between KSC and the various biomes, expanded with the 45 payload capacity Route Builder Rover"
[SmallSSTORocketStartRouteAtLaunch]: Screenshots/SmallSSTORocketStartRouteAtLaunch.png
[SmallSSTORocketRouteCost30]: Screenshots/SmallSSTORocketRouteCost30.png
[KERB375ROCKETCREDITS]: Screenshots/KERB375ROCKETCREDITS.png
[WOLFSSTO0CREDITS]: Screenshots/WOLFSSTO0CREDITS.png
[SSTORTCOST8]: Screenshots/WOLFSSTOinOrbitWithRouteCost8.png "The WOLF SSTO craft in orbit with Transport Computer PAW open showing route cost of 8"
[ES96RTCOST85]: Screenshots/ES96PythonInOrbitWithRouteCost85.png "The ES-96 Python in orbit with Transport Computer PAW open showing route cost of over 80"
[VABWOLFTutorial100TransportCredits]: Screenshots/VABWOLFTutorial100TransportCredits.png
