
Pixl8
=====
This repository contains an Eclipse Projects ""Pixl8-common"

You can simply import it into eclipse by choosing File/Import/General/Existing Projects into Workspace and then choose the local repositories root directory

Pixl8-common
Containing some extensions to Railo specific written for Pixl8


Build Lucee Extension
---------------------
On the command line go into the project "Pixl8-common", then simply call "ant" and the build script will build a classic (at /dist/classic) and a modern (at dist/modern) extension. If you wanna build only a classic extension, simply call "ant classic", to get only a modern extension call "ant modern".

Provide Classic Extension (for Lucee 4.5)
In the folder "/misc/classic-ExtensionProvider" you can find an extension provider implementation you can use to provide your extensions. Simply copy that file to your webroot (including the "ext" folder), then copy your extension you find at dist/classic to that "ext" folder with a sub folder, so you should end with the following structure.
<web-root>/ext/commom/doc.json
<web-root>/ext/commom/logo.png
<web-root>/ext/commom/extension.zip

How you name the folder inside "ext" does not matter.
After that go to your server admin to "Extension/Providers" and register the extension provider as follows http://<your-host>/ExtensionProvider.cfc After that the extension should be ready to install at "Extension/Applications"

Provide Modern Extension (for Lucee>=5.0)
Simply copy the file you find at "dist/modern" (with extension .lex) to "lucee-server/context/deploy" in your Lucee installation, Lucee then will automaticly install the extension.
Please have in mind that this Extension need at least the Lucee version 5.0.0.46
