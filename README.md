.Requirements:

<p dir="ltr"><span style="font-size: medium;"><b><a href="http://termux.com" target="_blank">Termux</a></b><br></span></p>


<b><a href="https://play.google.com/store/apps/details?id=com.realvnc.viewer.android" target="_blank">VNC viewer</a></b>

****



<div class="entry-header blog-entry-header has-meta">
<nav id="breadcrumb"><a class="home" href="https://technical-bot.blogspot.com/">Home</a></nav>
<script type="application/ld+json">{"@context":"http://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://technical-bot.blogspot.com/"},{"@type":"ListItem","position":2,"name":"Uncategorized","item":"https://technical-bot.blogspot.com/search/"},{"@type":"ListItem","position":3,"name":"How to install Ubuntu GNOME Desktop on Android with Termux | No Root","item":"https://technical-bot.blogspot.com/2022/10/how-to-install-ubuntu-gnome-desktop-on.html"}]}</script>
<h1 class="entry-title">How to install Ubuntu GNOME Desktop on Android with Termux | No Root</h1>
<div class="entry-meta">
<div class="align-left">
<span class="entry-author"><span class="author-avatar lazy-ify" data-image="//3.bp.blogspot.com/-yZX_B1nAmAg/YVSxHTzvTOI/AAAAAAAAADU/UIaX-o32jakfvW4j1abqYIJwF4NpicetQCK4BGAYYCw/w72-h72-p-k-no-nu/20210606_191532.jpg" style="background-image:url(https://3.bp.blogspot.com/-yZX_B1nAmAg/YVSxHTzvTOI/AAAAAAAAADU/UIaX-o32jakfvW4j1abqYIJwF4NpicetQCK4BGAYYCw/w26-h26-p-k-no-nu/20210606_191532.jpg)"></span>
<span class="by">by</span><span class="author-name">Technical Bot</span></span>
<span class="entry-time"><span class="on">Published on</span><time class="published" datetime="2022-10-27T07:41:00-07:00">October 27, 2022</time></span>
</div>
<div class="align-right">
<span class="entry-comments-link show">0</span>
</div>
</div>
</div>
<div class="entry-content-wrap">
<div class="post-body entry-content" id="post-body">

<ins class="adsbygoogle" data-ad-client="ca-pub-4676723305138770" data-ad-format="fluid" data-ad-layout="in-article" data-ad-slot="8676836602" style="display:block; text-align:center;"><iframe id="aswift_1" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;"><iframe id="google_ads_frame1"></iframe></iframe></ins>

<p><span style="font-size: medium;">&nbsp;</span></p><div class="separator" style="clear: both; text-align: center;"><span style="font-size: medium;"><a href="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEglD5v-g528TEcyo6vzb32ic5Wb1jOZSPeP5zlQfoBt4u4Uv_qCkeZWGX1a53ov2PTI-8KxbaXcqfOffcGbwBzjiX9pKlXlmsVAe8_32jFpM9E5z0gxZ07MpyOLv-zDsSpfMbjyPZWtm0_2Haz2Qqgmk6XLnOPoFSyRHxQAONJ-8Ifi2L4t7YJ8j5vX/s1280/2022-10-27_20-09-34.jpg" imageanchor="1" style="clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"><img data-original-height="720" data-original-width="1280" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEglD5v-g528TEcyo6vzb32ic5Wb1jOZSPeP5zlQfoBt4u4Uv_qCkeZWGX1a53ov2PTI-8KxbaXcqfOffcGbwBzjiX9pKlXlmsVAe8_32jFpM9E5z0gxZ07MpyOLv-zDsSpfMbjyPZWtm0_2Haz2Qqgmk6XLnOPoFSyRHxQAONJ-8Ifi2L4t7YJ8j5vX/s320/2022-10-27_20-09-34.jpg" width="320" height="180" border="0"></a></span></div><span style="font-size: medium;"><br></span><p></p><p dir="ltr"><span style="font-size: medium;">Ubuntu uses GNOME as their default desktop. So, In this article we will see how we can install Ubuntu GNOME Desktop on Android via Termux and you don't need root access to install it.<br></span></p>
<p dir="ltr"><span style="font-size: medium;">As GNOME uses systemd which cannot be used in Android without root so will uses GNOME flashback which doesn't require systemd.<br></span></p><p dir="ltr"><span style="font-size: medium;"><br></span></p>
<h3 style="text-align: left;"><span style="font-size: large;">Prerequisite :</span></h3>
<p dir="ltr"><span style="font-size: medium;"><b><a href="http://termux.com" target="_blank">Termux</a></b><br></span></p><p dir="ltr"><span style="font-size: medium;"><b><a href="https://play.google.com/store/apps/details?id=com.realvnc.viewer.android" target="_blank">VNC viewer</a></b></span></p><p dir="ltr"><span style="font-size: medium;"><b><br></b></span></p><p dir="ltr"><span style="font-size: medium;"></span></p><div class="separator" style="clear: both; text-align: center;"><span style="font-size: medium;"><iframe allowfullscreen="" class="BLOG_video_class" src="https://www.youtube.com/embed/eU6j1HwhBVk" youtube-src-id="eU6j1HwhBVk" width="320" height="266"></iframe></span></div><span style="font-size: medium;"><br><b><br></b></span><p></p><p dir="ltr"><span style="font-size: medium;"><b><br></b></span></p>
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
    
 UY6suqgq1DXHeJtjhjTN6m8Rqkwy4H82P2
