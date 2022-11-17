.Requirements:

<p dir="ltr"><span style="font-size: medium;"><b><a href="http://termux.com" target="_blank">Termux</a></b><br></span></p>


<b><a href="https://play.google.com/store/apps/details?id=com.realvnc.viewer.android" target="_blank">VNC viewer</a></b>

****


<h3 style="text-align: left;"><span style="font-size: large;">Installation :</span></h3><div><span style="font-size: large;"><br></span></div>
<p dir="ltr"><span style="font-size: medium;">So first we need to install proot-distro <br></span></p><p dir="ltr"><span style="font-size: medium;"><br></span></p>
<p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">pkg update &amp;&amp; pkg install proot-distro </span></blockquote><span style="font-size: medium;"><br><br></span><p></p>
<p dir="ltr"><span style="font-size: medium;">Now install Ubuntu<br></span></p><p dir="ltr"><span style="font-size: medium;"><br></span></p>
<p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">proot-distro install ubuntu</span></blockquote><span style="font-size: medium;"><br><br></span><p></p>
<p dir="ltr"><span style="font-size: medium;">Once Ubuntu is installed, then just login to it<br></span></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">proot-distro login ubuntu</span></blockquote><span style="font-size: medium;"><br></span><p></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Now install Gnome Desktop<br></span></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">apt update &amp;&amp; apt install gnome-session-flashback -y &amp;&amp; apt install gnome-terminal ubuntu-wallpapers dbus-x11 -y</span></blockquote><span style="font-size: medium;"><br><br></span><p></p>
<p dir="ltr"><span style="font-size: medium;">Once installation is completed the we need to setup VNCserver to access GUI, for that create a new session in termux and install vncserver<br></span></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><p dir="ltr"><span style="font-size: medium;">pkg install x11-repo -y &amp;&amp; pkg install tigervnc xorg-xhost -y <br></span></p>
<p dir="ltr"></p></blockquote><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Now start vncserver <br></span></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">vncserver -geometry 1280x720 -listen tcp :1 &amp;&amp; DISPLAY=:1 xhost +</span></blockquote><span style="font-size: medium;"><br></span><p></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Now again go to ubuntu and create a file to start GNOME desktop<br></span></p>
<p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">nano /usr/local/bin/vncstart</span></blockquote><span style="font-size: medium;"><br></span><p></p>
<div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Paste following in it and save the file<br>
</span></p>
</div><p dir="ltr"></p>
<div align="left"><p>&nbsp;</p><blockquote><p dir="ltr"><span style="font-size: medium;"></span></p></blockquote></div><blockquote><div align="left"><blockquote><p dir="ltr"><span style="font-size: medium;">#!/bin/sh<br>
</span></p>
</blockquote>
</div><blockquote><p dir="ltr"></p>
<p dir="ltr"><span style="font-size: medium;">rm -rf /run/dbus/pid</span></p>
<p dir="ltr"><span style="font-size: medium;">dbus-daemon --system</span></p>
<p dir="ltr"><span style="font-size: medium;">dbus-launch&nbsp;</span></p>
<p dir="ltr"><span style="font-size: medium;">DISPLAY=:1 $HOME/.vnc/xstartup</span></p></blockquote></blockquote><blockquote><p dir="ltr"><span style="font-size: medium;"><br>
</span></p>
</blockquote>
<p dir="ltr"><span style="font-size: medium;"><br><br></span></p>
<div align="left"><p dir="ltr"><span style="font-size: medium;">Give executable permission&nbsp;<br>
</span></p>
</div><p dir="ltr"></p>
<div align="left"><p>&nbsp;</p><blockquote><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">chmod +x /usr/local/bin/vncstart</span></blockquote><span style="font-size: medium;"><br>
</span><p></p>
</blockquote>
</div><p dir="ltr"></p>
<div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Now create xstartup file for VNC<br>
</span></p>
</div><p dir="ltr"></p>
<div align="left"><p>&nbsp;</p><blockquote><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">mkdir $HOME/.vnc &amp;&amp; nano $HOME/.vnc/xstartup</span></blockquote><span style="font-size: medium;"><br>
</span><p></p>
</blockquote>
</div><p dir="ltr"></p>
<div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">paste following in it and save it<br>
</span></p>
</div><p dir="ltr"><span style="font-size: medium;"><br></span></p>
<div align="left"><blockquote><p dir="ltr"><span style="font-size: medium;"></span></p></blockquote></div><blockquote><div align="left"><blockquote><p dir="ltr"><span style="font-size: medium;">#!/bin/sh<br>
</span></p>
</blockquote>
</div><blockquote><p dir="ltr"><span style="font-size: medium;"><br>
export XKL_XMODMAP_DISABLE=1</span></p>
<p dir="ltr"><span style="font-size: medium;">unset SESSION_MANAGER</span></p>
<p dir="ltr"><span style="font-size: medium;">unset DBUS_SESSION_BUS_ADDRESS</span></p>
<p dir="ltr"><span style="font-size: medium;">[ -x /etc/vnc/xstartup ] &amp;&amp; exec /etc/vnc/xstartup</span></p>
<p dir="ltr"><span style="font-size: medium;">[ -r $HOME/.Xresources ] &amp;&amp; xrdb $HOME/.Xresources</span></p>
<p dir="ltr"><span style="font-size: medium;">xsetroot -solid grey</span></p>
<p dir="ltr"><span style="font-size: medium;">gnome-panel &amp;</span></p>
<p dir="ltr"><span style="font-size: medium;">metacity &amp;</span></p>
<p dir="ltr"><span style="font-size: medium;">gnome-flashback &amp;<br></span></p></blockquote><p>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;panel &amp;</p>
<p dir="ltr"></p>
<div align="left"><p dir="ltr"></p></div></blockquote><div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Give executable permission<br>
</span></p>
</div><p dir="ltr"></p>
<div align="left"><p><br></p><p>&nbsp;<span style="font-size: large;"></span></p></div><blockquote><div align="left"><p><span style="font-size: large;">chmod +x $HOME/.vnc/xstartup</span></p></div><blockquote><p dir="ltr"></p>
<div align="left"><p dir="ltr"></p></div></blockquote><div align="left"><p dir="ltr"></p></div></blockquote><div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Start GNOME desktop&nbsp;<br>
</span></p>
</div><div align="left"><p>&nbsp;</p><blockquote><p dir="ltr"><span style="font-size: medium;"></span></p><blockquote><span style="font-size: medium;">vncstart</span></blockquote><span style="font-size: medium;">
</span><p></p>
</blockquote>
</div><div align="left"><blockquote><p dir="ltr"></p>
</blockquote>
</div><div align="left"><p dir="ltr"><span style="font-size: medium;"><br></span></p><p dir="ltr"><span style="font-size: medium;">Now open VNC viewer and create a connection with localhost:1 and connect to it.


