This is an official git repository for the jVectorMap plug-in for jQuery. Its main purpose is to show interactive vector maps on the web pages.

You can find maps, documentation, examples and more at [the official site](http://jvectormap.com/)

Dependencies
-------------

One way, which I believe to be the best way, to get this running on a Mac is the following:

1. brew update (install homebrew if you don't have this already) 
2. brew install python 
3. pip install Shapely
4. pip install anyjson

* Note: Make sure are using the right Python.  Running 'brew doctor' will help you out. 

Converter
--------------
It also includes a converter that could be used to create your own maps for jVectorMap from the data in various GIS formats like Shapefile. The following command could be used to convert USA map from the data available at [www.naturalearthdata.com](http://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-1-states-provinces/):

      python \
      /Users/adampreston/Repository/jvectormap/converter/converter.py \
      /Users/adampreston/Downloads/ne_50m_admin_0_map_subunits/ne_50m_admin_0_map_subunits.shp \
      /Users/adampreston/Repository/jvectormap/converter/resulting-map.js \
      --width 900 \
      --simplify_tolerance 20000 \
      --longitude0 0 \
      --projection mill \
      --country_name_index 8 \
      --country_code_index 43