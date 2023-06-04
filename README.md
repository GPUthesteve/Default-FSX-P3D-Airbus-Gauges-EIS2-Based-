# Default-FSX-P3D-Airbus-Gauges-EIS2-Based-
Default FSX/P3D Airbus Gauges in EIS2 format. 
Here, I will only provide things I've newly implemented into the gauges like background bitmap or some XML code. Original Sources can be found in old cabinet file. Or download it somewhere.


Usage
I hope you guys ~~know~~ remember how to call XML gauges from folder... Well i'll remind you how.
In panel.cfg:

Prirority of Calling : Local root panel/gauge folder (*aircraft folder*\panel) >simroot panel/gauge folder  (*simroot*\gauges)
while xx=sequence of gauge in specified window from 00 to inf?
filename, folder is not really case sensitive but please treat it as is.
calling for folder can be any slash but please don't mix it in a line.
```
//Example of Pop-up Window and calling XML gauge or Compiled SimPropBinary (.spb) from folder.
[Windowxx]//00 to inf
Background_color=0,0,0 //black, in order of rgba
size_mm=...//something pixel
visible=0//you don't want your pop-up to be displayed from the beginning, else set it to 1
ident=...//anything that is unique per window or vcockpit

gaugexx=foldername!xmlfile,  posx,posy,sizex,sizey,arguments
//or, Example of virtual cockpit gauge/panel and calling c-compiled gauge like .dll or .gau
[Vcockpit01]//vcockpit can only be 01 to inf
Background_color=0,0,0 
size_mm=1024,1024
visible=1
pixel_size=1024,1024//can be 4096,4096 but lags the simulator cuz of AA
texture=$texturename//name specified in modeling tool

gaugexx=foldername if present (not root)/filename!function,  posx,posy,sizex,sizey,arguments
```

glhf, correct me if im wrong. -GPUthesteve
