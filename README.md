# Namalsk Server Files
Welcome to the Namalsk Server Files repo.
This repo contains all the necessary information and files for any Namalsk server hoster.

# WARNING
**You cannot monetize server that is running Namalsk Island / Namalsk Survival mods! This includes even things such as selling priority queue slots.**

# Server Installation
**Basic setup**

1. Download DayZ and DayZ Server in your Steam.
2. Subscribe to [Namalsk Island](https://media.tenor.com/images/78ed59c71a9472e868490638d61d23e6/tenor.gif) and [Namalsk Survival](https://media.tenor.com/images/78ed59c71a9472e868490638d61d23e6/tenor.gif) packages.
3. Run DayZ Launcher from Steam and let it install Namalsk Island and Namalsk Survival.
4. Go to DayZ Server install folder.
5. Download key file from this repository (in folder called *Keys*) and place it into the keys folder.
5. Download server config from this repository (in folder called *Server Config*) and place it in the root.
6. Download a mission of choice (Regular/Hardcore) from this repository (in folder called *Mission Files*) and place it within the mpmissions folder.
7. Run the server with following: *DayZServer_x64.exe -config=serverNamalskCE.cfg -port=2302 "-mod=<path to your DayZ client installation>\!Workshop\@Namalsk Island;<path to your DayZ client installation>\!Workshop\@Namalsk Survival"*
8. Visit **Frequently Asked Section** for details regarding the server configuration.

**Advanced setup**

If you are running a dedicated machine with multiple DayZ servers, it is recommended to subscribe to Namalsk Island and Namalsk Survival server packages. These contain optimized pbo files for your server (to reduce loading times and memory load) and are present on unlisted Steam Workshop items available [here](https://media.tenor.com/images/78ed59c71a9472e868490638d61d23e6/tenor.gif) and [here](https://media.tenor.com/images/78ed59c71a9472e868490638d61d23e6/tenor.gif). Both public and unlisted (server) Namalsk Workshop entries will always be updated at the same time. If you want to use these, make sure you copy and paste standard (client) Island and Survival mods to your server folder, adjust -mod= launch parameter accordingly and overwrite PBO files with the ones from the server packages.

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

A: From my experience, I would recommend setting the maximum to 30-40 players.

**Q: Where can I find a default server config for Namalsk?**

A: Look into the *Server Config* folder in this repository. The config is split into two sections (standard server params and custom Namalsk edits). If you are using your own custom server config, I very much do recommend to look into the default Namalsk one to check the params for your Namalsk server.

**Q: Is there a dark and bright night lighting setup for Namalsk?**

A: Yes, use value *222* for dark and *223* for bright in your server config (*lightingConfig* parameter).

**Q: Where can I find a default mission for Namalsk?**

A: Look into the *Mission Files* folder in this repository. Namalsk has two missions available - Regular and Hardcore. Difference between these two are in the loot availability and the presence of vehicles.

**Q: Can I use my own custom init.c?**

A: Not recommended, build your own *init.c* from the ones that are included in this repository.

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

