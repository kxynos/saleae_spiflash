# SPI flash protocol analyzer for Saleae

Protocol analyzer for SPI flash decodes single, dual and quad commands.
Several manufacturer specific command sets can be used.
Most flashes can work in SPI mode 0 and 3, analyzer detects mode automatically or it can be set manually.

# Features
- SPI0 and SPI3 mode
- Single, dual and quad mode
- Commands for changing between single and quad or dual mode detected
- Continues read mode detected
- Register bit fields decoded
- Following manufacturers command sets supported:
  - Winbond
  - Macronix
  - GigaDevice
  - Adesto
  - Microchip
  - Micron
  - Cypress
  - Issi

# Installation (tested on MacOS 10.14)

```bash
git clone <saleae_spiflash_project>
cd <saleae_spiflash_project>
python3 build_analyzer.py
```

Launch Saleae Logic 1.x and under *Options -> Preferences -> Developer* you will find the *Search this path for analyzer plugins*. Either copy the path or via Browse find the newly create release path. On the other hand, you could create a folder in Documents with the release files and Browse to it instead. 

**Restart** the application to get the new plug-ins installed. 

# Installation (old)

For Windows there are two msi files in prebuilt folder, that will add analyzer to the existing Saleae Logic installation folder.

Manual installation
Simply put SpiFlashAnalyzer.dll in the Saleae *Analyzers* folder (typically: C:\Program Files\Saleae LLC\Analyzers).

For Linux and Mac OSX library needs to be build with Saleae provided build_analyzer.py script. The library then can be copied to *Analyzer* folder in the Logic installation folder.
