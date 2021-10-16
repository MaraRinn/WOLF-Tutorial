# WOLF Walkthrough -- Industry Without the Part Count <!-- omit in toc -->

- [WOLF for the Adventurous](#wolf-for-the-adventurous)
  - [WOLF Resource Conversions](#wolf-resource-conversions)
- [WOLF From Scratch: A Walkthrough](#wolf-from-scratch-a-walkthrough)
  - [The Plan](#the-plan)
- [Start a New Sandbox Game](#start-a-new-sandbox-game)
- [WOLF Biomes](#wolf-biomes)
  - [Surveying Harvestable Biome Resources](#surveying-harvestable-biome-resources)
  - [WOLF Dashboard -- Harvestable Resources and Depots](#wolf-dashboard----harvestable-resources-and-depots)
- [WOLF Depots](#wolf-depots)
  - [WOLF Modules](#wolf-modules)
  - [KSC Depot](#ksc-depot)
  - [WOLF Infrastructure Expansion](#wolf-infrastructure-expansion)
- [Production and Logistics](#production-and-logistics)
  - [Adding Production to WOLF Depots](#adding-production-to-wolf-depots)
  - [WOLF Routes](#wolf-routes)
  - [WOLF Transfers](#wolf-transfers)
- [Transport Routes and Transport Credits Costs](#transport-routes-and-transport-credits-costs)
  - [Quick and Dirty Transport Credit Example Flights](#quick-and-dirty-transport-credit-example-flights)
  - [Transport Module for Transport Credits](#transport-module-for-transport-credits)
  - [How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles](#how-to-avoid-transport-credit-costs-of-propellant-consuming-vehicles)
- [Extracting Resources from WOLF](#extracting-resources-from-wolf)
- [WOLF Walkthrough Conclusion](#wolf-walkthrough-conclusion)

The in-game goals for the walkthrough are roughly:

1. Small WOLF depot at KSC to produce Material Kits
1. Small WOLF depot at Kerbin Shores to produce Fuel
1. Build a shipyard in Kerbin Orbit to assemble ships from DIY kits
1. Export (WOLF-stuff) from KSC to Kerbin Orbit
2. Build an industrial base on Minmus, contrasting WOLF infrastructure vs MKS equivalents
2. Export fuel & parts from Minmus to Minmus orbit and Kerbin orbit
1. Build a shipyard in Minmus Orbit (or possibly move the Kerbin shipyard to Minmus)
3. Build a Duna mission in Minmus orbit
4. Establish a new base on Ike & Duna, starting with WOLF infrastructure

I'll be attempting to show how WOLF compares to MKS for certain tasks. The walkthrough will probably take a few hundred hours to write, so watch for a trickle of content over the next few months. I expect to spend up to two hours a day on this.

# WOLF for the Adventurous

RoverDude wrote up [this introduction to WOLF][RDWOLF1] which outlines most of what you need to know to get started. There's also RoverDude's [explanation of transport routes and transport credits][RDTRAN1] which will be expanded upon in this walkthrough. This walkthrough really only restates what is written there with a few step by step examples and an end goal of manufacturing spaceships at an orbital shipyard around Minmus.

## WOLF Resource Conversions

There are a number of differences in the resource chain between MKS and WOLF, check [RoverDude's resource conversion diagram][RDCONV] for the details.

# WOLF From Scratch: A Walkthrough

WOLF is an industry-focused extension to the industrial activities enabled in the Modular Kolonisation System. In typical mid- to late-game save files using MKS, you will have hundreds of MKS modules scattered about the place, with your planetary maps littered with various mining, refining or manufacturing facilities.  All of these facilities and the per-tick or per-second calculations they require place significant load on the KSP simulation, and loading up the models when they get in physics range can produce significant lag in the graphics engine.

The idea with WOLF is to provide the same industrial capability as MKS without the part count, without the lag, and without endless futzing around with manufacturing lines to get everything working the way you expect it to (including, for example, having to visit each industry site every few days to "catch up" with production that was supposed to happen in the meantime).

WOLF is intended as an enhancement to MKS industry — even if you haven't got enough parts in your infrastructure to invoke the Kraken, WOLF can still be handy for you by providing part-free and attention-free resource production and transfers between biomes on the same planet, between surface and orbit, and between worlds.

## The Plan

For the purposes of this guide, our goal is to set up a shipyard in Minmus Orbit and provide it with resources harvested using WOLF, with the minimal possible part count.

1. Produce ship building materials and fuel on Kerbin
1. Transfer those materials to Kerbin Orbit
1. Build a spacecraft in Kerbin Orbit from materials provided by WOLF
1. Produce ship building materials and fuel on Minmus
1. Transfer those materials to Minmus Orbit
1. Build a spacecraft in Minmus orbit from materials provided by WOLF

Note that the rules will change between these biomes, but from the end of this walkthrough you'll have the knowledge you need to establish infrastructure everywhere else in the Kerbin system.

Along the way there will be a number of pre-built vehicles for you to use so you aren't left wondering what pieces are needed to do various WOLF tasks.

Throughout this guide you'll see reference to PAW, which is the "Part Action Window" that you typically open up by right-clicking on a part.

# Start a New Sandbox Game

Let's have a look at how WOLF biomes and production chains work. Create a new sandbox game. Ensure that when you create the game, under _Difficulty Options_ > _Advanced_, you **deselect** _Enable Kerbal Experience_.  This will give all of your Kerbals maximum experience.  Since Kerbal experience affects resource production, the rest of this tutorial will make more sense. For the rest of this walkthrough we'll assume you called your game "WOLF Tutorial".

If you want to use the tutorial ships, get the [WOLF Tutorial Ships][MRWOLFTS] release file and unpack it now. Put put the **Ships** and **Subassemblies** folders into your save directory.

![The Kerbal Space Program saves directory showing the WOLF Tutorial save folder. Alongside that is the WOLF_Tutorial_Ships ZIP file contents. An arrow indicates that the contents of the ZIP file should be dragged directly to the WOLF Tutorial save folder]()

# WOLF Biomes

The foundation of industry in WOLF is the "WOLF Biome" and its associated depot. The basic idea is that you dedicate a "WOLF Biome" to certain types of activity, and either transfer resources to other biome depots for further processing, or extract resources through WOLF "Hoppers" for use in the MKS industry that you're familiar with.

You can imagine WOLF Biomes as stuff that happens "behind the scenes" in the KSP world. You build up the industrial machinery to produce the goods that you need, hand that assembled factory to WOLF, then WOLF stops rendering those parts. The entire production line becomes an abstraction, with hundreds of parts abstracted away to a handful of numbers.

Where the world of MKS is concerned with resource concentrations, extractor efficiency, engineer multipliers and storage capacity, the world of WOLF is concerned with resource availability, expressed as one single number. Each WOLF biome has a certain availability for each resource. There are no concentrations to worry about, nor are there survey maps to ponder and prime locations to target for resource extraction. There's just a number for each resource in each biome.

The major catch with WOLF is that once you've committed to a certain production chain, there's no taking it back and making changes. With MKS infrastructure you can start producing Transport Credits then pivot to producing Material Kits and Specialised Parts by changing the recipes for a bunch of modules. With WOLF infrastructure, once you start producing something, that production chain will stay in place for the rest of your game.

## Surveying Harvestable Biome Resources

As soon as you start the new sandbox game, head to the SPH and build yourself a survey rover. If you're using the tutorial ships, use the **WOLF Depot Deployer** for this section. You'll need the **Surface Scanning Module** from the stock game. Here's my **WOLF Depot Deployer** which has a **Surface Scanning Module**, the **WOLF Transport Computer** which we'll discuss later, and the **Bon Voyage Autopilot** module (automatically incorporated into the controlling part) which I highly recommend (but more about that later).

![The WOLF Depot Deployer rover with important components marked: surface scanner, transport computer and bon voyage autopilot][WolfDepotDeployerParts]

Launch this vessel and open the **Surface Scanning Module** PAW (Part Action Window, aka right-click menu). You'll see the usual MKS resource details in the Surface Scanning Module's window. For each resource there's a concentration tagged "[Surf]" (because it's a resource on the surface) which is then combined with harvester efficiency to determine how much of that resource you'll be extracting per second using MKS parts. WOLF doesn't use that data.

Now open the **WOLF Dashboard** and select the *Harvestable Resources* pane. You'll see that it's empty right now.

![WOLF Dashboard showing no biomes with harvestable resources][WolfDashboardHarvestableResourcesEmpty]

Looking back to the **Surface Scanning Module** PAW, there is one line under the MKS resources list specifying the "WOLF biome". You'll also see the "Survey WOLF Biome" action. Click it!

Recover this vessel.

## WOLF Dashboard -- Harvestable Resources and Depots

Now to check those resources. Switch scenes to the SPH and open the WOLF dashboard, then click the *Harvestable Resources* button:

![SPH scene showing WOLF Dashboard open to Harvestable Resources pane][WolfDashboardHarvestableResourcesScannedBiome]

You'll have one Body/Biome option: Kerbin:KSC. There are four columns here which help you understand what resources you have access to:

1. Resource name, which represents the WOLF version of resources (as opposed to the "surface" resources)
2. Abundance, which is the WOLF equivalent to surface resource "concentration" (but it works completely differently)
3. Harvested, which is how much of the abundance you are currently extracting
4. Remaining, which is how much of the abundance is left to extract

The *Depots* pane lists all your active WOLF Depots. Since you have no depots yet, it's empty.

![SPH scene showing WOLF Dashboard open to empty Depots pane][SPHWOLFEMPTY]

# WOLF Depots

Now that the KSC WOLF Biome is surveyed, we need to deploy a WOLF depot. Before we do that though, have a quick look at the modules that make up the WOLF system, then we'll go over the rules of deploying them.

## WOLF Modules

From the SPH scene, start a new ship and open the *Planner* pane in the **WOLF Dashboard**, and select the "WOLF" parts group in the selection pane on the left, then start planning this depot with a **WOLF Fabricator Module**. Set the **WOLF Fabricator Module** to produce *Material Kits*:

![SPH scene showing WOLF Dashboard open on Planning pane with a WOLF Fabricator Module as the first piece of the vessel under construction. The PAW shows Material Kits as the recipe.][SPHsceneFabricatorModuleWOLFDashboardPlanner]

There are two groups of values in the *Planning* pane: the first is the *depot summary* showing resources processed inside your WOLF Depot, the second is the harvestable resource report which shows the same details from the *Harvestable Resources* pane showing those resources that you are actually harvesting from this WOLF Biome. Since the fabricator you just added has not been configured it will be using the *Material Kits* recipe. The *Planner* now shows that you have a deficit of power, maintenance, technician crew point, chemicals, metals and polymers.

Add a *WOLF Maintenance Module* and a *WOLF Power Module*. Now you'll see that you have surplus maintenance and power, but have incurred a deficit in various crew points. At this point, add a **Karibou Passenger Cabin** onto your WOLF modules to get 10 seats for crew and add an Engineer, Kolonist, Mechanic and Technician to your crew -- each crew member will add 10 crew points for their respective speciality. Add a probe core to the passenger cabin (I tend to use the *Avionics Package* since it's small and cheap and provides all the necessary functionality). That's the crew points taken care of but now you have habitation and life support to worry about -- that's easily resolved by adding the **WOLF Habitation Module** and **WOLF Life Support Module**, leaving you with a deficit of food, oxygen and water (and the chemicals, metals and polymers for the fabricator).

Oxygen and water are avialable as *Harvestable Resources* which means we can supply the depot with those resources using **WOLF MHU-550 Bulk Harvester** modules. Add two of those, configure one to harvest water and the other to harvest oxygen.

In the harvestable resource section of the planner you'll see that the harvesters are using 5 units each of the 1000 abundance of oxygen and 750 abundance of water, leaving 995 and 745 available. Note the numbers in the "Harvested" column: "0 (-5)" means that the KSC Biome Depot is currently harvesting 0 of that resource, and the craft that we are building will be harvesting 5 (thus reducing the abundance by 5).

Food is produced by an agricultural module or bioreactor module. Add a **WOLF Agriculture Module** and set it up to use the *Farm* recipe. This has now added a demand for a farmer, dirt and fertiliser. Add a farmer to your crew, then you'll need three **WOLF MHU-550 Bulk Harvester** modules to get the dirt you need. To get fertiliser, we'll add a **WOLF MHU-559 Bulk Harvester** to harvest *gypsum*, then add two **WOLF Extractor Module** set to convert the *gypsum* to *fertiliser* (technically you only need one to feed the farm, but the harvester can feed two extractors). The two extractor modules have added a deficit for *Lab* resource which is supplied by a **WOLF Science Module** so add one of those onto your growing pile of infrastructure, then add the scientist and medic crew that are needed for the science module.

Finally, add the harvesters and refineries required for the chemicals (feed stock is minerals), metals (feed stock is metallic ore) and polymers (feed stock is substrates). To finish off this infrastructure install add a **WOLF Power Module**, and you should no longer have any deficits in the *Planner*. *Note* that some of the *Material Kits* produced by this infrastructure has immediately been consumed by other parts of the infrastructure (the habitation, life support and maintenance modules each consume 1 *Material Kits* abundance).

Before we can deploy this infrastructure we need to establish the depot itself. To do this, add a decoupler and a **WOLF Depot Module** with a probe core. When we launch this craft we'll decouple the depot, which needs a controlling part in order to be useful.

What a beautiful creation! Did yours turn out like mine?

![SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance][SPH2MATKITS]

If you're familiar with the production chains from MKS you'll see that this WOLF infrastructure is a lot simpler than what is required in MKS, for example each **WOLF MHU-550 Bulk Harvester** is roughly equivalent to a mining ship with a logistics hub attached to the planetary warehouse -- each of those mining ships will be a dozen parts given the need for drills, ore tanks, radiators, power source, probe core and whatever else you normally put on your mining ships. That part count can severely bulk out your save file size, and slow your game to a crawl any time you load a production facility into physics range.

## KSC Depot

Launch that craft you just created. You're going to separate the depot and immediately hand it over to the WOLF system.

**Warning: Any other parts attached to the WOLF modules will be consumed along with the WOLF modules when you hand them over to the biome depot, including any crew. In addition the WOLF Depot can not have any other WOLF components attached, not even the Survey Scanner.**

Now that you have your two-component craft separated (the WOLF Depot Module and a cheap probe core), it's time to commit them to the void! I mean … establish your KSC Biome Depot:

![WOLF Depot Module with PAW showing "Establish Depot" action.][WOLFDEPOTPAWESTABLISH]

Just select the *Establish Depot* action for the WOLF Depot Module, and the craft will disappear. It belongs to WOLF now.

Check out the Depots pane of the WOLF Dashboard now:

![WOLF Dashboard showing the new KSC Biome Depot with bonus resources awarded to Kerbin-based depots][WOLFDASHKERBINDEPOTBONUS]

That depot has given us 1 Food, 1 Oxygen, 5 Material Kits, 5 Water, and 10 Power. This will significantly reduce the amount of infrastructure we need to get started — but remember that these bonus resources only apply to WOLF biomes on Kerbin.

Switch to the remaining craft and select the *Connect to depot* action for one of the WOLF modules. With that done, open the **WOLF Dashboard** and check the *Depots* pane.

![Runway scene with WOLF Dashboard showing new production added][RUNWAYWOLFDASHNEWKSCDEPOTPRODUCTION]

## WOLF Infrastructure Expansion

To prepare for the next stage of the tutorial, let's expand the biome depots on Kerbin a little. To do that, we'll build ourselves a rover to help deploy the depot components. Why? Because sometimes the best way to get stuff to where you need it is to stick wheels or rockets on it.

**I highly recommend you get the Bon Voyage add-on, it makes the process of deploying biome depots much, much easier**

![This assemblage of WOLF modules and wheels will make life easier for us, trust me][RUNWAYDEPOTBONVOYAGE]

The ingredients are:

  + WOLF Depot Deployer Rover (based on the Karibou rover)
  + Tutorial Basic Depot subassembly
    + Karibou Flatbeds containing WOLF modules attached to rover via Clamp-O-Tron Sr
    + WOLF Depot & probe core on a decoupler
    + Engineer
    + Kolonist
    + Mechanic

**Remember to add the Engineer, Kolonist and Mechanic** (mentioned in the subassembly description) to the Karibou Passenger Cabin in the trailer before launching. 

Once you've launched the rover, activate the parking brake to stop it rolling down the runway, then activate Action Group 10 (press "0" on the keyboard) to turn on the power supply. Use the **Bon Voyage** autopilot to move the rover to *Kerbin Shores* (-0.04, -74.9).

Activate the Bon Voyage autopilot and then change scene to the Space Centre. Wait for the rover to reach its destination -- warp can help here -- and then switch back to the rover.

The process for establishing a depot using this rover is:

1. scan the WOLF biome
2. decouple the depot module and establish the depot
3. undock the trailer and connect it to the depot

![Kerbin Shores scene with WOLF Depot Deployer - Depot and trailer are decoupled and Surface Scanner PAW is open. There are numbers 1, 2 and 3 indicating the order of operations.][KERBINSHORESDEPOTDEPLOYMENT]

Once you have completed those operations you should see the new depot established with the Mechanic, Kolonist and Engineer resources added:

![Kerbin Shores scene with WOLF Dashboard open to Depots pane showing new Kerbin Shores depot][KERBINSHORESDEPOTDASHBOARD]

You can recover this vessel from where it's parked, drive it back to the KSC manually to recover it, or be brave and try to use Bon Voyage to send the rover back to (-0.1, -74.647) which parks it next to the astronaut complex at KSC.

Now repeat this process to deploy this simple infrastructure to:

  + Grasslands (0.0 -75.38)
  + Highlands (1.741, -77.339)
  + Mountains (0.637, -78.659)
  + Desert (1.472, -86.435)

Remember the basic process for establishing a new biome depot is:

 + Prepare the WOLF Depot Deployer rover with the WOLF Basic Depot subsystem
   + Required crew is Engineer, Kolonist, Mechanic
 + On the runway, lock the brakes and start the reactor
 + Move the rover to the new biome
 + Survey the WOLF Biome
 + Decouple the **WOLF Depot** component
 + Undock the **Tutorial Basic Depot** assembly
 + Use the *Establish Depot* action on the **WOLF Depot**
 + Use the *Connect to depot* action on the **Tutorial Basic Depot** assembly
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover back to the destination biome for the route (for our purposes, the KSC)
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Recover the rover

# Production and Logistics

Now that the basic depots are established, it's time to increase production of the resources we need for spaceship construction and get those resource so where we need them.

## Adding Production to WOLF Depots

To build spacecraft at the orbital shipyard, you'll need *Material Kits*, *Specialized Parts*, *Alloys*, *Electronics*, *Prototypes*, *Robotics* and *Synthetics*.

Let's start with the *Alloys*, building a *WOLF Depot Deployer Rover* trailer from scratch. To start with just assemble a **Karibou Passenger Cabin** and **Karibou Flatbed Wheel Bay**, add some wheels and an avionics package (this starting trailer is available as **WOLF Depot Deployer Trailer** in the subassemblies listing). Add a **WOLF Fabricator Module** and set its recipe to *Alloys*. Now you have a deficit of *Rare Metals*, which are collected by a harvester module. Add a **WOLF MHU-500 Bulk Harvester** and set its recipe to *Rare Metals*. There's a deficit of *Rare Metals* in this biome, so check through the remaining depots to see if you can find *Rare Metals*.

Unfortunately, it turns out that *Rare Metals* are not a thing in Kerbin biomes. Okay, what about the others? *Electronics* requires *Synthetics* which in turn requires *ExoticMinerals* ... which it turns out are not available on Kerbin either. Maybe *Prototypes* then? No, they require *Electronics* which we can't manufacture on Kerbin. *Robotics* are in the same boat, requiring *Alloys*. Last on the list are *Specialized Parts* but it turns out that they require *Rare Metals*.

The only spaceship-building things we can make on Kerbin using WOLF infrastructure are *Material Kits* and *Fuel*. What do we do about the rest? For the boot-strapping stage, any time we need *Specialized Parts*, *Alloys*, *Electronics*, *Prototypes*, *Robotics* or *Synthetics* the options are to buy them (create a new craft with a resource container full of the resource we're after), set up WOLF infrastructure where we *can* find them and transport the supplies to the shipyard, or find some surface resources to extract and perform all the industry using MKS (the shipyard is MKS infrastructure so this is perfectly acceptable).

For this walkthrough we're not going to go overboard with production, and as far as the other spaceship building materials go we'll focus on expanding the WOLF infrastructure to find them. Tens of abundance for *Material Kits* and *Fuel* will be enough to get us to Minmus. Let's get started, the sooner we get to Minmus the sooner we find what resources are available there!

Clear the SPH build area and load up the **WOLF Depot Deployer Rover**, add the **Tutorial 5 Material Kits** subassembly, put a Miner and a Technician in the passenger cabin (as indicated in the subassembly description), and check the *Planner* pane of the **WOLF Dashboard** to see which biome will have the most resources left over after we commit to this *Material Kit* production. For me this is the Mountains biome which had 100 *Minerals* abundance before this infrastructure took 10 away. Launch the rover and send it to the Mountains biome (0.637, -78.659). Undock the trailer and connect the new components to the depot. **Leave the rover here for the moment**, it's going to start setting up transport routes now.

## WOLF Routes

It's all well and good having that *Material Kits* production chain set up in the mountains, but what do we do with the output? The next step is getting those resources to orbit, where we want to use Material Kits and other resources to build spaceships.

WOLF handles transport of resources from one biome to another by way of *Routes* which are path established for *Transfers*. You establish a route by travelling between biomes using the WOLF Transport Computer. This will add *Route* between the source biome and the destination biome. You can then add resources to *Transfers* on that route. Each transfer has a certain capacity, you'll allocate an abundance of resource to a transfer, then the abundance of that resource will be reduced in the source biome and increased in the target biome.

With the rover parked in the mountains from the previous infrastructure deployment, start a new transport route using the *Connect to origin depot* action in the **WOLF Transport Computer** PAW:

![Mountains scene with WOLF Depot Deployer rover showing the Transport Computer PAW. The 'connect to origin depot' action is visible.][MountainsDepotDeployerConnectOriginDepot]

Drive that rover back to the KSC and activate the *Connect to destination depot* action from the **WOLF Transport Computer** PAW.

![WOLF Depot Deployer rover at KSC with 'connect to destination depot' action visible in the Transport Computer PAW][KSCDepotDeployerCoonectDestinationDepot]

On top of the depots you've just established, expand your infrastructure to produce *Material Kits* and *Fuel*. The tutorial pack includes a couple of example payloads for the **WOLF Depot Deployer** which will add 5 Material Kits production or 20 Fuel production to a depot. Use the planner to decide where to deploy them, and make sure you add the required crew and any extra production you need such as power, maintenance, life support (check with the *Planner* pane in the **WOLF Dashboard**).

![SPH scene with subassemblies listing visible showing the Tutorial 5 Material Kits and Tutorial 20 Fuel subassemblies][SPHDepotDeployerSubassemblies]

**Fuel Production** is very demanding of water. If you combine the **WOLF Depot Deployer** with a **Tutorial 20 Fuel** subassembly, then open the **WOLF Dashboard** to show the *Planner*, you should be able to cycle through the biomes you've surveyed to determine which has the greatest supply of water. For my game this was the *Highlands* with over 800 water supply, though I also set up production of *Fuel* at the *Kerbin Shore* biome just outside the KSC. You can repeat this with the **Tutorial 5 Material Kits** subassembly, which is dependent on *Mineral*, *Metallic Ore* and *Substrate*. For my game the biome with the greatest abundance of *Metallic Ore*  was the *Mountains*.

Here's what my transport routes and production look like with two depots producing 20 *Fuel* and two depots producing an extra 5 *Material Kits* each:

![KSC scene with WOLF Dashboard showing transfers from highlands, mountains and shores to KSC][KSCTransfersFromHighlandsMountainsShores]

Note that with 20 *Fuel* abundance I'd have to run the rover back and forth 7 times. That seems a lot like hard work so I'll slap together a rover with three of the largest WOLF payload Kontainers and call it the **WOLF Route Builder Rover**. This rover has 45 payload capacity so it'll build my fuel routes quite quickly. It also has a trailer subassembly, so if you were having trouble with the **WOLF Depot Deployer** due to the weight of the payloads it was hauling (I sometimes had problems with wheels popping or suspension bouncing) give this route builder rover a try.

![SPH scene with WOLF Route Builder Rover][SPHRouteBuilderRover]

Take that rover out to each of the depots to build a route to KSC, that should keep you covered for the entire walkthrough. Remember the procedure for building these routes with the tutorial rovers is:

 + Launch the rover on its own
 + On the runway, lock the brakes (icon in the HUD) and start the reactor (0)
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover to the remote biome
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover back to the KSC
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Repeat steps 3-8 as often as you need

Here's one I prepared earlier (just a bunch of routes with a decent amount of payload capacity):

![KSC scene with WOLF Dashboard open to the Routes pane][KSCRouteBuilderRoutesBuilt]

## WOLF Transfers

In this walkthrough the main purpose of setting up these biomes is to get Material Kits and Fuel to orbit to start building spaceships. There are no doubt untapped opportunities in your biomes (eg: the ability to send one resource from a biome with excess to another biome with a deficit), but for now we have plenty of output to get to orbit.

Open the WOLF dashboard to the *Routes* pane and open the *Manage Transfers* dialog:

![Manage Transfers dialog showing resources available at source and destination][ManageTransfersDiscussion]

This dialog is use to set up resource transfers over a route. The numbers visible in this dialog show:

 + The resources and their availability at the source biome depot
 + The selected resource
 + The availability of that resource in the source biome depot
 + The current available/incoming values of the resource in the destination biome
 + The list of resources that you have already selected for transfer on this route
 + How much payload capacity is left for transfers
 + How much payload capacity has already been used

How much of a resource you can add to transfers on this route is the smaller number of the availability of the resource or the available payload. In the example above there are 20 Material Kit points available, and the payload has space for all of them with room to spare.

Click the downward pointing triangle next to *Material Kits* in the available resources list.

If you have more Material Kit availability than will fit in the payload, you can simply connect the route more times with your route-building vehicles to increase the payload size.

Set the *Transfer Amount* to 1, then click *Transfer*. You should notice:

 + The "Origin" availability will drop by 1
 + The "Destination" availability will increase by 1
 + The "Available Payload" will drop by 1/1 (eg from 7/10 to 8/11)

You'll see a new row in the bottom table displaying the transfer you've just organised. Add another transfer of 5 Material Kits, and you'll see the details in the Resource/Origin/Destination values and the row in the bottom table updated to show the new payload contents.

The *Routes* pane of the **WOLF Dashboard** will now show the resources being transferred between the various biomes and the KSC. In my example I've set up the production, routes and transfers to provide 20 surplus *Material Kits* and 20 surplus *Fuel* for the KSC depot. I want to get that *abundance* to Kerbin orbit, so it's time to talk about transport credits which should be familiar to people who have used MKS in the past, and then we can talk about how to get *abundance* out of the WOLF system and turn it into materials for MKS activities.

Go ahead and get all the surplus *Material Kits* and *Fuel* abundance on transfers to KSC:

![WOLF Dashboard open to the Routes pane displaying the various transfers that have been arranged over the established routes]()

# Transport Routes and Transport Credits Costs

Up till now we've kept the transport routes simple by only connecting biomes that can be reached without expending mass. It's time to kick it up a notch and learn about Transport Credits, which is an abstraction of the process of building launch vehicles, fuelling them and launching payloads to orbit (or deorbiting payloads to bring them to the surface).

The first thing we'll do here is a few test flights to understand how many *Transport Credits* we'll need for sending supplies to orbit (or roughly, how Transport Credits correlate to delta-v and ship size). Let's start with a "small" rocket, a medium sized rocket, a 3t payload SSTO spaceplane, and a 55t payload SSTO spaceplane. Note that with enough Transport Credits each flight will add a certain payload capacity to the available routes from KSC to Kerbin Orbit, with the payload capacity being proportional to the payload capacity of each launch vehicle. We'll get the gory details soon!

**Save your game here**, give it a name like "Before Transport Credits". Skip ahead to the next section if you want to know why, but we're going to be restoring to this point after experimenting with *Transport Credits*.

## Quick and Dirty Transport Credit Example Flights

In the VAB, put together a rocket that can carry a single 3t **2.5m WOLF Cargo Kontainer** to orbit using 2.5m parts. The **WOLF Tutorial 2.5m SSTO* contains:

 + 2.5m WOLF Cargo Kontainer
 + RC-001S Remote Guidance Unit
 + Protective Rocket Nosecone Mk7
 + Rockomax Jumbo-64 Fuel Tank
 + RE-I5 "Skipper" Liquid Fuel Engine
 + WOLF Transport Computer

Send that to the launch pad, select the *Connect to Origin Depot* action on the **WOLF Transport Computer**, and launch the rocket to a 80km orbit. Once in orbit, check the "Route cost" reported by the **WOLF Transport Computer**.

If you try to use the **Connect to Destination Depot** action, you should get an error message about needing more Transport Credits to complete that operation. Revert to launch, and run it a few times just to see that the "Route cost" is predictable. My flights came up with a route cost of around 30 *Transport Credits* which works out to a *Transport Credits Per Unit* cost of around 10.

![Sample flight of 2.5m rocket showing a route cost of 30](https://i.imgur.com/Iq5PW4k.jpg)

Revert to vehicle assembly and do the same thing with a 3.75m rocket. The *WOLF Tutorial 3.75m SSTO* is roughly:

 + 2 x 3.75m WOLF Cargo Kontainer
 + Protective Rocket Nosecone Mk7
 + RC-L01 Remote Guidance Unit
 + Advanced Reaction Wheel Module, Large
 + WOLF Transport Computer
 + Kerbodyne S3-14400 Tank
 + S3 KS-24x4 "Mammoth" Liquid Fuel Engine

![Sample flight of 3.75m rocket showing a route cost of 85]()

Send that to the launch pad, select the "connect to origin depot" on the WOLF Transport Computer, and launch the rocket to an 80km orbit. As before, check the "route cost", revert to launch and run the process again to show that the "route cost" is predictable. My flights came up with a route cost of 86, giving a *Transport Credit Per Unit* cost of around 6.14. Revert to vehicle assembly when done.

Now do the same thing with spaceplanes. The two I use are the **WOLF SSTO** and the [ES-96 Python by Juggernoob](https://steamcommunity.com/sharedfiles/filedetails/?id=1722161481) which I find to be an aesthetically pleasing and easy-to-fly SSTO spaceplanes.

**Instructions:** for both these spaceplanes the procedure to get to orbit is:

 + set throttle to maximum
 + turn SAS on to stability assist
 + stage once to light the engines
 + rotate off the runway to 10 degrees at about 140m/s
 + hold the nose at 10 degrees for the whole flight through the atmosphere
 + when the airbreathing mode is insufficient to keep accelerating, switch to closed cycle (Action Group 1)
 + push the apoapsis to 80km and cut the throttle
 + cruise to the top of the atmosphere, plot a circularisation burn at apoapsis
 + execute that burn.

My flights with **WOLF SSTO** ended up producing routes with a cost of 9 for 3t cargo, or about 3 credits/unit.

![Sample flight of WOLF SSTO showing route cost of 8 for 3t cargo]()

The **ES-96 Python** got to orbit in the order of 90 Credits for 42t. The **WOLF ES-96 Python** in the tutorial ships package has already been modified and will automatically start the transport route when you stage to launch (the **Transport Computer** is in the cargo bay with the *Connect to origin depot* action linked to the *stage* action group).

![Sample flight of WOLF ES-96 PYTHON showing route cost of 85 for 42t]()

## Transport Module for Transport Credits

How do we produce Transport Credits? The short version is that *Transport Credits* are produced by the *WOLF Transport Module*. By now you should be familiar with the drill: start assembling a new WOLF infrastructure component with the WOLF Dashboard open to the Planning pane, beginning with the WOLF Transport Module. Fuel is produced by the Fuel(Ore) or Fuel(H2O) recipes in the WOLF Refinery Module — each recipe will take 5 points of input availability and provide 2 points of Fuel availability. As usual one harvester will provide sufficient Ore or Water for two refineries.

The "atomic" component of a Transport Credit production line is 1 Transport Module (producing 10 *Transport Credits* from 10 *Fuel*), 3 MHU-500 harvesters (*Water*), and 6 Refinery Modules (producing 2 *Fuel* from 5 *Water*) this needs to be supplemented with 1 abundance of *Material Kits*. To produce the target of 100 Transport Credits to get our *Fuel* and *Material Kits* to orbit we need to start off with:

 + 10 x WOLF Transport Module
 + 30 x MHU-500 harvesters (harvesting water)
 + 60 x WOLF Refinery Module (producing fuel from water)
 + local or imported abundance of 10 x Material Kits

Then you add all the habitation, power, maintenance and other infrastructure required to support this.

![VAB showing the ridiculous WOLF infrastructure required to produce 100 transport credits]()

One catch with *Transport Credits* is that you can't deliver them elsewhere: they can only support the establishment of routes from the biome which they're produced in. Thus to use *Transport Credits* to fund transfers from Fuel-rich KSC to Fuel-poor Kerbin Orbit, you need to deploy this infrastructure at KSC.

## How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles

Now that you've gone to the effort of figuring out that Transport Credit infrastructure, I have a confession to make. You can make the system work to your advantage and completely eliminate the Transport Credit cost of these route-building flights.

How? Put a propellant depot in orbit, fly your transport vehicle to that depot and refuel before connecting the **WOLF Transport Computer** to the destination depot -- since the transport cost is calculated based on the difference in mass between the start and the end of the transport route, if you can restore all the consumed mass you can get a transport route that costs 0 *Transport Credits*. This is how you'd do it if you had an established MKS or stock infrastructure (for example exporting propellant from Minmus to Kerbin orbit), flying your freighter to the destination and refuelling to get it back to the origin port.

Here's the **WOLF ES-96 PYTHON** at the end of a 3t haul to orbit having just refuelled. How many transport credits to fly 3t to orbit? 0. Let's make this work for you!

![WOLF ES-96 Python in Kerbin orbit with Propellant Depot in background and WOLF Transport Computer action window showing route cost 0 and route payload 42]()

Go back and load your "Before Transport Credits" save game.

If you're happy to take a shortcut for the purpose of the walkthrough, load the **WOLF Type 3 Propellant Depot** that you'll find in the SPH from the tutorial ships package. Cheat that craft to orbit (Alt+F12, Cheats, Set Orbit, use 690000 for the SMA), undock the **WOLF Depot** component and establish the orbital depot. You can rendezvous a route-building craft with this depot to refuel (for example the **WOLF SSTO** or **WOLF ES-96 Python**), and start building your orbital industry from there.

If you want to build your own depot, the key components here are the **WOLF Fuel Hopper** (available in 2.5m or 3.75m versions) and the *local storage* for the propellant types the hopper will be producing (don't forget the **WOLF Depot Module** with a probe core and a decoupler). There's no built-in storage for the hopper, its only purpose is to extract resources from the WOLF infrastructure and deliver them to Stock/MKS infrastructure at which point all the usual Stock/MKS rules apply -- most notably having storage for materials to be consumed while the production facility is packed up out of physics range. Note that the **2.5m WOLF Fuel Hopper** will convert 2 *Fuel* abundance into 180 *Liquid Fuel* and 220 *Oxidiser* per day. Refilling the 1440 *Liquid Fuel* and 1760 *Oxidiser* of the orbital depot's storage tank will take about 8 days. Refuelling the **WOLF SSTO** will take up to 2000 *Liquid Fuel* though getting a zero route cost at 80x80km should cost far less.

 Another hint for setting up zero-cost routes: you only need the propellant in the vehicle at the time that you complete the route. After that you can take all the propellant back out except for what's absolutely necessary to land back at KSC. All you are doing here is showing the WOLF Transport Computer that you have infrastructure available to support refuelling, and you're not using expendable rockets.

# Extracting Resources from WOLF

With bootstrapping supplies taken care of, let's connect the abundance of *Fuel* produced on Kerbin to the depot in orbit. With the route you just established, prepare a transfer of 20 *Fuel* from KSC to Kerbin Orbit:

![Transfer Resources dialog showing a transfer of fuel and material kits from the KSC depot to the Kerbin Orbit depot]()

Now open the **WOLF Dashboard** to the *Depots* pane, expand the *Kerbin: Orbit* depot so you can watch the figures while we configure the propellant depot, and set the hopper up:

 1. Open the hopper's PAW (for this we want the PAW and the WOLF Dashboard open)
 1. Click *Connect to depot*
 2. Click *Start hopper*

Observe that the abundance of a resource will be reduced the moment you connect the hopper to the depot, regardless of whether or not the hopper is running. Here's what it should look like for you now:

![At the propellant depot in orbit, WOLF Dashboard is open to the Depots pane and the Kerbin: Orbit depot is expanded to show the incoming/outgoing/available resources. There is fuel outgoing to service the two connected fuel hoppers.]()

While you are here, keep the **WOLF Dashboard** open and see what happens when you stop the hopper and disconnect it from the depot. What you should see happen is that the local resource production will stop when you stop the hopper, and the abundance of *Fuel* in the Kerbin Orbit depot will change from *Outgoing* to *Available*. When you're ready, reconnect the hopper and start it up again. With the 20 fuel now available for the Kerbin Orbit depot you should be able to connect 4 of the 3.75m fuel hoppers.

# WOLF Walkthrough Conclusion

We haven't finished building this walkthrough. Still to come are establishing infrastructure on Minmus, and ultimately building craft using the shipyard.

Come back later to check things out.

[MRWOLFTS]: https://github.com/MaraRinn/WOLF-Tutorial-Ships "Mara Rinn's WOLF Tutorial Ships repository"
[RDWOLF1]: https://docs.google.com/document/d/1zft2Ka9gubOYQf4CQgvReTxpnP8_LQYNyHouEjQZqjw/edit "Roverdude's introduction to WOLF"
[RDCONV]: https://kerbal-forum-uploads.s3.us-west-2.amazonaws.com/monthly_2020_12/wolf.png.53d635bf5f1f4cc0e4e2f6286409d827.png "Roverdude's resource conversion diagram"
[RDTRAN1]: https://docs.google.com/document/d/1BEqW60RrnYiVJKpAIFHAUqhdBrzbwwQ7KsaJ8hZjH4w/edit "Roverdude's introduction to transport credits"

[WolfDepotDeployerParts]: Screenshots/WolfDepotDeployerParts.png "Runway scene with Wolf Depot Deployer showing WOLF related parts with PAWs open for Surface Scanner, WOLF Transport Computer and Bon Voyage controller"
[WolfDashboardHarvestableResourcesEmpty]: Screenshots/WolfDashboardHarvestableResourcesEmpty.png "Runway scene with WOLF Dashboard open to Harvestable Resources pane showing no biomes with harvestable resources because they have not been scanned"
[WolfDashboardHarvestableResourcesScannedBiome]: Screenshots/WolfDashboardHarvestableResourcesScannedBiome.png "SPH scene with WOLF Dashboard open to Harvestable Resources pane showing resource abundance for freshly scanned biome"
[SPHWOLFEMPTY]: Screenshots/SPHWOLFEMPTY.png "SPH scene with WOLF Dashboard open to Depots pane showing no depots"
[SPHsceneFabricatorModuleWOLFDashboardPlanner]: Screenshots/SPHsceneFabricatorModuleWOLFDashboardPlanner "SPH scene with WOLF Dashboard open to Planner pane and WOLF Fabricator Module as the first part of a new vessel"
[SPHSCENE2MATKITS]: Screenshots/SMHSCENE2MATKITS.png "SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance"
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
