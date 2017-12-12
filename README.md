# xios_snap

last snapshot of my xios blockchain files

# Ubuntu

Use this script if you are stuck on the wrong blockchain

This script keeps your wallet.dat safe

Edit the first line and copy paste

<pre>myxiosfolder="<b>/root/.XIOS1</b>" # <b>CHANGE TO CORRECT .XIOS PATH</b>

# Stop your node
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf stop
# Remove your current database
rm -r $myxiosfolder/database
rm -r $myxiosfolder/txleveldb
rm $myxiosfolder/banlist.dat
rm $myxiosfolder/peers.dat
rm $myxiosfolder/blk0001.dat
# Get the last blockchain snap
cd
git clone https://github.com/dirtyak/xios_snap
# Put this db in your folder
cp -r xios_snap/* $myxiosfolder/.
# Restart the node with new files
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf -daemon</pre>

# Windows 

Close your XIOS wallet

Open explorer and go to <b>%APPDATA%/XIOS</b> (default path)

Remove <b>database</b> & <b>txleveldb</b> folders

Run XIOS one time to populate files and close it (make sure it's not running in background)

Download the blockchain files : https://github.com/dirtyak/xios_snap/archive/master.zip

Unzip it into <b>%APPDATA%/XIOS</b> and replace files

Restart Wallet
