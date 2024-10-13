Examples: don't jsut follow blindly!  
https://github.com/Eemilp/install-opencv-on-wsl   
https://pimylifeup.com/raspberry-pi-opencv/  


## Difficulties  
**`make -j4` too slow**  
use `nproc` command to show number of cores. Don't use too many if you plan to work on something else while compiling!

</br>

**using python to check, after compilation**  
`import cv2          # no error`  
`cv2.__version__     # apparently no such attribute`  
because forgot to `sudo make install` !  
https://stackoverflow.com/questions/65019604/attributeerror-module-cv2-has-no-attribute-version  

</br> 

**importing cv2 failed: opencv compiled with numpy-1-x?**  
https://stackoverflow.com/questions/78641150/a-module-that-was-compiled-using-numpy-1-x-cannot-be-run-in-numpy-2-0-0  
to try to understand why, see this discussion of this issue: apparently, np 2.0 is new, so support is not here yet...  
https://github.com/opencv/opencv-python/issues/943

</br>

**wrong cmake configs: but still works though...**  
**correct:** `OPENCV_PYTHON_INSTALL_PATH=/home/username/.local/lib/python3.10/site-packages`  
**wrong:** `OPENCV_PYTHON_INSTALL_PATH=/home/username/.local/lib/python3.10/site-packages/`  
cmake output:  
**wrong:** `install path: /home/yucheng/.local/lib/python3.10/site-packages//cv2/python-3.10`

</br>

**where should python module be installed**
```
pip show numpy      # gives installation location
which python3
which jupyter
cd <directory>
ls -d folder_name/
ls -d */ | wc
```

</br>

**Don't delete build if you want to uninstall!**  
`sudo make uninstall`

</br>

But I did not really understood all the configurations. Should have read this:  
**cmake configuration options**  
https://stackoverflow.com/questions/16851084/how-to-list-all-cmake-build-options-and-their-default-values  
https://docs.opencv.org/4.x/db/d05/tutorial_config_reference.html  

</br>
</br>

# Background

**right next to branch, you'll see release and tags**  
https://github.com/opencv/opencv  

https://stackoverflow.com/questions/35979642/what-is-git-tag-how-to-create-tags-how-to-checkout-git-remote-tags   
https://stackoverflow.com/questions/54161556/how-can-i-show-all-the-branches-in-a-repository  
only `git log` works for me though...  
https://stackoverflow.com/questions/3404936/show-which-git-tag-you-are-on  



