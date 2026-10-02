### Changed

- The setup file installs a missing prerequisite itself: it downloads Microsoft's installer for the Windows App Runtime, the WebView2 Runtime or the .NET 10 runtime, runs it, and checks again. Before, it named the winget command and stopped. The .NET runtime installs for the whole PC, so Windows asks for administrator rights for it; a silent setup without them still stops and names the winget command. The winget package is now this setup file instead of the zip.
