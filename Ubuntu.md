# Ubuntu Setup

## Setup LocalWP
https://localwp.com/
Downloaded .deb file and tried to install with below command

`apt-get install ./local-9.2.4-linux.deb `
Error:

The following information may help to resolve the situation:

The following packages have unmet dependencies:
 local : Depends: libaio1 but it is not installable
         Depends: libncurses5 but it is not installable
E: Unable to correct problems, you have held broken packages.

Solution:
Install some packages by installing from this location:
https://community.localwp.com/t/installation-failed-in-ubuntu-24-04-lts/42579/3

