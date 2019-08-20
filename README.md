# eccodes-build-windows
Automated ECMWF EcCodes library and tools builds for Windows

This repository is almost empty and consists mostly of an appveyor build file.

The original source code resides there : [https://github.com/ecmwf/eccodes](https://github.com/ecmwf/eccodes) (Apache 2 License)

The stuff resides inside the [releases page](https://github.com/moonpyk/eccodes-build-windows/releases) where compiled binaries are available.

The build system compiles EcCodes with the following features enabled :

  * JPEG Support (via openjpeg)
  * PNG (via libpng)

Those features should make tools/lib able to read all grib packings supported by EcCodes (tested with NOAA GFS, Méteo-France AROME/ARPEGE, DWD ICON, ECMWF WMO Essentials forecasts).

## Requirements

 * [Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017 and 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe) as MSVC 2017 C Compiler toolchain and SDKs are used.

## Installation

Grab the binaries zip (EcCodes-win-x64.zip) from the releases pages, unzip it to `C:\`, add `C:\ECMWF\bin` to your PATH and you are good to go.
If you decide to unzip it anywhere else you will have to create 2 additional environment variables :

  * `ECCODES_DEFINITION_PATH`, pointing to `<UNZIPPED_PATH>\ECMWF\share\eccodes\definitions`
  * `ECCODES_SAMPLES_PATH`, pointing to `<UNZIPPED_PATH>\ECMWF\share\eccodes\samples`

So that the library and command line tools can find needed assets to operate.

## Possible evolutions

  * 32bit build
  * Chocolatey Package

## Disclaimer

> THOSE ARE UNOFFICIAL BUILDS, NOT ENDORSED BY THE ECMWF ORGANIZATION, PROVIDED WITHOUT ANY SUPPORT.

> THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
