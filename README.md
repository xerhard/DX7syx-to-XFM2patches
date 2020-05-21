# DX7syx-to-XFM2patches
Quick and dirty convertion of DX7 syx files containing 32 presets into XFM2 json patch files.

Code is built on javac 11.0.7


## File/Directory structure

unzip the zipfile DX7toXFM2.zip

put your sys files in the same folder as the **ReadSysEx.class** file. A vaild 32 preset DX7 syx files should always be 4104 bytes long.

a syx file is included as example: aegix.syx

the **conf** directory contains an empty patch and the 32 DX7 algorithms.

The **000init.json** is used as a template where DX7 settings are written to. 

The **out** folder is where the XFM2 patches are written to.

The **out/DX7** folder contains the extracted settings of the DX7 patches. These files can be used to check and compare dx7 with the XFM2 patches. 

## Usage
Run in commanline tool:

### Linux/MacOS

  `java -classpath .:./json_simple-1.1.jar ReadSysEx <filename>.syx`
  
### Windows (not checked)

  `java -classpath .;.\json_simple-1.1.jar ReadSysEx <filename>.syx`
  
