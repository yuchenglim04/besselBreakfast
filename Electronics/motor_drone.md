## Background reading
How Brushless Motor and ESC Work and How To Control them using Arduino  
https://youtu.be/uOQk8SJso6Q  
- 3 phase: 2 active, 1 inactive at a time
- back emf: the floating coil
- $K_V$ and RPM
- BEC line: same way to control ESC as servo: 50Hz PWM, greater duty cycle, greater speed: 1ms to 2ms?
- arming of the ESC: minimum value???

How to measure $K_V$ of motor  
https://fishpepper.de/2017/10/17/tutorial-how-to-measure-the-kv-of-a-brushless-motor/

Load cell  
https://youtu.be/sxzoAGf1kOo?si=cU87RI_PW1aGcbZx  

XFLY-MODEL 50mm 12 Blades EDF Ducted Fan with 4S 2627-KV4600  
https://www.aliexpress.com/item/1005006159284786.html  

SimonK Firmware Flashing Tutorial (Brushless Drive)  
https://youtu.be/MQQX7IIdAtI

What flashing means  
https://oscarliang.com/flash-esc-simonk-firmware-arduino-without-usbasp/

RC Basics - Understanding Electronic Speed Controllers (ESC)  
https://youtu.be/OZNxbxL7cdc  
  
Control Brushless Motor Using Arduino  
https://youtu.be/DTOK6CgXRXg  



## Problem log
Problem  
Solution  

**How does maximum current come in, how related to speed/torque/duty cycle?**  
https://powerdrives.net/blog/what-is-an-esc  
**Is there current limiting/overcurrent protection?**  
https://www.rcgroups.com/forums/showthread.php?2497878-ESC-current-ratings-limiter  
Current vs voltage  
Speed vs voltage  
Current vs speed  
Ideas:
- current through magnetic field -> force
- voltage supplied is to overcome back emf for current
- steady speed: current depends on resistive forces. Voltage affected by speed and current.

**So, what happens when you start the motor?**  
Initially motor not moving. Current increases from 0. Torque increases, accelerating the shaft. Speed increases, current decreases so that back emf constant at applied voltage. Maximum speed, minimum current to apply minimum torque to overcome friction etc.  
**Check out the plots of current, torque, speed!**  
https://motoranalysis.com/motoranalysis-im/simulation-of-induction-motor-startup/  
https://pdfs.semanticscholar.org/3208/6d58b4eac62a135e392cec0607eb24ad5cbd.pdf  
LTSpice Tutorial - Modeling a DC brushed motor  
https://youtu.be/Wc4XzTrWSpo?si=VNr_Bw-K6fj8ukBM  

PWM duty cycle signal input  
Actual duty cycle output by ESC in time  
Duty cycle after a long time/stabilized ESC output  



**DC motors have smooth shaft. How to attach load!??**



our motor:
outrunner
