Revision: 25
Author: aznyi
Date: Sunday, April 3, 2022 12:25:44 PM
Message:
[core]:
* Crashfix with FindTarget in AIInterface
* Crashfix with UpdateCombat in AIInterface presenting a null spell
----
Revision: 24
Author: aznyi
Date: Sunday, April 3, 2022 11:37:32 AM
Message:
[core]:
* Load TransportAnimation.dbc so that in the future we can use it to load the time, pathing, and other metrics needed instead of using the database
----
Revision: 23
Author: aznyi
Date: Sunday, April 3, 2022 2:05:46 AM
Message:
[core]:
* Implement SoundEntries.dbc for future use
* Correct GameObject loading
* Added script activation for GAMEOBJECT_TYPE_TEXT

[scripts]:
* Shrine of Dath'Remar now works as intended
----
Revision: 22
Author: aznyi
Date: Saturday, April 2, 2022 10:49:56 PM
Message:
[core]:
* Moved items_extended cost to the vendors table as a column, we no longer need a separate table
----
Revision: 21
Author: aznyi
Date: Saturday, April 2, 2022 10:48:47 PM
Message:
[core]:
* Add GAMEOBJECT_TYPE_TEXT
----
Revision: 20
Author: aznyi
Date: Saturday, April 2, 2022 10:48:02 PM
Message:
[core]:
* Crash fix in MapMgr
----
Revision: 19
Author: aznyi
Date: Saturday, April 2, 2022 10:47:31 PM
Message:
[core]:
* Crashfix in AIInterface
----
Revision: 18
Author: aznyi
Date: Saturday, April 2, 2022 10:46:50 PM
Message:
[core]:
* Updated UpdatedFields to 2.4.3
* Compile fix due to double _ in Player.cpp
----
Revision: 17
Author: aznyi
Date: Sunday, March 27, 2022 9:07:49 PM
Message:
[core]:
* Fixed CMSG_CANCEL_TRADE issues in console with mishandled packets.
----
Revision: 16
Author: aznyi
Date: Thursday, March 24, 2022 10:15:16 PM
Message:
[core]:
* Our opcodes now match MaNGoS for 2.4.3.8606
----
Revision: 15
Author: aznyi
Date: Thursday, March 24, 2022 7:11:30 PM
Message:
[core]:
* Implemented CMSG_MEETING_STONE_INFO
----
Revision: 14
Author: aznyi
Date: Thursday, March 24, 2022 6:36:53 PM
Message:
[database]:
- Removed all old world, char, and logon updates and structures
+ Added fully updated logon_character_structures.sql
----
Revision: 13
Author: aznyi
Date: Thursday, March 24, 2022 6:35:27 PM
Message:
[database]:
- Removed changeset_notes.txt
- Added Database Import tool and required dependencies
* removed MoonScripts from the changeset_1.txt and added a fix for gameobjects that aren't supposed to be spawned
* Rebased the entire database to EndDB which is based on NCDB as WhyDB was shit and after digging in we noticed tons of issues
----
Revision: 12
Author: aznyi
Date: Thursday, March 24, 2022 6:30:47 PM
Message:
[core]:
* Added .bank command which shows your bank, applied for any user

[scripts]:
* Removed the version check for script loads, we don't care what version we are running 
----
Revision: 11
Author: aznyi
Date: Wednesday, March 23, 2022 1:23:23 AM
Message:
[core]:
- Remove realmserver
- Remove voicechat
----
Revision: 10
Author: aznyi
Date: Wednesday, March 23, 2022 12:43:58 AM
Message:
[core]:
* Crash fixes

[misc]:
+ Add DBC files zip
- Remove outdated sql query files
----
Revision: 9
Author: aznyi
Date: Monday, March 21, 2022 12:59:48 AM
Message:
[core]:
* We are now able to login using the WoW TBC 2.4.3 client
* Fixed Spell.DBC overload
* FH is now StanceBarOrder & dummy is now spellIconID in SpellEntry
+ Added VC Includes that are required to compile
+ Added svn_revision.h temporarily so we can compile and work accordingly, revisions don't matter except for versioning and tracking
----
Revision: 8
Author: aznyi
Date: Sunday, March 20, 2022 10:34:09 PM
Message:
[misc]:
* Moved configs to /configs
----
Revision: 7
Author: aznyi
Date: Sunday, March 20, 2022 10:32:43 PM
Message:
[scripts]:

* Scripts now build with the core, no need for individual hunting to the sln
* Moved Lua scripts to extras for referencing encase something is completed there we can move it to C++
* Moved the SQL file from Moon++ to changeset_1.txt
- Deleted the base Ascent Emulator scripts/Development
* Moved the Moon++ scripts to the scripts folder as a permanent home
- Deleted the server status plugin we don't need it anymore
- Deleted extras scripts as we don't need them either we are a Blizzlike project
----
Revision: 6
Author: aznyi
Date: Sunday, March 20, 2022 10:21:03 PM
Message:
[scripts]:
- Remove LUA Engine - we will be performing all code in the database and in C++
- Cleanup of the Scripts folder
* Upgraded the scripts VS Project files to VS Community 2022, tested compiling
----
Revision: 5
Author: aznyi
Date: Sunday, March 20, 2022 9:52:49 PM
Message:
[core]:

We now compile!

* hash_map -> unordered_map
* unsigned long -> ULONG_PTR
* Corrected a compile warning for sprintf by converting to std::ostringstream to use a C++ equivalent
* Corrected size_t to ulong warnings
* Corrected warning D9035
* Corrected issues with TargetMapping after converting to unordered_map
* A laundry list of other compile corrections and warning corrections.. more to come on the warnings.. the core should be brought to the latest C++ standard / Microsoft standards

[database]:
+ Added changeset_1.txt and changeset_notes.txt for future use as we make database changes

[misc]:
- Cleaned up the SVN a little bit
----
Revision: 4
Author: aznyi
Date: Saturday, March 19, 2022 11:16:04 PM
Message:
[core]:
- Removed the Zip file for the ascent windows libraries
+ Extracted the libraries and organized them in to the dep folder on the root folder structure
* Updated the VS Project files to the 2022 
----
Revision: 3
Author: aznyi
Date: Saturday, March 19, 2022 11:03:54 PM
Message:
[core]:
* Upgraded Visual  Studio project files to version 2022.
----
Revision: 2
Author: aznyi
Date: Saturday, March 19, 2022 10:59:33 PM
Message:
- Minor cleanup removing old Visual Studio projects.
----
Revision: 1
Author: aznyi
Date: Saturday, March 19, 2022 10:56:31 PM
Message:
+ Adding source files for Database, Core, and Scripts.
----
