# ETF2LDivs

This SourceMod plugin shows players ETF2L team and division in the server chat when they are joining the server. It is based on [thraaawn's tETF2LDivision plugin](https://github.com/thraaawn/tETF2LDivision). At this point I wanted to thank [JoinedSenses](https://github.com/JoinedSenses) for converting whole tETF2LDivision plugin to a new SourceMod syntax and whole help provided to me while making this plugin.

## Changes to original repo

- added a rudimentary caching system
- fixed (a bug?) where steamids were formatted differently

## Dependencies

- [System2](https://github.com/dordnung/System2)
- [SourceMod 1.10](https://www.sourcemod.net/downloads.php?branch=stable)

## Building

- download SM 1.10 and System2 extension, place System2 files in their respective folders
- in `addons/sourcemod/scripting` execute `spcomp ETF2LDivs.sp` or `spcomp64 ETF2LDivs.sp` if you are using a 64-bit OS

## Variables

- `sm_etf2ldivs_enable` (`0`/`1`) (def. 1) - disables/enables plugin
- `sm_etf2ldivs_teamtype` (`Highlander`, `6on6`, `2on2`, `1on1`) (def. 6on6) - defines team type shown in all announcements
- `sm_etf2ldivs_announce` (`0`/`1`) (def. 1) - disables/enables announcing players with their ETF2L data on join
- `sm_etf2ldivs_seasonsonly` (`0`/`1`) (def. 0) - disables/enables placements in fun cups
- `sm_etf2ldivs_announce_adminsonly` (`0`/`1`) (def. 0) - disables/enables announcements only for server administrators

## Commands

- `!div` / `sm_div` - shows up divisions for all players on the server
- `!divdetails <player nickname>` / `sm_divdetail <player nickname>` - opens a ETF2L profile in a MOTD window if it is possible to find the player on the server, otherwise ETF2L search window opens up
- `div?` in any chat message will print sender's team/division info
