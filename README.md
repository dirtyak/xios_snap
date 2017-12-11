# xios_snap

update to my last snap of the xios blockchain

# Ubuntu

<pre>myxiosfolder="/root/.XIOS1" <b># EDIT TO YOUR .XIOS CONF PATH</b>

# Stop your node
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf stop
# Remove your current database
rm -r $myxiosconf/database
rm -r $myxiosconf/txleveldb
rm $myxiosconf/banlist.dat
rm $myxiosconf/peers.dat
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
