# mod_cold_boot
I asked ChatGPT if it could compose MOD files. To my surprise, it said yes.

## build notes
To get the ST-01 archive on Debian-based Linux, issue these commands:

       sudo apt update
       sudo apt install lhasa wget
       install -d mod_cold_boot/stxx
       cd mod_cold_boot/stxx
       wget -O st-01.lha https://aminet.net/mods/inst/st-01.lha
       lha x st-01.lha

These files are in IFF format and AmigaOS doesn't use file extensions, so to make MilkyTracker see them you have to rename the ones you want with '.iff' extensions.

       mv Stabs Stabs.iff
