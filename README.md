# xios_snap

last snapshot of my xios blockchain files

# Ubuntu (tested it works)

Use this script if you are stuck on the wrong blockchain

This script keeps your wallet.dat safe

Edit the first line and copy paste in console <b>as root</b> :

<pre>myxiosfolder="<b>/root/.XIOS1</b>" # <b>CHANGE TO CORRECT .XIOS PATH</b>

# Stop your node
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf stop
# Remove your current files (except backups/ wallet.dat XIOS.conf & masternode.conf)
rm -r $myxiosfolder/database
rm -r $myxiosfolder/txleveldb
rm -r $myxiosfolder/smsgDB
rm -r $myxiosfolder/smsgStore
rm $myxiosfolder/banlist.dat
rm $myxiosfolder/blk0001.dat
rm $myxiosfolder/db.log
rm $myxiosfolder/debug.log
rm $myxiosfolder/mncache.dat
rm $myxiosfolder/peers.dat
rm $myxiosfolder/smsg.ini
rm $myxiosfolder/XIOSd.pid
# Get the last blockchain snap
cd
git clone https://github.com/dirtyak/xios_snap
# Put this db in your folder
cp -r xios_snap/* $myxiosfolder/.
# Restart the node with new files
/root/xios/src/XIOSd -datadir=$myxiosfolder -config=$myxiosfolder/XIOS.conf -daemon</pre>

# Windows (not working properly)

Close your XIOS wallet

Open explorer and go to <pre>%APPDATA%/XIOS</pre> (default path)

Remove all files <b>except backups, wallet.dat, XIOS.conf and masternode.conf</b>

Run XIOS one time to populate files and close it (make sure it's not running in background)

Download the blockchain files : https://github.com/dirtyak/xios_snap/archive/master.zip

Unzip it into <b>%APPDATA%/XIOS</b> and replace files

Restart Wallet