*****
 termux-setup-storage
 
 pkg install wget
 
 wget -O install-nethunter-termux https://offs.ec/2MceZWr
 
 chmod +x install-nethunter-termux
 
 ./install-nethunter-termux
 


---------------

Intel Core2 or newer, or AMD Steamroller or newer CPU. ARM CPUs are not
supported.
64 bit Linux operating system. Apple is not supported.



$ sudo apt-get install build-essential automake libssl-dev libcurl4-openssl-dev libjansson-dev libgmp-dev zlib1g-dev git



. Download cpuminer-opt
------------------------

Download the source code for the latest realease from the official repository.

https://github.com/rplant8/cpuminer-opt-rplant/releases

Extract the source code.

$ tar xvzf cpuminer-opt-linux.tar.gz


Alternatively it can be cloned from git.

$ git clone https://github.com/rplant8/cpuminer-opt-rplant/releases/download/5.0.29/cpuminer-opt-linux.tar.gz
 
 $ git clone https://github.com/rplant8/cpuminer-opt-rplant/archive/refs/tags/5.0.29.tar.gz
 
 
 wget https://github.com/rplant8/cpuminer-opt-rplant/releases/download/5.0.29/cpuminer-opt-linux.tar.gz
 
 Normal text editors are nano, or vi.

For example:

root@user:# nano galfit.feedme
or

root@user:# vi galfit.feedme

For exiting

Press Esc

    :wq //for exiting and saving
    :q! //for exiting without saving
    
 <span data-coinwidget-instance="0" class="COINWIDGETCOM_CONTAINER"><a class="COINWIDGETCOM_BUTTON_BITCOIN" href="#"><img src="http://pool.rplant.xyz/static1/img/uranium-x.png"><span>Donate UraniumX</span></a><span>UY6suqgq1DXHeJtjhjTN6m8Rqkwy4H82P2</span></span>
 
 
 
 UY6suqgq1DXHeJtjhjTN6m8Rqkwy4H82P2
