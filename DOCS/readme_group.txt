How to?

to introduce a term in the index:
1) Use the following tag
<term>Word-in-document</term><idx><h>Parent-Word-in-index</h><h>son-word-in-index</h></idx> 

2) put enumerated equations in a row
 <mdn>
    <mrow xml:id="labelforequation" >
    Equation-in-Latex-Mode
    </mrow>
</mdn>
3) put non-enumerated equations in a row
<me>
  Equation-in-Latex-Mode
</me>

4) put equation in line <m>w_i</m>

5) put a plot (need to be tested)
<figure xml:id ="figure-label">
<caption> figure caption</caption>
<image xml:id="sageplot-updown" width="45%">
    <sageplot>
    f(x) = x^2
    g(x) = - x^2
    up = plot(f, (x,-1.5,1.5), color="blue", thickness=2)
    down = plot(g, (x,-1.5,1.5), color="red", thickness=2) 
    up + down   
    </sageplot>
 </image>
 </figure>   

Reference: https://www.youtube.com/watch?v=Z-BfcnZ8Sm8


6) Figures are not working: I tried with 
  <figure xml:id="fig-dotPlots">
    <caption>A vertical dot plot.</caption>
  <image source="JO.png" width="40%"> </image> 
  </figure>

  LG: Possible solution for including images:
  <image source="[put file name here]"> </image>
  For some reason, when trying to find the file pretext looks in the /output/web/external folder and I can't get it to look at a different path, so we might need to just put image files in this folder


-----------------------
Latex packages:
Put the following lines in the main/docinfo file between 
<latex-image-preamble>
- \usepackage{tiks, pgplots}
- \usetikzlibrary{positioning, matrix, arrows}
- \usetikzlibrary{shapes, decorations, shadows, fadins, patterns}
- \usetikzlibrary{decroations.markings}

-----------------------
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
c) sudo kill -9 $(sudo lsof -t -i:8000)

3) to push a change from local to remote repository:
- git init
- git add .
- git commit -m "[MESSAGE GOES HERE]"
- git push

to to pull a change from remote repository to local:
- git init
- git add .
- git commit -m "[MESSAGE GOES HERE]"
- git pull
- git push (if you made changes)

-----------------------

Here are the hex color codes for our pretext website
Dark Red: #671d12
Blue: #3572A0
