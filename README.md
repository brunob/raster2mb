![gdal2mb logo](http://mapbox.com/sites/mapbox.com/files/imagecache/scale_150x/tools_gdal2mb.png)

### Installation

* GDAL
 * OSX: [GDAL Complete](http://www.kyngchaos.com/software/frameworks) from kyngchaos
 * Other systems: [GDAL binaries](http://trac.osgeo.org/gdal/wiki/DownloadingGdalBinaries)
* [Python](http://www.python.org/) (included on OSX and Linux)

Clone the repository

    git clone git://github.com/mapbox/raster2mb.git

Add raster2mb to your PATH and make it executable.

### Usage

    raster2mb raster_merc.tiff raster_merc.mbtiles

_If GeoTIFFs are in projections other than `EPSG:900913` (as many are), run gdalwarp first:_

    gdalwarp -t_srs EPSG:900913 raster.tiff raster_merc.tiff

Run `raster2mb -h` for usage instructions.

### Description

This is a variation of the [gdal2tiles](http://www.klokan.cz/projects/gdal2tiles/) script that supports MapBox `mbtiles` SQLite tilesets as an output option. It has the same requirements as the original script - notably an installation of [GDAL](http://www.gdal.org/).

Usage of this command is

The resultant `.mbtiles` file can be used in Maps on a Stick and elsewhere.
