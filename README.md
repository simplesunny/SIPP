# SIPP

Once you have your server instance created login via ssh and install the following dependancies for Sipp.

yum install make gcc gcc-c++ ncurses ncurses.x86_64 ncurses-devel ncurses-devel.x86_64 openssl libnet libpcap libpcap-devel libpcap.x86_64 libpcap-devel.x86_64 gsl gsl-devel
Now that all the dependancies are installed download and extract the Sipp source code.

cd /usr/src
wget https://sourceforge.net/projects/sipp/files/sipp/3.4/sipp-3.3.990.tar.gz
OR
wget https://excellmedia.dl.sourceforge.net/project/sipp/sipp/3.4/sipp-3.3.990.tar.gz
tar -zxvf sipp-3.3.990.tar.gz
The next step is to compile the Sipp application, so we need to go to the Sipp directory and run make.

cd /usr/src/sipp-3.3.990
./configure
make all
Now Sipp is compiled and you can start using it with the following commands.

cd /usr/src/sipp-3.3.990
./sipp -sn uac -d 200000 -s 123456789 127.0.0.1 -l 10 -r 2 -m 10
