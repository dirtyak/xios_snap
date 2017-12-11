# Ubuntu

<pre>cd
git clone https://github.com/dirtyak/xios_snap
myxiosconf="/root/.XIOS1"  # Replace by your XIOS conf folder 
rm -r $myxiosconf/database
rm -r $myxiosconf/txleveldb
rm $myxiosconf/banlist.dat
rm $myxiosconf/peers.dat
cp -r xios_snap/* $myxiosconf/.</pre>

# Windows 
