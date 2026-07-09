# mod_cold_boot
I asked ChatGPT if it could compose `.mod` files. To my surprise, it said yes.

To be clear, by `.mod` file I mean an old-school 90s musical composition format. They were mainly used by Amiga games. A `.mod` file had to be incredibly small and sparse --- several of them had to fit comfortably alongside a full game in just 880 *kilobytes* of disk space. Producing catchy tunes under these conditions required all the skills of the compositional geniuses of the day.

Just for fun, take a look at any modern AAA title's assets folder. The musical assets individually consume megabytes of disk space, and there are dozens of them.

Not complaining, just saying.

## build notes
To get the ST-01 archive on Debian-based Linux, issue these commands:
   
    ❯ sudo apt update
    ❯ sudo apt install lhasa wget
    ❯ install -d mod_cold_boot/stxx
    ❯ cd mod_cold_boot/stxx
    ❯ wget -O st-01.lha https://aminet.net/mods/inst/st-01.lha
    ❯ lha x st-01.lha

These files are in IFF format and AmigaOS doesn't use file extensions, so to make MilkyTracker see them you have to rename the ones you want with '.iff' extensions. Like this:
   
    ❯ mv Stabs Stabs.iff
