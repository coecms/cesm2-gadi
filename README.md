Gadi Configuration for CESM2
============================

Download this repository to ~/.cime on Gadi:

    git clone https://github.com/coecms/cesm2-gadi ~/.cime

Edit the paths in `config_machines.xml` if desired

Follow the CESM2 instructions to download the source code

## Building the Model

Copy the `FindNetCDF.cmake` script to the CESM2 source directory `cime/src/CMake`

Follow the CESM2 instructions to configure a case and build it

You may need to install the perl XML::LibXML library with

    cpan XML::LibXML

## Downloading Inputs

To download the input data, edit the file in your CESM source directory
`cime/config/cesm/config_inputdata.xml`, and add a `/` to the end of
`ftp://ftp.cgd.ucar.edu/cesm/inputdata`, so the 'wget' section reads

```xml
<server>
  <protocol>wget</protocol>
  <address>ftp://ftp.cgd.ucar.edu/cesm/inputdata/</address>
  <user>anonymous</user>
  <password>user@example.edu</password>
  <checksum>../inputdata_checksum.dat</checksum>
</server>
```

## Running the Model

Before attempting a large experiment make sure the model decomposition is
efficient, see
https://esmci.github.io/cime/versions/master/html/users_guide/porting-cime.html#performance-tuning-of-a-cesm-port
