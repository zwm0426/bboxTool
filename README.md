## Introduction to Bounding-Box Propagating Tool

The bounding-box propagating tool is an effective tool for generating bounding-box in image set by users' input.

### Before Using
Before you using this tool, you have to setup the envrioment below:

```
MATLAB R2016a (or later version)
openCV 2.4 (or later version)
Microsoft Visual Studio 2010 (or later version)
```

Then, you need to setup the RP method in MATLAB by using commands below:

```
**In MATLAB **
>>> addpath('compile')
>>> addpath('cmex')
>>> gbvs_install
>>> gbvs_compile
```

Next, you need to compile the file of MBS(?) saliency map by: 

```
**In MATLAB **
>>> addpath('mex')
>>> compile_win
```

### While Using

The GUI of this tool:
<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/GUI.JPG?raw=true) </center>


* You should select the input directory, output directory and evaluation directory (optional). 
* Then, click "Run" button.
* After you click "Run" button, all the directory are set and cannot be changed.

Then, the program will choose the images from input image set.

<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/gui3.JPG?raw=true) </center>

* You can use your mouse dragging on the image to bound the object, those object would be used as the 
* If the image is the noise image, you can just click the image and our algorithm will ignore this image.

After your annotation, this tool will proceed to propagate bounding-box. We would show every result here for you to see the result. 

<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/gui4.JPG?raw=true) </center>

Optinally, if you choose to evaluate the quality of the result by Jacarrd socre, then the GUI would proceed to evaluation part.

<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/gui5.JPG?raw=true) </center>
<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/gui6.JPG?raw=true) </center>

After all the procedure, this tool would show the image like this.
<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/gui7.JPG?raw=true) </center>

The whole procedure are done now! 

* You could check result file in the output directory you choosed.

<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/folder1.JPG?raw=true) </center>

```
File: "ANNO_xxx.jpg" is the bounded by yourself.
File: "RESU_xxx.jpg" is the image we propageted your bounding-box.
```

* And you could also check the folder **"EVALUATION"**, if you choosed with the ground-truth folder. 

<center>![GUI](https://github.com/zwm0426/bboxTool/blob/master/GUI_snap/folder2.JPG?raw=true) </center>
The green box is the ground truth, and the red box is our result.

**Thank you for using our tool.**

##Credits

[1] S. Manen, M. Guillaumin, and L. Van Gool. Prime Object Proposals with Randomized Prim's Algorithm. In ICCV, 2013.

[2] P. F. Felzenszwalb and D. P. Huttenlocher Efficient graph-based image segmentation. In IJCV, 2004 http://people.cs.uchicago.edu/~pff/segment/

[3] Zhang, Jianming, et al. "Minimum barrier salient object detection at 80 fps." Proceedings of the IEEE International Conference on Computer Vision. 2015.

