# Plot_RGB_MODISA
Extract RGB bands from [MODIS-Aqua Level-2 images](https://oceancolor.gsfc.nasa.gov/cgi/browse.pl?sen=amod) to a netCDF file and plot it using GMT.

## What does the scripts do?
### [create_RGB_netcdf.R](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/create_RGB_netcdf.R)
It takes [MODIS-Aqua Level-2 image](https://oceancolor.gsfc.nasa.gov/cgi/browse.pl?sen=amod) containing surface reflectance values and converts them to log-normalised values to be used to create RGB images using [plot_GMT_rgb.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/plot_GMT_rgb.bash).


### [input_GMT.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/input_GMT.bash)
[input_GMT.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/input_GMT.bash) takes the input parameters required to plot the RGB image such as
* Extent 
* Projection
* Font
* Masks, etc.

### [plot_GMT_rgb.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/plot_GMT_rgb.bash)
It is the final script which generates RGB image in PNG format using [GMT v6.0](https://www.generic-mapping-tools.org/)


## How to run the script?
* Step 1: Run [create_RGB_netcdf.R](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/create_RGB_netcdf.R) in [R](https://www.r-project.org/) to create \*rgb.nc containing rge red, blue and green bands.
* Step 2: Input all the initialisation parameters in [input_GMT.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/input_GMT.bash)
* Step 3: In [Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) shell, run [plot_GMT_rgb.bash](https://github.com/rakeshkstp/Plot_RGB_MODISA/blob/main/plot_GMT_rgb.bash) to generate \*TC.png.

## Author
**Rakesh Kumar Singh**
