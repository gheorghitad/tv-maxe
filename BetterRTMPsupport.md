# Introduction #

**rtmpdump** is a tool for dumping RTMP streams from internet, developed and maintained by MPlayer developers. Unfortunately, the official builds of **rtmpdump** are pretty old and they're missing some features introduced in Adobe's Flash Player 10 so, to be able to play RTMP streams fine in TV-Maxe we'll need to compile a patched version of it.

# Details #

First, we need to download the sources of the unofficial **rtmpdump**'s version. To do this, run:
```
# link removed because of legal issues. You'll need to manually find the Xeebo's patches for *rtmpdump*.
```
After that you need to install the development tools and headers for your distribution. In Ubuntu, this can be done with:
```
sudo apt-get install build-essential gcc make subversion libssl0.9.8 libssl-dev libssl0.9.8
```
Unzip the archive's content:
```
unzip rtmpdump-v2.5.zip -d rtmpdump
```
CHDIR to the source's directory:
```
cd rtmpdump/
```
Compile and install this unofficial version of **rtmpdump**:
```
make SYS=posix XLIBS="-lm" SHARED="no"
sudo make install
```

If all is ok, **rtmpdump** should compile and install in a few seconds. To make sure that all was ok, run:
```
rtmpdump --help 2>&1 | grep RTMPDump
```
If you get **RTMPDump v2.5 GIT-2012-03-31 (Handshake 10 support by Xeebo)** it means that everything was ok and you're now able to play RTMP streams fine on TV-Maxe.