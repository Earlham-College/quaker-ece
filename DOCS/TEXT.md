TEXT:

This is guide to use this pretext book

1) Commands

pretext new -d .
pretext build
pretext view
fuser -k 8128/tcp
pretext deploy -u

It is deployed in: https://earlham-college.github.io/quaker-ece/


To change the path
conda create -p ~/github/BkQC151

To install a pretext version
python3 -m pip install --user pretext==1.7.5

To refresh the requirements
pretext init --refresh 

Or
You should change the requirements.txt file.


2) Mac: IOSX Apple.

Commands
Kill a port:
a) lsof -i tcp:XXXX
b) kill -9 PID-XXXX

