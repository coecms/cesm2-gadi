Gadi Configuration for CESM2
============================

Download this repository to ~/.cime on Gadi:

    git clone https://github.com/coecms/cesm2-gadi ~/.cime

Edit the paths in `config_machines.xml` if desired

Follow the CESM2 instructions to download the source code

Copy the `FindNetCDF.cmake` script to the CESM2 source directory `cime/src/CMake`

Follow the CESM2 instructions to configure a case and build and run it

You may need to install the perl XML::LibXML library with

    cpan XML::LibXML
