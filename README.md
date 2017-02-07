
Pixl8
=====
This repository contains an Eclipse Projects ""Pixl8-common"

You can simply import it into eclipse by choosing File/Import/General/Existing Projects into Workspace and then choose the local repositories root directory

Pixl8-common
Containing some extensions to Railo specific written for Pixl8


Build Lucee Extension
---------------------
On the command line go into the project "Pixl8-common", then simply call "ant" and the build script will build a classic (at /dist/classic) and a modern (at dist/modern) extension. If you wanna build only a classic extension, simply call "ant classic", to get only a modern extension call "ant modern".

Provide Modern Extension (for Lucee>=5.0)
-----------------------------------------
Simply copy the file you find at "dist/modern" (with extension .lex) to "lucee-server/context/deploy" in your Lucee installation, Lucee then will automaticly install the extension.
Please have in mind that this Extension need at least the Lucee version 5.0.0.46
