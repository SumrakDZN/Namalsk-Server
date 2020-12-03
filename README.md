# Namalsk Server Files
Welcome to the Namalsk Server Files repo.
This repo contains all the necessary information and files for any Namalsk server hoster.

# WARNING
**You cannot monetize any server that is running Namalsk Island / Namalsk Survival mods! This includes even things such as selling priority queue slots.**

# Server Installation

**Basics**

* Make sure you have up-to-date *@Namalsk Island* and *@Namalsk Survival* folders in your server root.
* Copy *sumrak.bikey* from *Keys* folder to your server root *keys* folder.
* Get the mission of choice alongside default server config from *Extras* folder in Survival mod.

**Advanced setup**

If you are running a dedicated machine with multiple DayZ servers, it is recommended to subscribe to Namalsk Island and Namalsk Survival server packages. These contain optimized pbo files for your server (to reduce loading times and memory load) and are present on unlisted Steam Workshop items available [here](https://steamcommunity.com/sharedfiles/filedetails/?id=2288339650) and [here](https://steamcommunity.com/sharedfiles/filedetails/?id=2288336145). Both public and unlisted (server) Namalsk Workshop entries will always be updated at the same time. In order to mask these files as the ones clients are running, you need to use meta.cpp files from the client mods (ids are *2289456201* for island and *2289461232* for survival pack).

# Frequently Asked Questions (FAQ)
**Q: Can I use Namalsk Island without Namalsk Survival and vice versa?**

A: Yes.

**Q: Can I monetize my server when using Namalsk Terrain and/or Namalsk Survival mods?**

A: No. You may accept donations from people, but you are obliged to give nothing in return.

**Q: Can I repack Namalsk Island and/or Namalsk Survival mods?**

A: No, use Steam Workshop collections!

**Q: Is Namalsk compatible with X?**

A: I do not have any comprehensive list of what works with it and what not. What I can say is that I tried to make both Namalsk Terrain and Namalsk Survival as light as possible to make sure it is compatible with plenty of mods out there.

**Q: Can my mod somehow detect Namalsk?**

A: Yes, quite possibly - using script *#ifdef NAMALSK_SURVIVAL* and/or *NAMALSK_TERRAIN*.

**Q: What is the suggested player count for Namalsk?**

A: From my experience, I would recommend setting the maximum of 30-40 players.

**Q: Where can I find a default server config for Namalsk?**

A: Look into the *Server Config* folder in this repository. There are two available (for each difficulty) and each config is split into two sections (standard server params and custom Namalsk edits). If you are using your own custom server config, I very much do recommend to look into the default Namalsk one to check the params for your Namalsk server.

**Q: Is there a dark and bright night lighting setup for Namalsk?**

A: Yes, use value *222* for dark and *223* for bright in your server config (*lightingConfig* parameter).

**Q: Where can I find a default mission for Namalsk?**

A: Look into the *Mission Files* folder in this repository. Namalsk has two missions available - *Regular* and *Hardcore*.

**Q: What is the difference between the Regular and Hardcore missions?**

A: They differ in the CE setup itself. The regular setup has a very basic vehicle setup, all base building options, fast lifetime values, higher food and weapon/ammo availbility and November temperature values. The hardcore setup has no vehicles, no base building options (except stashes and small tents), higher lifetime values, lower weapon/ammo availability and December temperature values.

**Q: I want to host only Namalsk Island. Which mission should I use?**

A: Use *Regular* or *Hardcore* mission and remove the include of *types_dzn.xml* from *cfgeconomycore.xml*. Doing this will stop spawning custom items from the *Survival* package.

**Q: Where can I find a default CE Tool project files for Namalsk?**

A: Look into the *Central Economy Tool* folder in this repository. Namalsk is using area territories for most animals (rather than territories per species). As for areaflags.map, that is used only for the tier definition.

**Q: Can I use my standard types.xml from Chernarus/Livonia on Namalsk?**

A: Not entirely, Namalsk uses CE params in a different way than the vanilla terrains. There are no usage flags, only categories, tags (which act as usage flags per containers) and value flags (tiers) on map groups (buildings). Look into existing (vanilla) Namalsk types (types.xml), to get an idea how to configure your own.

**Q: Can I add new types to the existing vanilla Namalsk setup?**

A: Of course you can, but there is much to keep in mind since the map size and the amount of available places is far lower than Chernarus. Overall, if you plan to add more loot to the map, consider also adding additional buildings to the map to compensate.

**Q: I would like to adjust date to have warmer/colder environment and/or longer/shorter days.**

A: The answer is within the *init.c* file of your mission. Keep in mind that you are going to need to figure out different values for *serverTimeAcceleration* and *serverNightTimeAcceleration* within your server config to achieve a desired day:night ratio. Namalsk is positioned far north and the winter nights are really long!
Default temperature (min/max per month) for Namalsk is defined as:

> MAX{-12,  -8,  -3,   0,   2,   5,   7,  11,   8,   5,   2,  -8}

> MIN{-32, -27, -21, -14,  -7,  -4,  -2,   2,  -3,  -7, -15, -25}

Note: This only applies for servers running with Namalsk Survival! Namalsk terrain runs on default ChernarusPlus temperature values.

**Q: I need help with something I could not find in this FAQ section.**

A: Join us at our Official Namalsk [Discord](https://discord.com/invite/gK7HRDN) and request *Server Hoster* role in *#create-ticket* channel.
