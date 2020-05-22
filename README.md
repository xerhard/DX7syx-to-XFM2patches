# DX7syx-to-XFM2patches
Quick and dirty convertion of DX7 sysex files containing 32 presets into XFM2 json patch files.

Code is built on javac 11.0.7


## File/Directory structure

unzip the zipfile **DX7toXFM2.zip**

put your sysex files in the same folder as the **ReadSysEx.class** file. A valid 32 preset DX7 syxex files should always be 4104 bytes long.

A sysex file is included as example: aegix.syx

the **conf** directory contains an empty patch and the 32 DX7 algorithms.

The **000init.json** is used as a template where DX7 settings are written to. 

The **out** folder is where the XFM2 patches are written to.

The **out/DX7** folder contains the extracted settings of the DX7 patches. These files can be used to check and compare DX7 with the XFM2 patches. 

## Usage
Run in commanline tool:

### Linux/MacOS

```
cd <path_to_unzipped_location>/DX7toXFM2
java -classpath .:./json_simple-1.1.jar ReadSysEx <filename>.syx
```
  
### Windows (not checked)

```
cd <path_to_unzipped_location>\DX7toXFM2
java -classpath .;.\json_simple-1.1.jar ReadSysEx <filename>.syx
```

  
