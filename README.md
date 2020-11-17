# Namalsk Server Files
Welcome to the Namalsk Server Files repo.
This repo contains all the necessary information and files for any Namalsk server hoster.

# WARNING
You cannot monetize server that is running Namalsk Island / Namalsk Survival mods! This includes even things such as selling priority queue slots.

# Server Installation
**Basic setup**

1. Download DayZ and DayZ Server in your Steam.
2. Subscribe to Namalsk Island (LINK) and Namalsk Survival (LINK) packages.
3. Run DayZ Launcher from Steam and let it install Namalsk Island and Namalsk Survival.
4. Go to DayZ Server install folder.
5. Download the key file (LINK) from this repository and place it into the keys folder.
5. Download server config (LINK) from this repository and place it in the root.
6. Download a mission of choice (Regular/Hardcore) from this repository and place it within the mpmissions folder.
7. Run the server with following: *DayZServer_x64.exe -config=serverNamalskCE.cfg -port=2302 "-mod=<path to your DayZ client installation>\!Workshop\@Namalsk Island;<path to your DayZ client installation>\!Workshop\@Namalsk Survival"*
8. Visit **Frequently Asked Section** for details regarding the server configuration.

**Advanced setup**

If you are running a dedicated machine with multiple DayZ servers, it is recommended to subscribe to Namalsk Island and Namalsk Survival server packages. These contain optimized pbo files for your server (to reduce loading times and memory load). These packages are available on unlisted Steam Workshop items available here (LINK) and here (LINK). In this case, make sure you copy and paste standard (client) Island and Survival mods to your server folder, adjust -mod= launch parameter and overwrite PBO files with the ones from the server packages. Both public and unlisted (server) Namalsk Workshop entries will always be updated at the same time.

# Frequently Asked Questions (FAQ)
> Can I use Namalsk Island without Namalsk Survival and vice versa?

Yes.

> Can I monetize my server when using Namalsk Terrain and/or Namalsk Survival mods?

No. You may accept donations from people, but you are obliged to give nothing in return.

> Can I repack Namalsk Island and/or Namalsk Survival mods?

No, use Steam Workshop collections!

> Is Namalsk compatible with X?

I do not have any comprehensive list of what works with it and what not. What I can say is that I tried to make both Namalsk Terrain and Namalsk Survival as light as possible to make sure it is compatible with plenty of mods out there.

> Can my mod somehow detect Namalsk?**

Yes, quite possibly - using script *#ifdef NAMALSK_SURVIVAL* and/or *NAMALSK_TERRAIN*.

> What is the suggested player count for Namalsk?

From my experience, I would recommend setting the maximum to 30-40 players.
