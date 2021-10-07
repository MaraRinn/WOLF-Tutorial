+ [WOLF For The Adventurous](#wolf-for-the-adventurous)
  + [WOLF Resource Conversions](#wolf-resource-conversions)
+ [WOLF From Scratch: A Walkthrough](#wolf-from-scratch-a-walkthrough)
  + Correctly installing the USI mods
  + [The Plan](#the-plan) (what the walkthrough will cover)
  + [WOLF Biomes](#wolf-biomes)
  + [WOLF Modules](#wolf-modules)
  + [KSC Biome: Depot](#ksc-biome-depot)
  + [KSC Biome: Fabrication Module for Material Kits](#ksc-biome-fabrication-module-for-material-kits)
  + [WOLF Transport Routes and Shipments](#wolf-transport-routes-and-shipments)
    + [WOLF Infrastructure Expansion](#wolf-infrastructure-expansion)
    + [WOLF Transport Routes](#wolf-transport-routes)
    + [WOLF Shipments](#wolf-shipments)
  + [KSC Biome: Transport Module for Transport Credits](#ksc-biome-transport-module-for-transport-credits)
+ [Transport Routes and Transport Credit Costs](#transport-routes-and-transport-credits-costs)
  + [Quick and Dirty Transport Credit Example Flights](#quick-and-dirty-transport-credit-example-flights)
  + [KSC Biome: Transport Module for Transport Credits](#ksc-biome-transport-module-for-transport-credits)
  + [WOLF Hopper for Resource Delivery](#wolf-hopper-for-resource-delivery)
+ Intermediate WOLF
  + Combining WOLF with MKS
    + WOLF Material Kits + MKS Specialized Parts on Kerbin
    + WOLF, MKS and Stock fuel plant on Minmus
+ How I Learned to Stop Worrying and Love Transport Credits
  + Sample vehicles (PackRat, SSTO spaceplane, NTR interplanetary freighter)
  + Strategies for optimising routes
    + Surface-to-Surface
    + Surface-to-Orbit
    + Orbit-to-Surface
    + Orbit-to-Orbit

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

RoverDude wrote up [this introduction to WOLF](https://docs.google.com/document/d/1zft2Ka9gubOYQf4CQgvReTxpnP8_LQYNyHouEjQZqjw/edit) which outlines most of what you need to know to get started. There's also RoverDude's [explanation of transport routes and transport credits] which will be expanded upon in this walkthrough. This walkthrough really only restates what is written there with a few step by step examples and an end goal of manufacturing spaceships at an orbital shipyard.

## WOLF Resource Conversions

[RoverDude's resource conversion diagram](https://kerbal-forum-uploads.s3.us-west-2.amazonaws.com/monthly_2020_12/wolf.png.53d635bf5f1f4cc0e4e2f6286409d827.png).

# WOLF From Scratch: A Walkthrough

WOLF is an industry-focused extension to the industrial activities enabled in the Modular Kolonisation System. In typical mid- to late-game save files using MKS, you will have hundreds of MKS modules scattered about the place, with your planetary maps littered with various mining, refining or manufacturing facilities.  All of these facilities and the per-tick or per-second calculations they require place significant load on the KSP simulation, and loading up the models when they get in physics range can produce significant lag in the graphics engine.

The idea with WOLF is to provide the same industrial capability as MKS without the part count, without the lag, and without endless futzing around with manufacturing lines to get everything working the way you expect it to (including, for example, having to visit each industry site every few days to "catch up" with production that was supposed to happen in the meantime).

WOLF is intended as an enhancement to MKS industry — even if you haven't reached the limits of part count for your save game, WOLF can still be handy for you with resource transfers between biomes on the same planet, between surface and orbit, and between worlds.

## The Plan

For the purposes of this guide, our goal is to set up a shipyard in Minmus Orbit and provide it with resources harvested using WOLF, with the minimal possible part count. From that shipyard we'll build and launch a mission to Duna.

1. Produce material kits, specialised parts and fuel on Kerbin
1. Transfer those materials to Kerbin Orbit
1. Build a spacecraft in Kerbin Orbit from materials provided by WOLF
1. Produce material kits, specialised parts and fuel on Minmus
1. Transfer those materials to Minmus Orbit
1. Build a spacecraft in Minmus orbit from materials provided by WOLF

Note that the rules will change between these biomes, but from the end of this walkthrough you'll have the knowledge you need to establish infrastructure everywhere else in the Kerbin system.

Along the way there will be a number of pre-built vehicles for you to use so you aren't left wondering what pieces are needed to do various WOLF tasks.

## WOLF Biomes

The foundation of industry in WOLF is the "WOLF Biome" and its associated depot. The basic idea is that you dedicate a "WOLF Biome" to certain types of activity, and either transfer resources to other biome depots for further processing, or extract resources through WOLF "Hoppers" for use in the MKS industry that you're familiar with.

You can imagine WOLF Biomes as stuff that happens "behind the scenes" in the KSP world. You build up the industrial machinery to produce the goods that you need, hand that assembled factory to WOLF, then WOLF stops rendering those parts. The entire production line becomes an abstraction, with hundreds of parts abstracted away to a handful of numbers.

Where the world of MKS is concerned with resource concentrations, extractor efficiency, engineer multipliers and storage capacity, the world of WOLF is concerned with resource availability, expressed as one single number. Each WOLF biome has a certain availability for each resource. There are no concentrations to worry about, nor are there survey maps to ponder and prime locations to target for resource extraction. There's just a number for each resource in each biome.

The major catch with WOLF is that once you've committed to a certain production chain, there's no taking it back and making changes. With MKS infrastructure you can start producing Transport Credits then pivot to producing Material Kits and Specialised Parts by changing the recipes for a bunch of modules. With WOLF infrastructure, once you start producing something, that production chain will stay in place for the rest of your game.

### Start a New Sandbox Game

Let's have a look at how WOLF biomes and production chains work. Create a new sandbox game. Ensure that when you create the game, under _Difficulty Options_ > _Advanced_, you deselect _Enable Kerbal Experience_.  This will give all of your Kerbals maximum experience.  Since Kerbal experience affects resource production, the rest of this tutorial will make more sense. For the rest of this walkthrough we'll assume you called your game "WOLF Tutorial".

If you want to use the tutorial ships, get the [WOLF Tutorial Ships][MRWOLFTS] release file and unpack it now. Put put the Ships and Subassemblies folders into your save directory.

![The Kerbal Space Program saves directory showing the WOLF Tutorial save folder. Alongside that is the WOLF_Tutorial_Ships ZIP file contents. An arrow indicates that the contents of the ZIP file should be dragged directly to the WOLF Tutorial save folder]()

### Surveying Harvestable Biome Resources

As soon as you start the new sandbox game, head to the SPH and build yourself a survey rover. If you're using the tutorial ships, use the **WOLF Depot Deployer** for this section. You'll need the **Surface Scanning Module** from the stock game. Here's my **WOLF Depot Deployer** which has a **Surface Scanning Module**, the **WOLF Transport Computer** which we'll discuss later, and the **Bon Voyage Autopilot** module (automatically incorporated into the controlling part) which I highly recommend (but more about that later).

![The WOLF Depot Deployer rover with important components marked: surface scanner, transport computer and bon voyage autopilot](https://i.imgur.com/tbamdi2.png)

Launch this vessel and open the **Surface Scanning Module** context menu (right-click menu). You'll see the usual MKS resource details in the Surface Scanning Module's window. For each resource there's a concentration tagged "[Surf]" (because it's a resource on the surface) which is then combined with harvester efficiency to determine how much of that resource you'll be extracting per second. WOLF doesn't use that data.

Now open the **WOLF Dashboard** and select the *Harvestable Resources* pane. You'll see that it's empty right now.

![WOLF Dashboard showing no biomes with no harvestable resources]()

Looking back to the **Surface Scanning Module** context menu, there is one line under the MKS resources list specifying the "WOLF biome". You'll also see the "Survey WOLF Biome" action. Click it!

![Surface Scanning Module context menu showing the usual MKS resources along with the WOLF Biome name and Survey WOLF Biome action](https://surfacescanningmodule.jpg)

Recover this vessel.

## WOLF Dashboard -- Harvestable Resources and Depots

Now to use those resources. Switch scenes to the SPH and open the WOLF dashboard, then click the *Harvestable Resources* button:

![SPH scene showing WOLF Dashboard open to Harvestable Resources pane](https://i.imgur.com/kRFiRqw.jpg)

You'll have one Body/Biome option: Kerbin:KSC. There are four columns here which help you understand what resources you have access to:

1. Resource name, which represents the WOLF version of resources (as opposed to the "surface" resources)
2. Abundance, which is the WOLF equivalent to surface resource "concentration" (but it works completely differently)
3. Harvested, which is how much of the abundance you are currently extracting
4. Remaining, which is how much of the abundance is left to extract

![SPH scene showing WOLF Dashboard open to Depots pane](https://i.imgur.com/3LUj6WM.png)

The *Depots* pane lists all your active WOLF Depots. Since you have no depots yet, it's empty.

## WOLF Modules

Now that the KSC WOLF Biome is surveyed, we need to deploy a WOLF depot. Before we do that though, have a quick look at the modules that make up the WOLF system, then we'll go over the rules of deploying them.

Switch to the *Planner* pane in the **WOLF Dashboard**, and select the "WOLF" parts group in the selection pane on the left, then start planning this depot with a **WOLF Fabricator Module**:

![SPH scene showing WOLF Dashboard open on Planning pane with a WOLF Fabricator Module added as the first piece of the vessel under construction](https://i.imgur.com/PzDhvPY.jpg)

There are two groups of values here: the first is the **depot summary** showing resources processed inside your WOLF Depot, the second is the harvestable resource report which shows the same details from the *Harvestable Resources* pane, but limited to only those resources that you are actually harvesting from this WOLF Biome. Since the fabricator you just added has not been configured it will be using the *Material Kits* recipe. The *Planner* now shows that you have a deficit of power, maintenance, technician crew point, chemicals, metals and polymers.

Add a *WOLF Maintenance Module* and a *WOLF Power Module*. Now you'll see that you have surplus maintenance and power, but have incurred a deficit in various crew points. At this point, stack two *PPD-10 Hitchhiker Storage* components onto your WOLF modules and add an Engineer, Kolonist, Mechanic and Technician to your crew -- each crew member will add 10 crew points for their respective speciality. That's the crew points taken care of but now you have habitation and life support to worry about -- that's easily resolved by adding the *WOLF Habitation Module* and *WOLF Life Support Module*, leaving you with a deficit of food, oxygen and water (and the chemicals, metals and polymers for the fabricator).

Oxygen and water are avialable as *Harvestable Resources* which means we can supply the depot with those resources using **WOLF MHU-550 Bulk Harvester** modules. Add two of those, configure one to harvest water and the other to harvest oxygen.

In the harvestable resource section of the planner you'll see that the harvesters are using 5 units each of the 1000 abundance of oxygen and 750 abundance of water, leaving 995 and 745 available. Note the numbers in the "Harvested" column: "0 (-5)" means that the KSC Biome Depot is currently harvesting 0 of that resource, and the craft that we are building will be harvesting 5 (thus reducing the availability by 5).

Food is produced by an agricultural module or bioreactor module. Add a **WOLF Agriculture Module** and set it up to use the *Farm* recipe. This has now added a demand for a farmer, dirt and fertiliser. Add a farmer to your crew, then you'll need three **WOLF MHU-550 Bulk Harvester** modules to get the dirt you need. To get fertiliser, we'll add a **WOLF MHU-559 Bulk Harvester** to harvest *gypsum*, then add two **WOLF Extractor Module** set to convert the *gypsum* to *fertiliser* (technically you only need one to feed the farm, but the harvester can feed two extractors). The two extractor modules have added a deficit for *Lab* resource which is supplied by a **WOLF Science Module** so add one of those onto your growing pile of infrastructure, then add the scientist and medic crew that are needed for the science module.

Finally, add the harvesters and refineries required for the chemicals (feed stock is minerals), metals (feed stock is metallic ore) and polymers (feed stock is substrates). To finish off this infrastructure install add a power module, and you should no longer have any deficits in the *Planner*. Then the final part to add is a probe core. What a beautiful creation! Did yours turn out like mine?

![SPH scene showing WOLF infrastructure required to support creation of 2 Material Kits abundance]()

If you're familiar with the production chains from MKS you'll see that this WOLF infrastructure is a lot simpler than what is required in MKS, for example each **WOLF MHU-550 Bulk Harvester** is roughly equivalent to a mining ship with a logistics hub attached to the planetary warehouse -- each of those will be a dozen parts given the need for drills, ore tanks, radiators, power source, probe core and whatever else you normally put on your mining ships. That part count can severely bulk out your save file size, and slow your game to a crawl any time you load a production facility into physics range.

**Now save this vessel and clear the build area**. We're not going to launch this monstrosity just yet since you can't do anything with it until we set up a depot for the KSC biome.

## KSC Depot

To establish the KSC Depot, create a new vessel which is just the WOLF Depot Module and the smallest probe core. You don't need much, just the ability to control the vessel for a few seconds once it's launched. We're going to launch this Depot and immediately hand it over to the WOLF system.

**Warning: Any other parts attached to the WOLF modules will be consumed along with the WOLF modules when you hand them over to the biome depot, including any crew. In addition the WOLF Depot can not have any other WOLF components attached, not even the Survey Scanner.**

Now that you have your two-component vessel (the WOLF Depot Module and a cheap probe core), it's time to commit them to the void! I mean … establish your KSC Biome Depot:

![WOLF Depot Module with context panel showing "Establish Depot" action.](https://i.imgur.com/XiGvGVE.jpg)

Just select the "Establish Depot" action for the WOLF Depot Module, and the vessel will disappear. It belongs to WOLF now.

Return to the SPH, and let's set up Material Kits production in this new depot.

## KSC Biome: Fabrication Module for Material Kits

Check out the Depots pane of the WOLF Dashboard now:

![WOLF Dashboard showing the new KSC Biome Depot with bonus resources awarded to Kerbin-based depots](https://i.imgur.com/06X5OVl.jpg)

That depot has given us 1 Food, 1 Oxygen, 5 Material Kits, 5 Water, and 10 Power. This will significantly reduce the amount of infrastructure we need to get started — but remember that these bonus resources only apply to WOLF biomes on Kerbin.

Now load the infrastructure you built in the previous step (there is also the **WOLF Tutorial Example Material Kits** craft if you didn't save your own) and launch this mass of modules. Remember you can use the *Planner* pane of the **WOLF Dashboard** to figure out which specialists you need. Once it's all on the runway select the **connect to depot** action. With that done, open the **WOLF Dashboard** and check the *Depots* pane.

![Runway scene with WOLF Dashboard showing new production added](https://i.imgur.com/6ocmxfV.jpg)

## WOLF Transport Routes and Shipments

It's all well and good having that production chain set up, but what do we do with those WOLF Material Kit resources? The next step is getting those resources to orbit, where we want to use Material Kits to assemble DIY Kits (the DIY kits will be launched from KSC to start with).

WOLF handles transport of resources from one biome to another by way of *Routes* which are path established for *Shipments*. You establish a route by travelling between biomes using the WOLF Transport Computer. This will add *Route* between the source biome and the destination biome. You can then add resources to *Shipments* on that route. Each shipment has a certain capacity, you'll allocate a number of units of resource to a shipment, then that resource will be reduced in the source biome and increased in the target biome.

## WOLF Infrastructure Expansion

To introduce you to transport routes and shipments, let's expand the biome depots on Kerbin a little. To do that, we'll build ourselves a Frankenstein's monster of a rover. Why? Because sometimes the best way to get stuff to where you need it is to stick wheels or rockets on it.

**I highly recommend you get the Bon Voyage add-on, it makes the process of deploying biome depots much, much easier**

![This assemblage of WOLF modules and wheels will make life easier for us, trust me](https://i.imgur.com/eaLvBmB.jpg)

The ingredients are:

  + WOLF Depot Deployer Rover (based on the Karibou rover)
  + Tutorial Basic Depot subassembly
    + Karibou Flatbeds containing WOLF modules attached to rover via Clamp-O-Tron Sr
    + WOLF Depot & probe core on a decoupler

Why build a contraption with so many complications? Because simple is boring!

The game plan is to drive this Frankenstein's Monster of a rover out to a new biome, scan the biome, deploy the depot, connect the modules we're delivering, then build the transport route back to KSC biome.

Before you head out, lock the brakes and activate Action Group 10 (press '0') to start the reactor and radiator. Then start a new transport route using the **WOLF Transport Computer**:

![WOLF Depot Deployer rover with 'connect to source depot' action visible in the Transport Computer context menu]()

Drive that rover into the new biome, in this example I've taken a new depot up to the mountains. If you use Bon Voyage, be careful about setting a destination in the mountains because it will spawn your vehicle above the ground, from where it will fall and tumble to its doom — set the destination to be somewhere relatively flat and drive the rover into the Mountains biome manually. Similarly be careful about using Bon Voyage to travel back to KSC — set the destination to be southwest of KSC in the "shores" biome so you don't end up spawning the rover under the KSC terrain where it will explode the moment you try moving it.

Once you get the rover to the new biome, detach the WOLF Depot component and select the "Establish depot" action:

![The WOLF Depot rover is detached and about to establish the Kerbin Mountains biome depot](https://i.imgur.com/svUwwfQ.jpg)

Then detach the command rover and connect the WOLF modules to the depot:

![The WOLF modules rover ready to be connected to the depot](https://i.imgur.com/VR7i2Za.jpg)

Now check the **Transport Computer** and see that this route was very expensive. This is because you lost most of the weight of the vehicle between the start and end of the route. Please cancel this route, you don't want to use it.

![WOLF Deppot Deployer Rover in the mountains with the Transport Computer context menu showing the route was expensive. The cancel route button is indicated.]()

## WOLF Transport Routes

With the depot established, it's time to connect it to the KSC biome. Select the "connect to source depot" action on the WOLF Transport Computer, then move the rover back to the KSC biome.

![WOLF Depot Deployer Rover with 'connect to source depot' action visible in the Transport Computer context menu]()

Once the rover is back at KSC, select the "connect to destination depot" action on the WOLF Transport Computer You'll get a notification about your infrastructure being upgraded, and you'll be able to see the new route listed in the *Routes* pane of the WOLF Dashboard.

![The WOLF Dashboard shows the established route](https://i.imgur.com/UFyD9sy.jpg)

Now go ahead and repeat the process of deploying biome depots, populating them with equipment to produce Material Kits, and connecting those biomes to KSC with multiple routes. Each time you run a route you'll improve the logistics capacity between the source and destination biome. If you improve a biome that already has a WOLF Depot, you won't need to ship out a new depot so you can exclude that component from the rover before launching it. Remember the basic process for establishing a new biome depot is:

 + Prepare the WOLF Depot Deployer rover with the WOLF Basic Depot subsystem
   + Required crew is Engineer, Kolonist, Mechanic
 + On the runway, lock the brakes and start the reactor
 + Move the rover to the new biome
 + Survey the WOLF Biome
 + Decouple the **WOLF Depot** component
 + Use the *Establish Depot* action on the **WOLF Depot**
 + Decouple the **Tutorial Basic Depot** assembly
 + Use the *Connect to depot* action on the **Tutorial Basic Depot** assembly
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover back to the destination biome for the route (for our purposes, the KSC)
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Recover the rover

Once you have established a depot the process becomes much simpler:

 + Launch the WOLF Depot Deployer on its own
 + On the runway, lock the brakes and start the reactor
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover to the remote biome
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Use the *Connect to Origin Depot* action on the **WOLF Transport Computer**
 + Move the rover back to the KSC
 + Use the *Connect to Destination Depot* action on the **WOLF Transport Computer**
 + Repeat steps 3-8 as often as you need

Here's an example of routes between multiple biomes that I prepared earlier:

![Multiple routes created between Kerbin Shores and KSC mean that route now has a payload capacity of 12](https://i.imgur.com/hZpj49i.jpg)

Now to actually use those routes!

## WOLF Shipments

In this walkthrough the main purpose of setting up these biomes is to get Material Kits and Fuel to orbit to start building spaceships. There are no doubt untapped opportunities in your biomes (eg: the ability to send one resource from a biome with excess to another biome with a deficit), but for now we have heaps of WOLF Material Kit output to get to orbit.

By now you should have at least two biomes (eg: KSC, Mountains, Grasslands, Shores) established with infrastructure to fabricate Material Kits.

Open the WOLF dashboard to the *Routes* pane and open the *Manage Transfers* dialog:

![Manage Transfers dialog showing resources available at source and destination](https://i.imgur.com/GbwsEpS.jpg)

This dialog is use to set up resource shipments over a route. The numbers visible in this dialog show:

 + The resources and their availability at the source biome depot
 + The selected resource
 + The availability of that resource in the source biome depot
 + The current available/incoming values of the resource in the destination biome
 + The list of resources that you have already selected for shipment on this route
 + How much capacity is left for the shipment payload
 + How much payload capacity has already been used

How much of a resource you can add to shipments on this route is limited to the smaller number of the availability of the resource or the available payload. In the example above there are 20 Material Kit points available, and the payload has space for all of them with room to spare.

Click the downward pointing triangle next to *Material Kits* in the available resources list.

If you have more Material Kit availability than will fit in the payload, you can simply connect the route more times with your route-building vehicles to increase the payload size.

Set the *Transfer Amount* to 1, then click *Transfer*. You should notice:

 + The "Origin" availability will drop by 1
 + The "Destination" availability will increase by 1
 + The "Available Payload" will drop by 1/1 (eg from 7/10 to 8/11)

You'll see a new row in the bottom table displaying the transfer you've just organised. Add another transfer of 5 Material Kits, and you'll see the details in the Resource/Origin/Destination values and the row in the bottom table updated to show the new payload contents.

If you have set up other biomes, go ahead and set up their shipments to include the Material Kits they're set up to fabricate. The next stage of the walkthrough is getting those Material Kits to orbit.

The *Routes* pane of the **WOLF Dashboard** will now show the resources being transferred between the various biomes and the KSC.

![WOLF Dashboard open to the Routes pane displaying the various transfers that have been arranged over the established routes]()

# Transport Routes and Transport Credits Costs

Up till now we've kept the transport routes simple by only connecting biomes that can be reached without expending mass. It's time to kick it up a notch and learn about Transport Credits, which is an abstraction of the process of building launch vehicles, fuelling them and launching payloads to orbit (or deorbiting payloads to bring them to the surface).

The first thing we'll do here is a few test flights to understand how many *Transport Credits* we'll need for sending supplies to orbit (or roughly, how Transport Credits correlate to delta-v and ship size). Let's start with a "small" rocket, a medium sized rocket, a 3t payload SSTO spaceplane, and a 55t payload SSTO spaceplane. Note that with enough Transport Credits each flight will add a certain payload capacity to the available routes from KSC to Kerbin Orbit, with the payload capacity being proportional to the payload capacity of each launch vehicle. We'll get the gory details soon!

## Quick and Dirty Transport Credit Example Flights

Put together a rocket that can carry a single 3t **2.5m WOLF Cargo Kontainer** to orbit using 2.5m parts. The **WOLF Tutorial 2.5m SSTO* contains:

 + 2.5m WOLF Cargo Kontainer
 + RC-001S Remote Guidance Unit
 + Protective Rocket Nosecone Mk7
 + Rockomax Jumbo-64 Fuel Tank
 + RE-I5 "Skipper" Liquid Fuel Engine
 + WOLF Transport Computer

Send that to the launch pad, select the *Connect to Origin Depot* action on the **WOLF Transport Computer**, and launch the rocket to a 80km orbit. Once in orbit, check the "Route cost" reported by the **WOLF Transport Computer**.

If you try to use the **Connect to Destination Depot** action, you should get an error message about needing more Transport Credits to complete that operation. Revert to launch, and run it a few times just to see that the "Route cost" is predictable. My flights came up with a route cost of around 30.

![Sample flight of 2.5m rocket showing a route cost](https://i.imgur.com/Iq5PW4k.jpg)

Revert to launch and do the same thing with a 3.75m rocket. The *WOLF Tutorial 3.75m SSTO* is roughly:

 + 2 x 3.75m WOLF Cargo Kontainer
 + Protective Rocket Nosecone Mk7
 + RC-L01 Remote Guidance Unit
 + Advanced Reaction Wheel Module, Large
 + WOLF Transport Computer
 + Kerbodyne S3-14400 Tank
 + S3 KS-24x4 "Mammoth" Liquid Fuel Engine

Send that to the launch pad, select the "connect to origin depot" on the WOLF Transport Computer, and launch the rocket to an 80km orbit. As before, check the "route cost", revert to launch and run the process again to show that the "route cost" is predictable. My flights came up with a route cost of 86, giving a *Transport Credit Per Unit* cost of around 6.14.

Now do the same thing with spaceplanes. The two I use are the **WOLF SSTO** and [ES-96 Python by Juggernoob](https://steamcommunity.com/sharedfiles/filedetails/?id=1722161481) which I find to be an aesthetically pleasing and easy-to-fly SSTO spaceplanes. To get them to orbit just set throttle to maximum, stage once to light the engines, rotate off the runway to 10 degrees at about 140m/s and hold the nose at 10 degrees for the whole flight through the atmosphere. When the airbreathing mode is insufficient to keep accelerating, switch to closed cycle and push the apoapsis to 80km. Cruise to the top of the atmosphere, plot a circularisation burn at apoapsis, and execute that burn. My flights with **WOLF SSTO** ended up producing routes with a cost of 9 for 3t cargo, or about 3 credits/unit. The **ES-96 Python** got to orbit in the order of 90 Credits for 42t -- you'll need to pull the orange tank payload out and put in 6 x 3.5m WOLF Cargo Kontainers, two end-to-end where the orange tank started, then the other four stacked on top in pairs and then clipped into the cargo bay so they are fully contained. The ES-96 in the tutorial ships package has already been modified and will automatically start the route when you stage to launch.

## Transport Module for Transport Credits

Save your game here, give it a name like "Before Transport Credits". Skip ahead to the next section if you want to know why.

How do we produce Transport Credits? The short version is that *Transport Credits* are produced by the *WOLF Transport Module*. By now you should be familiar with the drill: start assembling a new WOLF infrastructure component with the WOLF Dashboard open to the Planning pane, beginning with the WOLF Transport Module. Fuel is produced by the Fuel(Ore) or Fuel(H2O) recipes in the WOLF Refinery Module — each recipe will take 5 points of input availability and provide 2 points of Fuel availability. As usual one harvester will provide sufficient Ore or Water for two refineries.

The "atomic" component of a Transport Credit production line is 1 Transport Module, 2 MHU-500 harvesters, 4 Refinery Modules.

![Atomic Transport Credit production facility is 1 Transport Module, 2 MHU-500 Harvesters, 4 Refinery Modules](https://i.imgur.com/NR5YYcv.jpg)

Have a go at producing 2 Frankenstein rovers each capable of producing 50 transport credits. Between them they will give you the 100 needed to establish a transport route with the Juggernoob ES-96 Python.

![A Frankestein's Monster rover that can addd 50 Transport Credit production to a biome depot](https://i.imgur.com/2zIhbHs.jpg)

FIXME: post the craft file somewhere

With 100 transport credits under our belt, time to catch a SSTO space plane to orbit!

![ES-96 Python in the SPH with WOLF Dashboard showing 105 transport credits available](https://i.imgur.com/xBi7Hod.jpg)

FIXME: get a screenshot of the ES-96 Python achieving orbit with the route cost showing.

The nice thing about SSTOs is an extremely low route cost for the deorbiting of payloads.

![ES-96 Python reentering with route cost displaying 2 credits](https://i.imgur.com/vhcsb2x.jpg)

FIXME: don't crash the plane on landing. Show the route cost for the deorbit trip Kerbin Orbit Biome -> KSC Biome.

## How To Avoid Transport Credit Costs of Propellant-Consuming Vehicles

Now that you've gone to the effort of establishing that Transport Credit infrastructure, I have a confession to make. You can make the system work to your advantage and completely eliminate the Transport Credit cost of these SSTO flights.

How? Put a propellant depot in orbit, fly your transport vehicle to that depot and refuel before connecting the **WOLF Transport Computer** to the destination depot.

Here's the **ES-96 Python** at the end of a 42t haul to orbit having just refuelled. How many transport credits to fly 42t to orbit? 0.

Go back and load your "Before Transport Credits" save game. As an apology for giving you the runaround, please accept the **WOLF Orbital Propellant Depot** that you'll find in the tutorial ships package. Note that the propellant depot has a tanker that can also fly to your stranded vehicle, so you don't have to worry about carrying spare propellant to orbit.

## WOLF Hopper for Resource Delivery

WIP: Provide a Stock + USI Constellation orbital ship yard capable of assembling DIY kits and then constructing ships from those kits. Point out the use of WOLF hoppers to deliver resources into MKS Kontainers.

So now we have a decent amount of payload to Kerbin Orbit, time to set up shipment of those WOLF Material Kit resources. Open the WOLF Dashboard, and select *Manage Transfers* from the *Routes* pane. In my example there are 82 Material Kits points at KSC, and 165 payload available to get to Kerbin Orbit.

Let's send all of those to orbit:

![WOLF Routes Dashboard showing transfer of 82 availability of Material Kits to orbit](https://i.imgur.com/7HkvfNw.jpeg)

Then we can go to the orbital shipyard and take delivery of all those units at this one facility. To do that, activate the Material Kits Hopper. That hopper will now "produce" Material Kits as an MKS resource at the rate of 2000/day (for the 2.5m hopper) or 5000/day (for the 5m hopper) while consuming 2 units of availability from the biome depot.


[MRWOFLTS]: https://github.com/MaraRinn/WOLF-Tutorial-Ships "Mara Rinn's WOLF Tutorial Ships repository"
