First line is for mod version, second line for Minecraft version.

The first line should be filled in like this (where build will be automatically filled in by the jenkins system):

All master builds: SNAPSHOT-build (this is to allow the amount of beta build users to show up on MCStats)

Release builds: major.minor.rc#/bugfix (Do not fill in build numbers for Jenkins. Always increment the rc# or bugfix)

.rc# denote testing release candidate builds whereas .bugfix is for released versions (having both should be okay)

Example:

Release candidates: 1.3rc1, 1.3rc2, 1.3rc3, etc

Proper releases: 1.3, 1.3.1, 1.3.2, etc

The API revision number is in the API zip filename - if it doesn't change, you do not have to update your mods.