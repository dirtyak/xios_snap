# xios_snap
last snapshot of my xios blockchain files

# Ubuntu procedure

<pre>
# EDIT TO YOUR CORRECT PATH
XIOSPATH="/root/.XIOS"
XIOSdPATH="/root/xios/src/XIOSd"

# Stop XIOSd
$XIOSdPATH -datadir=/root/$FOLDER -config=/root/$FOLDER/XIOS.conf stop

# Remove old files
rm -r $XIOSPATH/database
rm -r $XIOSPATH/txleveldb
rm $XIOSPATH/banlist.dat
rm $XIOSPATH/peers.dat
rm $XIOSPATH/blk0001.dat

# Clone this repo
git clone https://github.com/dirtyak/xios_snap/

# Make a copy of this repo to your XIOS path
cp -r xios_snap/database $XIOSPATH/.
cp -r xios_snap/txleveldb $XIOSPATH/.
cp xios_snap/banlist.dat $XIOSPATH/.
cp xios_snap/peers.dat $XIOSPATH/.
cp xios_snap/blk0001.dat $XIOSPATH/.

# Restart XIOSd
$XIOSdPATH -datadir=$XIOSPATH -config=$XIOSPATH/XIOS.conf start
</pre>

# Windows procedure

- Close the Wallet
- go to your config files path <pre>%APPDATA%/XIOS</pre>
- Remove all files <b>EXCEPT</b> :
<pre>
Backups (folder)
wallet.dat
XIOS.conf
masternode.conf
</pre>
- Restart the wallet one time to populate files and close it
- Download the blockchain snapshot : https://github.com/dirtyak/xios_snap/archive/master.zip
- Unzip and copy all files to <pre>%APPDATA%/XIOS</pre>
- Restart the wallet
