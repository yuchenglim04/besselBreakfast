#OpenEMS Python Interface Installation Tips

https://www.youtube.com/watch?v=VcJqhsbzR3c&ab_channel=panire  
https://github.com/thliebig/openEMS-Project/discussions/125  
https://docs.openems.de/python/install.html#python-windows-install  

```
cd  C:\pythonEnv

myenv3.11\Scripts\activate

cd C:\openEMS\python

pip install numpy h5py matplotlib cython
pip install CSXCAD-0.6.3-cp311-cp311-win_amd64.whl
pip install openEMS-0.0.36-cp311-cp311-win_amd64.whl

setx OPENEMS_INSTALL_PATH C:\openEMS

cd Tutorials
 
Bent_Patch_Antenna.py
```
to test OpenEMS Simulation Program

#OpenEMS Python Octave Installation Tips
https://octave.org/download
https://octave.discourse.group/t/workaround-for-weird-behavior-of-command-window-widget-in-windows/4981

```
Warning on Octave GUI by changing from Windows Terminal to Windows Console Host
Goto Windows Terminal Settings -> System For Developers -> Terminal -> Let Windows Choose to Windows Console Host

goto windows explorer
click on "C:\openEMS\matlab\Tutorials\Bent_Patch_Antenna.m"

At Octave GUI console messages, type 'Yes' to proceeed!
```
