<img src="https://upload.wikimedia.org/wikipedia/de/3/38/GeoServer_Logo.svg" align="center" />
<h4 align="center">Task: Build Windows installer [Windows users only]</h4>
<p align="center">The following README covers the process by which I created my own installer (using a Windows machine) for GeoServer 2.17.</p>

# Process

1. Firstly, I downloaded and installed [NSIS](http://nsis.sourceforge.net/).
2. Next, I downloaded and extracted the [NSIS Access Control Plugin](http://nsis.sourceforge.net/AccessControl_plug-in). I copied the `AccessControl.dll` which was present in the `Plugins` directory, and the `AccessControl.dll` which was present in the `Unicode/Plugins` directory to their respective folders in `C:\Program Files (x86)\NSIS\Plugins`. These folders were called `x86-ansi` and `x86-unicode`.
3. After this, I downloaded the [nightly development build](https://build.geoserver.org/geoserver/master/geoserver-master-latest-bin.zip) and unzipped the contents.
4. Once I had unzipped the GeoServer platform independent binaries, I cloned the GeoServer repository and copied all of the files in the `src/release/installer/win` directory to my previously downloaded binary directory.
5. Once the files had copied over, I right-clicked on the installer script titled `GeoServerEXE.nsi` and selected `Compile Script` to build the installer.
