The linux distribution my choice is CentOS7 Minimal, because it is full free, precarious and slim.

I use WM(window manager) instead of DE(desktop environment) because of efficiency.

There are my configuration:

`yum install -y gcc gcc-c++ cmake clang python-devel python3-devel git vim`

`yum groupinstall -y "X Window System"`


Note! don't Opera in root

+ WM: dwm+dmenu+compton

patch:`cd dwm`,`git apply patch.diff`
alse,I will choose these patches:dwm-statusbar,slstatus

+ Terminal: st

change the fonts in the config.h,you can list the fonts installed with this command:
`fc-list`
The font name is behind the filename.

+ screenshot: scrot


+ browser: chrome

+ VPN: pppd
`sudo yum install ppp pptp pptp-setup`

+ Font: [yahei_mono]
(https://de-3.offcloud.com/cloud/download/5713129db40677dd57001377/yahei_mono.ttf)

+ PDF: FoxitReader

+ Media: mplayer

+ Games: steam

+ Download: aria2+webui-aria2+ThunderLiXianAssistant+BaiduExporter

+ Team Manager: slack

+ WifiManager: networkmanager
You might see this error:

> /usr/lib64/librsvg-2.so.2: undefined symbol:g_type_class_adjust_private_offset

solve: `sudo yum install -y selinux-policy-devel`

+ Audio driver

`sudo yum install -y pulseaudio`

+ File Manager:vifm

Develop Enviroment

vim:
`vi .vimrc`
```sh
#ts means tabstop
set ts=4
set expandtab
```

opencv:

`cd opencv`

`cmake CMakeLists.txt`

