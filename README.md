A blot that can draw 30cm x 50cm! Controlled with an arduino and 4 stepper motors, it runs the GRBL firmware and uses the CNC shield with 4 a4988 stepper drivers.   
  
In total I spent around $200 CAD on this project, but it will cost way more if you buy it from the amazon links I provided. There are definitely cheaper alternatives online, and you can find them pretty easily through research.  

I built this as a project to pass the time while waiting for an acutal hack club blot, but it turned into an adventure of pen plotters, GRBL, and much much more.   

If you would like to create your own, here are the parts I used to build the project:  

# Electrical Parts  
1x Arduino + CNC sheild + 4x a4988 Motor drivers  
https://www.amazon.ca/DAOKI-Expansion-Arduino-Heatsink-Engraving/dp/B08KFYKKN4/  

4x NEMA17 Stepper Motors (I used 3x normal and 1x pancake for Z axis)  
https://www.zyltech.com/store/stepper-motors/nema-17-motors/  

# Mechanical Parts  
3x 2020 aluminium extrusions (I used 1M here but you can use any length youd like)  
https://www.zyltech.com/2020-v-groove-extrusion-pre-cut-lengths-300mm-2000mm/?sku=EXT-2020-REG-300-VGRV

3x V-slot gantry plates + POM wheels (These are 3D printable, but they have horrible tolerances and are not rigid enough for precise drawings)  
https://www.amazon.ca/Standard-Aluminum-Dimensional-Printer-Accessories/dp/B0B5DY7XLH

A ton of m5 bolts, washers, nuts, and V groove nuts. (didn't really keep count of how many!)  
https://www.amazon.ca/Screws-Stainless-Thread-Bright-Machine/dp/B09TDRJ5GR/
https://www.amazon.ca/Boeray-Carbon-Hammer-Aluminum-Extrusion/dp/B01G7ZYHHI/

1x 5m GT2 belt (you might need more! YMMV)  
https://www.amazon.ca/HICTOP-Printer-Timing-Meters-Creality/dp/B00YMM6IQW/

3x belt tensioner (you can replace these with 3d printed parts)
https://www.amazon.ca/Garosa-Straighten-Synchronous-Stretching-Straightening/dp/B09QKPZSHZ/

1x Linear rail (you only need 10cm/100mm)  
https://www.zyltech.com/zyltech-mgn9-linear-rail-with-single-or-double-carriage-block/

and a ton of 3d printed parts!   
All 3d printed parts are printed using the bambu lab a1 mini, stock profile, 200mm/s, 30% infill.

# Printed Parts  
1. 2x y axis motor mount v2  
![image](https://github.com/user-attachments/assets/341bea2c-4da8-4b20-ae75-a19801528ce6)  

2. 2x extrusion mount v2  
![image](https://github.com/user-attachments/assets/fb5bb205-a7dd-4d95-b796-0c06fd3610e9)  

3. 1x X axis motor mount v2  
![image](https://github.com/user-attachments/assets/833f4ddf-7fd5-4d77-8571-f1c674949353)  

4. 1x pen motor mount  
![image](https://github.com/user-attachments/assets/3991d896-ed29-4872-b756-6c095fe516b1)  
  
![image](https://github.com/user-attachments/assets/b6ee275e-d1fd-47d4-af19-828cbc1ebd6b)


# Electronics  
For the arduino case, you can make any one you want, I just found one off of thingiverse. 


There are many tutorials on youtube as to how to build a cnc machine with this type of setup, I have linked a few that I used.  
https://www.youtube.com/watch?v=Xlkmso01vUk&t=6s  
https://www.youtube.com/watch?v=5qAwCg7XPZw (Replace the linear rods with the extrusion and vslot gantries.)  
  

A few notes, a 12V source is required to power this, and gets screwed into the terminals:  
![image](https://github.com/user-attachments/assets/b7a0064d-c230-4a93-acea-fe5a74dea8b2)

And you need to make sure that the stepper motors are microstepped. Under each stepper motor driver slot, there are 6 pins, make sure they are all shorted:  
![image](https://github.com/user-attachments/assets/f6568c5c-3b0b-45f8-8ae5-dc1213cf86f0)  
Short from top to bottom like so:    
![image](https://github.com/user-attachments/assets/6980463a-a608-4daa-a116-48cfffb0b79a)  


# Software 
When everything is built correctly, upload the GRBL firmware to the arduino, there are many tutorials on youtube, but it is fairly straight forward if you have experience with arduino.   
https://www.youtube.com/watch?v=Xlkmso01vUk&t=6s

And thats about it! Have fun with the plotter, and to send gcode to it, use a program such as G-sender or UGS, and generate gcode using vpype!  
G-sender: https://sienci.com/gsender/  
UGS: https://winder.github.io/ugs_website/  
vpype: https://github.com/abey79/vpype  

:)
