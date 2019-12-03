<p align="center"><img src="https://upload.wikimedia.org/wikipedia/de/3/38/GeoServer_Logo.svg" /></p>
<h4 align="center">Task: Build Windows installer [Windows users only]</h4>
<p align="center">The following README covers the process by which I created my own installer for GeoServer 2.17.</p>

# Process

1. Firstly, I downloaded and installed [NSIS](http://nsis.sourceforge.net/).

2. Next, I downloaded and extracted the [NSIS Access Control Plugin](http://nsis.sourceforge.net/AccessControl_plug-in). I copied the `AccessControl.dll` which was present in the `Plugins` directory, and the `AccessControl.dll` which was present in the `Unicode/Plugins` directory to their respective folders in `C:\Program Files (x86)\NSIS\Plugins`. These folders were called `x86-ansi` and `x86-unicode`.
<p align="center"><img src="https://i.imgur.com/5mYLqa9.png"></p>

3. After this, I downloaded the [nightly development build](https://build.geoserver.org/geoserver/master/geoserver-master-latest-bin.zip) and unzipped the contents.

4. Once I had unzipped the GeoServer platform independent binaries, I cloned the GeoServer repository and copied all of the files in the `src/release/installer/win` directory to my previously downloaded binary directory.

<p align="center"><img src="https://i.imgur.com/A3H6rNz.png"></p>
<p align="center"><img src="https://i.imgur.com/WPCobwW.png"></p>

5. Once the files had copied over, I right-clicked on the installer script titled `GeoServerEXE.nsi` and selected `Compile Script` to build the installer.

<p align="center"><img src="https://i.imgur.com/iS6XFaj.png"></p>

# Finished image
<p align="center"><img src="https://i.imgur.com/EBXTC3z.png"></p>
