# xios_snap

last snapshot of my xios blockchain files

# Ubuntu

Edit the first line and copy paste

<pre>myxiosfolder="/root/.XIOS1" <b># EDIT TO YOUR .XIOS CONF PATH</b>

# Stop your node
cd
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf stop
# Remove your current database
rm -r $myxiosfolder/database
rm -r $myxiosfolder/txleveldb
rm $myxiosfolder/banlist.dat
rm $myxiosfolder/peers.dat
# Get the last blockchain snap
git clone https://github.com/dirtyak/xios_snap
# Put this db in your folder
cp -r xios_snap/* $myxiosfolder/.
# Restart the node with new files
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf -daemon</pre>

# Windows 

Open explorer and go to <b>%APPDATA%/XIOS</b>

Remove <b>database</b> & <b>txleveldb</b> folders

Download the blockchain files : https://github.com/dirtyak/xios_snap/archive/master.zip

Unzip it into <b>%APPDATA%/XIOS</b> and replace files

Restart Wallet
