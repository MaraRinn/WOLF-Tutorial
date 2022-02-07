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
  - [WOLF Transfers](#wolf-transfers)
  - [Transport Routes and Transport Credits Costs](#transport-routes-and-transport-credits-costs)
    - [Quick and Dirty Transport Credit Example Flights](#quick-and-dirty-transport-credit-example-flights)
    - [Transport Module for Transport Credits](#transport-module-for-transport-credits)
    - [How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles](#how-to-avoid-transport-credit-costs-of-propellant-consuming-vehicles)
  - [Bootstrapping Kerbin Orbit WOLF Infrastructure](#bootstrapping-kerbin-orbit-wolf-infrastructure)
  - [Extracting Resources from WOLF to MKS](#extracting-resources-from-wolf-to-mks)
  - [Establishing the Kerbin Shipyard](#establishing-the-kerbin-shipyard)
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
5. I recommend you install the [Bon Voyage][BonVoyageAddon] addon, it will be very useful for managing rovers later (it will save you hours of driving rovers around)

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

Finally, add the harvesters and refineries required for the chemicals (feed stock is minerals), metals (feed stock is metallic ore) and polymers (feed stock is substrates). These modules have added demand for a _Miner_ crew member so recruit one of those and add them to the crew module. To finish off this infrastructure install add another **WOLF Power Module**, and you should no longer have any deficits in the _Planner_. **Note** that some of the _Material Kits_ produced by this infrastructure have immediately been consumed by other parts of the infrastructure (the habitation, life support and maintenance modules each consume 1 *Material Kits* abundance). From the 5 _Material Kits_ produced by the fabricator, 3 have been consume by the depot infrastructure leaving 2 for use elsewhere.

Before we can deploy this infrastructure we need to establish the depot itself. To do this, add a decoupler and a **WOLF Depot Module** with a probe core. Note that this depot module, probe core and decoupler combination is going to be used so often that I prepared a subassembly for it -- check Subassemblies for _Depot on Decoupler_. When you launch this craft you'll decouple the depot, which needs control in order to be useful.

What a beautiful creation! Did yours turn out like mine?

![SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance][SPHSCENE2MATKITS]

If you're familiar with the production chains from MKS you'll see that this WOLF infrastructure is a lot simpler than what is required in MKS, for example each **WOLF MHU-550 Bulk Harvester** is roughly equivalent to a mining ship with a logistics hub attached to the planetary warehouse -- each of those mining ships will be a dozen parts given the need for drills, ore tanks, radiators, power source, probe core and whatever else you normally put on your mining ships. That part count can severely bulk out your save file size, and slow your game to a crawl any time you load a production facility into physics range. WOLF removes all that complexity from the save file and physics simulation (including the need to visit facilities every so often to update the resource processing chains).

## Establish KSC Depot

Launch that craft you just created. You're going to separate the depot and immediately hand it over to the WOLF system.

**Warning**: Any other parts attached to the WOLF modules will be consumed along with the WOLF modules when you hand them over to the biome depot, including any crew. In addition the WOLF Depot can not have any other WOLF components attached, _not even the Survey Scanner_.

Now that you have your two-component craft separated (the WOLF Depot Module and a cheap probe core), it's time to establish your KSC Biome Depot:

![WOLF Depot Module with PAW showing "Establish Depot" action.][WOLFDEPOTPAWESTABLISH]

Just select the _Establish Depot_ action for the WOLF Depot Module, and the craft will disappear. It belongs to WOLF now.

Check out the Depots pane of the WOLF Dashboard now:

![WOLF Dashboard showing the new KSC Biome Depot with bonus resources awarded to Kerbin-based depots][WOLFDASHKERBINDEPOTBONUS]

That depot has given us 1 Food, 1 Oxygen, 5 Material Kits, 5 Water, and 10 Power. This will significantly reduce the amount of infrastructure we need to get started — but remember that these bonus resources only apply to WOLF biomes on Kerbin.

Switch to the remaining craft (by default '[' or ']' will cycle active vessels) and select the _Connect to depot_ action for one of the WOLF modules. With that done, open the **WOLF Dashboard** and check the _Depots_ pane.

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
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer**
- Move the rover back to the KSC
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer**
- Recover the rover

## Adding Production to WOLF Depots

The aim of our activities here is to establish an orbital ship yard and build spacecraft in orbit to further expand the WOLF infrastructure to other worlds. To build spacecraft at the orbital shipyard, you'll need _Material Kits_, _Specialized Parts_, _Alloys_, _Electronics_, _Prototypes_, _Robotics_ and _Synthetics_.

Let's start with the _Alloys_, building a _WOLF Depot Deployer Rover_ trailer from scratch. To start with just assemble a **Karibou Passenger Cabin** and **Karibou Flatbed Wheel Bay**, add some wheels and an avionics package (this starting trailer is available as **WOLF Depot Deployer Trailer** in the subassemblies listing). Add a **WOLF Fabricator Module** and set its recipe to _Alloys_. Now you have a deficit of _Rare Metals_, which are collected by a harvester module. Add a **WOLF MHU-500 Bulk Harvester** and set its recipe to _Rare Metals_. There's a deficit of _Rare Metals_ in this biome, so check through the remaining depots to see if you can find _Rare Metals_.

Unfortunately, it turns out that _Rare Metals_ are not a thing in Kerbin biomes. Okay, what about the others? _Electronics_ requires _Synthetics_ which in turn requires _ExoticMinerals_ ... which it turns out are not available on Kerbin either. Maybe _Prototypes_ then? No, they require _Electronics_ which we can't manufacture in WOLF on Kerbin. _Robotics_ are in the same boat, requiring _Alloys_. Last on the list are _Specialized Parts_ but it turns out that they require _Refined Exotics_ (_Rare Metals_ and _Exotic Minerals_).

The only spaceship-building things we can make on Kerbin using WOLF infrastructure are _Material Kits_ and _Fuel_. What do we do about the rest? For the boot-strapping stage, any time we need _Specialized Parts_, _Alloys_, _Electronics_, _Prototypes_, _Robotics_ or _Synthetics_ the options are to buy them (create a new craft with a resource container full of the resource we're after), set up WOLF infrastructure where we _can_ find them and transport the supplies to the shipyard, or find some surface resources to extract and perform all the industry using MKS (the shipyard is MKS infrastructure so this is perfectly acceptable).

For this walkthrough we're not going to go overboard with production, and as far as the other spaceship building materials go we'll simply buy them. Tens of abundance for _Material Kits_ and _Fuel_ will be enough to get us to Minmus where we'll find the resources that Kerbin doesn't have itself. Along the way we'll also produce _Fertilizer_, _Food_, _Oxygen_, and _Water_ to reduce the amount of infrastructure we need to establish on Minmus at the start.

Clear the SPH build area and load up the **WOLF Depot Deployer Rover**, add the **DDR 5 Material Kits** subassembly, put a Miner and a Technician in the passenger cabin (as indicated in the subassembly description), and check the _Planner_ pane of the **WOLF Dashboard** to see which biome will have the most resources left over after we commit to this _Material Kit_ production. For me this is the Mountains biome which had 100 _Minerals_ abundance before this infrastructure took 10 away. Launch the rover and send it to the Mountains biome (0.637, -78.659).

As is usual with the Depot Deployer Rover:

- undock the trailer and connect that to the depot
- connect the transport computer to the origin depot
- send the rover back to KSC
- connect the transport computer to the destination depot
- recover the vessel

You should be able to send one of these **DDR 5 Material Kits** trailers to each of the biomes, and a second one to the _Mountains_ biome.

One that is done, send a Depot Deployer rover with the **DDR 20 Fuel** subassembly to the Shores biome and deploy it there.

Now send the **DDR 20 Food** subassembly to the Grasslands biome and deploy that.

Finally send the **DDR Life Support** subassembly to the Shores and deploy that.

To recap:

- DDR 5 Material Kits expansions deployed to
  - KSC
  - Shores
  - Grasslands
  - Highlands
  - Mountains
- DDR 20 Fuel expansion deployed to Shores
- DDR 20 Food expansion deployed to Grasslands
- DDR Life Support expansion to Highlands

After all that effort the _Depots_ tab of your **WOLF Dashboard** should look something like this:

![SPH scene with WOLF Dashboard showing material kits and fuel production from KSC, Shores, Grasslands, Highlands and Mountians][SPHWOLFDASHSTARTERPRODUCTION]

## WOLF Routes

It's all well and good having that _Material Kits_ production chain set up in the mountains, but what do we do with the output? At present all of this work has set up _abundance_ of certain resource types in the invisible world of WOLF. Eventually you'll pull resources out of WOLF into the MKS world.

The next stage from WOLF production to MKS extraction is getting those WOLF resources to orbit, where we want to use Material Kits and other resources to build spaceships. The immediate progress we need to make is pulling the resources from the WOLF depots to the KSC and then transferring them to orbit over a WOLF route.

WOLF handles transport of resources from one biome to another by way of _Routes_ which are path established for _Transfers_. You establish a route by travelling between biomes using the WOLF Transport Computer to connect origin and destination depots. This will add _Route_ between the source biome and the destination biome. You can then add resources to *Transfers* on that route. Each transfer has a certain capacity, you'll allocate an abundance of resource to a transfer, then the abundance of that resource will be reduced in the source biome and increased in the target biome.

You already have some routes established as part of the initial deployment of WOLF depots with the WOLF Depot Deployer. To establish a *transfer* open the **WOLF Dashboard** to the _Routes_ pane. Select the _Manage Transfers_ button which will show you the _Manage Transfers_ interface:

![SPH scene with WOLF Dashboard showing the Manage Transfers interface][SPHWOLFDASHMANAGETRANSFERS]

To transfer resources simply select the resource in the top section, enter the abundance you wish to shift between depots in _Transfer Amount_ then select _Transfer_. Do that now to move 5 Material Kits from the Mountains depot to the KSC depot. Use either the drop-down menu at the tp of the _Manage Transfers_ interface or the left/right arrows either side of that drop-down to select the route that you want the transfer to use (in this case "Kerbin:Mountains => Kerbin:KSC").

Here's what my transport routes and production look like with the depots transferring some resources to KSC:

![KSC scene with WOLF Dashboard showing transfers from highlands, mountains and shores to KSC][KSCTransfersFromHighlandsMountainsShores]

Note that with 20 _Fuel_ abundance I'd have to run the rover back and forth 7 times. That seems a lot like hard work so I'll slap together a rover with three of the largest WOLF payload Kontainers and call it the **WOLF Route Builder Rover**. This rover has 45 payload capacity so it'll build my fuel routes quite quickly. It also has a trailer subassembly, so if you were having trouble with the **WOLF Depot Deployer** due to the weight of the payloads it was hauling (I sometimes had problems with wheels popping or suspension bouncing) give this route builder rover a try.

![SPH scene with WOLF Route Builder Rover][SPHRouteBuilderRover]

Take that rover out to each of the depots to build a route to KSC, that should keep you covered for the entire walkthrough. The procedure for building these routes with the tutorial rovers is:

- Launch the rover on its own
- On the runway, lock the brakes (icon in the HUD) and start the reactor (AG0)
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer**
- Move the rover to the remote biome
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer**
- Use the _Connect to Origin Depot_ action on the **WOLF Transport Computer**
- Move the rover back to the KSC
- Use the _Connect to Destination Depot_ action on the **WOLF Transport Computer**
- Repeat this process as often as you need

Here's one I prepared earlier (just a bunch of routes with a decent amount of payload capacity):

![KSC scene with WOLF Dashboard open to the Routes pane][KSCRouteBuilderRoutesBuilt]

## WOLF Transfers

In this walkthrough the main purpose of setting up these biomes is to get Material Kits and Fuel to orbit to start building spaceships. There are no doubt untapped opportunities in your biomes (eg: the ability to send one resource from a biome with excess to another biome with a deficit), but for now we have plenty of output to get to orbit.

Open the WOLF dashboard to the _Routes_ pane and open the _Manage Transfers_ dialog:

![Manage Transfers dialog showing resources available at source and destination][ManageTransfersDiscussion]

This dialog is use to set up resource transfers over a route. The numbers visible in this dialog show:

- The resources and their abundance at the source biome depot
- The selected resource
- The abundance of that resource in the source biome depot
- The current available/incoming values of the resource in the destination biome
- The list of resources that you have already selected for transfer on this route
- How much payload capacity is left for transfers
- How much payload capacity has already been used

How much of a resource you can add to transfers on this route is the smaller number of the abundance of the resource or the available payload. In the example above there are 20 Material Kit points available, and the payload has space for all of them with room to spare.

Click the downward pointing triangle next to _Material Kits_ in the available resources list.

If you have more Material Kit abundance than will fit in the payload, you can simply connect the route more times with your route-building vehicles to increase the payload size.

Set the _Transfer Amount_ to 1, then click _Transfer_. You should notice:

- The "Origin" abundance will drop by 1
- The "Destination" abundance will increase by 1
- The "Available Payload" will drop by 1/1 (eg from 7/10 to 8/11)

You'll see a new row in the bottom table displaying the transfer you've just organised. Add another transfer of 5 Material Kits, and you'll see the details in the Resource/Origin/Destination values and the row in the bottom table updated to show the new payload contents.

The _Routes_ pane of the **WOLF Dashboard** will now show the resources being transferred between the various biomes and the KSC. In my example I've set up the production, routes and transfers to provide 20 surplus _Material Kits_ and 20 surplus _Fuel_ for the KSC depot. I want to get that _abundance_ to Kerbin orbit, so it's time to talk about transport credits which should be familiar to people who have used MKS in the past, and then we can talk about how to get _abundance_ out of the WOLF system and turn it into materials for MKS activities.

Go ahead and get all the surplus _Material Kits_ and _Fuel_ abundance on transfers to KSC:

![WOLF Dashboard open to the Routes pane displaying the various transfers that have been arranged over the established routes]()

## Transport Routes and Transport Credits Costs

Up till now we've kept the transport routes simple by only connecting biomes that can be reached without expending mass. It's time to kick it up a notch and learn about Transport Credits, which is an abstraction of the process of building launch vehicles, fuelling them and launching payloads to orbit (or deorbiting payloads to bring them to the surface).

The first thing we'll do here is a few test flights to understand how many _Transport Credits_ we'll need for sending supplies to orbit (or roughly, how Transport Credits correlate to delta-v and ship size). Let's start with a "small" rocket, a medium sized rocket, a 3t payload SSTO spaceplane, and a 55t payload SSTO spaceplane. Note that with enough Transport Credits each flight will add a certain payload capacity to the available routes from KSC to Kerbin Orbit, with the payload capacity being proportional to the payload capacity of each launch vehicle. We'll get the gory details soon!

**Save your game here**, give it a name like "Before Transport Credits". Skip ahead to the next section (_Extracting Resources from WOLF to MKS_) if you don't want to learn about transport costs and how to avoid them. You're going to be restoring to this point after experimenting with _Transport Credits_, and through the rest of the walkthrough there will be no transport costs other than time.

### Quick and Dirty Transport Credit Example Flights

In the VAB, put together a rocket that can carry a single 3t **2.5m WOLF Cargo Kontainer** to orbit using 2.5m parts. The *_WOLF Tutorial 2.5m SSTO_ contains:

- 2.5m WOLF Cargo Kontainer
- RC-001S Remote Guidance Unit
- Protective Rocket Nosecone Mk7
- Rockomax Jumbo-64 Fuel Tank
- RE-I5 "Skipper" Liquid Fuel Engine
- WOLF Transport Computer

Send that to the launch pad, select the _Connect to Origin Depot_ action on the **WOLF Transport Computer**, and launch the rocket to a 80km orbit. Once in orbit, check the "Route cost" reported by the **WOLF Transport Computer**.

If you try to use the **Connect to Destination Depot** action, you should get an error message about needing more Transport Credits to complete that operation. Revert to launch, and run it a few times just to see that the "Route cost" is predictable. My flights came up with a route cost of around 30 _Transport Credits_ which works out to a _Transport Credits Per Unit_ cost of around 10.

![Sample flight of 2.5m rocket showing a route cost of 30](https://i.imgur.com/Iq5PW4k.jpg)

Revert to vehicle assembly and do the same thing with a 3.75m rocket. The _WOLF Tutorial 3.75m SSTO_ is roughly:

- 2 x 3.75m WOLF Cargo Kontainer
- Protective Rocket Nosecone Mk7
- RC-L01 Remote Guidance Unit
- Advanced Reaction Wheel Module, Large
- WOLF Transport Computer
- Kerbodyne S3-14400 Tank
- S3 KS-24x4 "Mammoth" Liquid Fuel Engine

![Sample flight of 3.75m rocket showing a route cost of 85]()

Send that to the launch pad, select the "connect to origin depot" on the WOLF Transport Computer, and launch the rocket to an 80km orbit. As before, check the "route cost", revert to launch and run the process again to show that the "route cost" is predictable. My flights came up with a route cost of 86, giving a _Transport Credit Per Unit_ cost of around 6.14. Revert to vehicle assembly when done.

Now do the same thing with spaceplanes. The two I use are the **WOLF SSTO** and the [ES-96 Python by Juggernoob](https://steamcommunity.com/sharedfiles/filedetails/?id=1722161481) which I find to be an aesthetically pleasing and easy-to-fly SSTO spaceplanes.

**Instructions:** for both these spaceplanes the procedure to get to orbit is:

- set throttle to maximum
- turn SAS on to stability assist
- stage once to light the engines
- rotate off the runway to 10 degrees at about 140m/s
- hold the nose at 10 degrees for the whole flight through the atmosphere
- when the airbreathing mode is insufficient to keep accelerating, switch to closed cycle (Action Group 1)
- push the apoapsis to 80km and cut the throttle
- cruise to the top of the atmosphere, plot a circularisation burn at apoapsis
- execute that burn.

My flights with **WOLF SSTO** ended up producing routes with a cost of 9 for 3t cargo, or about 3 credits/unit.

![Sample flight of WOLF SSTO showing route cost of 8 for 3t cargo][SSTORTCOST8]

The **ES-96 Python** got to orbit in the order of 90 Credits for 42t. The **WOLF ES-96 Python** in the tutorial ships package has already been modified and will automatically start the transport route when you stage to launch (the **Transport Computer** is in the cargo bay with the _Connect to origin depot_ action linked to the _stage_ action group).

![Sample flight of WOLF ES-96 PYTHON showing route cost of 85 for 42t][ES96RTCOST85]

### Transport Module for Transport Credits

How do we produce Transport Credits? The short version is that _Transport Credits_ are produced by the _WOLF Transport Module_. By now you should be familiar with the drill: start assembling a new WOLF infrastructure component with the WOLF Dashboard open to the Planning pane, beginning with the WOLF Transport Module. Fuel is produced by the Fuel(Ore) or Fuel(H2O) recipes in the WOLF Refinery Module — each recipe will take 5 points of input availability and provide 2 points of Fuel availability. As usual one harvester will provide sufficient Ore or Water for two refineries.

The "atomic" component of a Transport Credit production line is 1 Transport Module (producing 10 _Transport Credits_ from 10 _Fuel_), 3 MHU-500 harvesters (_Water_), and 6 Refinery Modules (producing 2 *Fuel* from 5 *Water*) this needs to be supplemented with 1 abundance of _Material Kits_. To produce the target of 100 Transport Credits to get our *Fuel* and *Material Kits* to orbit we need to start off with:

- 10 x WOLF Transport Module
- 30 x MHU-500 harvesters (harvesting water)
- 60 x WOLF Refinery Module (producing fuel from water)
- local or imported abundance of 10 x Material Kits

Then you add all the habitation, power, maintenance and other infrastructure required to support this.

![VAB showing the ridiculous WOLF infrastructure required to produce 100 transport credits]()

One catch with _Transport Credits_ is that you can't deliver them elsewhere: they can only support the establishment of routes from the biome which they're produced in. Thus to use *Transport Credits* to fund transfers from KSC to Kerbin Orbit, you need to deploy this infrastructure at KSC.

### How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles

Now that you've gone to the effort of figuring out that Transport Credit infrastructure, I have a confession to make: you can make the system work to your advantage and completely eliminate the Transport Credit cost of these route-building flights.

How? Put a propellant depot in orbit, fly your transport vehicle to that depot and refuel before connecting the **WOLF Transport Computer** to the destination depot. Because the transport cost is calculated based on the difference in mass between the start and the end of the transport route, if you can restore all the consumed mass you can get a transport route that costs 0 _Transport Credits_. This is how you'd do it if you had an established MKS or stock infrastructure (for example exporting propellant from Minmus to Kerbin orbit), flying your freighter to the destination and refuelling to get it back to the origin port.

Here's the **WOLF SSTO** at the end of a 3t haul to orbit having just refuelled. How many transport credits to fly 3t to orbit? 0. Let's make this work for you!

![WOLF SSTO in Kerbin orbit with Kerbin Shipyard in background and WOLF Transport Computer action window showing route cost 0 and route payload 3]()

 Another hint for setting up zero-cost routes: you only need the propellant in the vehicle at the time that you complete the route. After that you can take all the propellant back out except for what's absolutely necessary to land back at KSC. All you are doing here is showing the WOLF Transport Computer that you have infrastructure available to support refuelling, and you're not using expendable rockets.

 You can also start the next route before putting propellant in your spacecraft. This means you start the mission with surplus mass and don't have to put as much propellant back into the spacecraft before you send it on its way.

Go back and load your "Before Transport Credits" save game.

## Bootstrapping Kerbin Orbit WOLF Infrastructure

Load the **WOLF Shipyard Launcher** that you'll find in the VAB from the tutorial ships package, under the **WOLF Tutorial Shipyard** folder. Launch that shipyard to an 80km orbit, undock the **WOLF Depot** component and establish the orbital depot.

Now to expand on this shipyard to provide a propellant supply and the ability to construct spacecraft for the expansion to Minmus and Mun. To start with, let's add a propellant supply to the shipyard. To accomplish this:

- supply the MKS resources (other than Material Kits) required to build the _Fuel Hopper_ shipyard component
- supply the propellant required to refuel a route builder (there's a trick to avoid this)
- build a route to provide WOLF MaterialKits that the shipyard
- extract the WOLF Material Kits to MKS Material Kits that the shipyard can use (this will be the focus of the following section)

The WOLF ES-96 Python will need around 15,000 fuel and oxidizer to replenish at the end of its run. One option is to send up a large tanker with the required propellant, another is to have an empty tank near the launch site (the western end of the runway), empty the propellant from the Python into this tank, start the route, then fill the Python for launch. Now you can fly to orbit for 0 transport credits cost.

With the propellant handling in place, you can rendezvous further route-building craft with this shipyard to refuel (for example the **WOLF SSTO** or **WOLF ES-96 Python**), and start building your orbital industry from there.

Use the "Connect to destination depot" action on the _Transport Computer_ to establish this route. With the **WOlF ES-96 Python** this should be 42 units of transport, which is enough to get started.

 ![WOLF ES-96 Python in Kerbin orbit with just-launched Kerbin Shipyard in background, WOLF Transport Computer action windows showing route cost 0]()

 Bring the spaceplane back to KSC.

## Extracting Resources from WOLF to MKS

With bootstrapping supplies taken care of, let's connect the abundance of _Material Kits_ and _Fuel_ produced on Kerbin to the shipyard in orbit.

Switch scenes to the **Kerbin Shipyard**. With the route established, prepare a transfer of 5 _Material Kits_ from KSC to Kerbin Orbit from the _Routes_ pane of the **WOLF Dashboard**:

- At the top of the listing is the _Manage Transfers_ button, click it to open the _Transfer Resources_ dialog
- Use the left/right arrows or the dropdown menu in the _Transfer Resources_ dialog to select the "Kerbin:KSC => Kerbin:Orbit" route
- in the top selector, find the _Material Kits_ resource and click the arrow button to the left of it
- The middle section of the _Transfer Resources_ dialog will expand to show which resource you are about to transfer, how many exist in the source depot and how many are available in the destination depot
- In the box labelled "Transfer amount" enter 20
- Do the same for the _Fuel_ resource
- Click the _Transfer_ button

Now there is a new route carrying 20 abundance of _Material Kits_ and 20 of _Fuel_ to Kerbin Orbit from KSC.

![WOLF Dashboard open to the Routes pane. Transfer Resources dialog is open, showing a transfer of material kits and fuel from the KSC depot to the Kerbin Orbit depot]()

Now open the **WOLF Dashboard** to the _Depots_ pane, expand the _Kerbin: Orbit_ depot so you can watch the figures while we configure the propellant depot, and set the hopper up:

 1. Open a (_Material Kits_) Manufacturing Hopper's PAW (for this we want the PAW and the WOLF Dashboard open)
 2. Click _Connect to depot_
 3. Click _Start hopper_

Observe that the abundance of a resource will be reduced the moment you connect the hopper to the depot, regardless of whether or not the hopper is running. Here's what it should look like for you now:

![At the shipyard in orbit, WOLF Dashboard is open to the Depots pane and the Kerbin: Orbit depot is expanded to show the incoming/outgoing/available resources. There are Material Kits outgoing to service the connected manufacturing hopper. The PAW for the manufacturing hopper is open showing the "Disconnect from depot" and "Stop hopper" buttons.]()

While you are here, keep the **WOLF Dashboard** open and see what happens when you stop the hopper and disconnect it from the depot. What you should see happen is that the local resource production will stop when you stop the hopper, and the abundance of the resource in the Kerbin Orbit depot of the **WOLF Dashboard** _Depots_ pane will be deducted from _Outgoing_ and added to _Available_. When you're ready, reconnect the hopper and start it up again.

Now connect and start the other _Material Kits_ hoppers. The combined output of three 3.75m Manufacturing Hoppers will be 15,000 _Material Kits_ a day. We'll need 34,782 for the next step. The fourth hopper is configured for Specialized Parts, which are not available yet.

## Establishing the Kerbin Shipyard

Now that resources are flowing to the shipyard, launch an **Advanced Materials Delivery** rocket (you'll find it in the WOLF Tutorial Shipyard folder). Rendezvous with the shipyard and transfer those resources across.

# WOLF Walkthrough Conclusion

We haven't finished building this walkthrough. Still to come are establishing infrastructure on Minmus, and ultimately building craft using the shipyard.

Come back later to check things out.

[MRWOLFTS]: https://github.com/MaraRinn/WOLF-Tutorial-Ships "Mara Rinn's WOLF Tutorial Ships repository"
[RDWOLF1]: https://docs.google.com/document/d/1zft2Ka9gubOYQf4CQgvReTxpnP8_LQYNyHouEjQZqjw/edit "Roverdude's introduction to WOLF"
[RDCONV]: https://kerbal-forum-uploads.s3.us-west-2.amazonaws.com/monthly_2020_12/wolf.png.53d635bf5f1f4cc0e4e2f6286409d827.png "Roverdude's resource conversion diagram"
[RDTRAN1]: https://docs.google.com/document/d/1BEqW60RrnYiVJKpAIFHAUqhdBrzbwwQ7KsaJ8hZjH4w/edit "Roverdude's introduction to transport credits"
[USIRELEASES]: https://github.com/UmbraSpaceIndustries/UmbraSpaceIndustries/releases "Umbra Space Industries combined package releases"
[CRPRELEASES]: https://github.com/UmbraSpaceIndustries/CommunityResourcePack/releases "Community Resource Pack releases"
[KSPROOT]: https://wiki.kerbalspaceprogram.com/wiki/Root_directory "Where to find the KSP root directory"

[AddOnInstallation]: Screenshots/AddonInstallation.png "Drag the contents of the USI GameData folder to teh KSP GameData folder, then drag the contents of the CRP GameData folder to the KSP GameData folder, overwriting the CommunityResourcePack folder that's already there"
[TutorialShipsInstall]: Screenshots/WOLFTutorialSaveInstall.png "Drag the WOLF Tutorial folder from the WOLF Tutorial package to the Kerba Space Program saves folder, replacing any existing save of the same name"
[WolfDepotDeployerParts]: Screenshots/WolfDepotDeployerParts.png "Runway scene with Wolf Depot Deployer showing WOLF related parts with PAWs open for Surface Scanner, WOLF Transport Computer and Bon Voyage controller"
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
[MountainsDepotDeployerConnectOriginDepot]: Screenshots/MountainsDepotDeployerConnectOriginDepot.png "Mountains scene with WOLF Depot Deployer rover showing the Transport Computer PAW. The 'connect to origin depot' action is visible."
[KSCDepotDeployerCoonectDestinationDepot]: Screenshots/KSCDepotDeployerCoonectDestinationDepot.png "WOLF Depot Deployer rover at KSC with 'connect to destination depot' action visible in the Transport Computer PAW"
[SPHDepotDeployerSubassemblies]: Screenshots/SPHDepotDeployerSubassemblies.png "SPH scene with subassemblies listing visible showing the Tutorial 5 Material Kits and Tutorial 20 Fuel subassemblies"
[KSCTransfersFromHighlandsMountainsShores]: Screenshots/KSCTransfersFromHighlandsMountainsShores.png "KSC scene with WOLF Dashboard showing transfers from highlands, mountains and shores to KSC"
[SPHRouteBuilderRover]: Screenshots/SPHRouteBuilderRover.png "SPH scene showing Route Builder Rover"
[KSCRouteBuilderRoutesBuilt]: Screenshots/KSCRouteBuilderRoutesBuilt.png "KSC scene with WOLF Dashboard open to the Routes pane. There are a number of routes built between KSC and the various biomes, expanded with the 45 payload capacity Route Builder Rover"
[ManageTransfersDiscussion]: Screenshots/ManageTransfersDiscussion.png "Manage Transfers dialog showing resources available at source and destination"
[SSTORTCOST8]: Screenshots/WOLFSSTOinOrbitWithRouteCost8.png "The WOLF SSTO craft in orbit with Transport Computer PAW open showing route cost of 8"
[ES96RTCOST85]: Screenshots/ES96PythonInOrbitWithRouteCost85.png "The ES-96 Python in orbit with Transport Computer PAW open showing route cost of 85"
