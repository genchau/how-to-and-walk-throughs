#### Objective:
Installing a working version of Ubuntu on top of Windows 10. This is the whole graphical interface of Ubuntu not just CLI.

#### Situation:
Doing it just for fun for now. I don't have a use for it yet.

#### Resources:
https://www.youtube.com/watch?v=c4M8zKPEisQ

#### My Equipment:
Dell 7559
Windows 10

#### Procedure:
1. Windows Store: Install ubuntu
2. In Ubuntu CLI, run `sudo apt update`
3. `sudo apt upgrade`
4. download/install: `https://sourceforge.net/projects/vcxsrv/`
5. `sudo apt install xfce4`
6. `nano ~/.bashrc`
7. Add this line to the bottom: `export DISPLAY=:0.0`
8. Start XLaunch. Large window worked for me. Can check "Disable access control". 
9. Run `xfce4-session`
