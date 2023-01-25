*******************************************************************************************

Working with P2 (Parallax Propller 2) - flexprop build for Fedora 37

flexprop release:
https://github.com/totalspectrum/flexprop/releases/tag/v5.9.23

******************************************************************************************

1. Download flexprop.tar.gz and unzip it into /opt (so that it’s /opt/flexprop):

sudo tar -xvzf p2llvm.tar.gz -C /opt

*****************************************************************************************

2. Create symbolic link for flexprop:

sudo ln -s /opt/flexprop/flexprop /usr/local/bin/flexprop 

or 

Download flexprop link from this repository and copy it using -P option to usr/local/bin:

sudo cp -P flexprop /usr/local/bin

****************************************************************************************
