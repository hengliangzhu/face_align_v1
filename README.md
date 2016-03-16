# face_align_v1
Face alignment tool v1
2016.3
------------------------------------------------------

The provided tool is a quick implementation of the paper [1]. And this tool is implemented based on Caffe [2]. The example images in the folder "data" are selected from AFLW [3].

References:

[1] Shao Z, Ding S, Zhu H, et al. Face alignment by deep convolutional network with adaptive learning rate[C]//Acoustics, Speech and Signal Processing (ICASSP), 2016 IEEE International Conference on. IEEE, 2016.

[2] Jia Y, Shelhamer E, Donahue J, et al. Caffe: Convolutional architecture for fast feature embedding[C]//Proceedings of the ACM International Conference on Multimedia. ACM, 2014: 675-678.

[3] Kostinger M, Wohlhart P, Roth P M, et al. Annotated facial landmarks in the wild: A large-scale, real-world database for facial landmark localization[C]//Computer Vision Workshops (ICCV Workshops), 2011 IEEE International Conference on. IEEE, 2011: 2144-2151.
------------------------------------------------------

Prerequisites:
1. The provided tool is compiled on Windows 8.1, 64 bit. But we have tested this tool successfully on Windows 7 and Windows 10.  

2. If you haven't installed Visual Studio 2013 or Visual C++ Redistributable for Visual Studio 2013, then please download and install the Visual C++ Redistributable for Visual Studio 2013 from: https://www.visualstudio.com/downloads/download-visual-studio-vs
------------------------------------------------------

Usuage:

face_align_icassp.exe modelPath imagePath listfile outputFile
rd /s/q modelPath\\input_data

Input:
- "listfile " is a file that contains the images and corresponding face bounding box for each image. 
- "imagePath " is the path to a directory containing the image files.
- "modelPath " is the path to a directory containing the model file.

Output:
- "outputFile" is a file that will be generated by this tool and contains the predicted facial landmark locations.

The demand of "rd /s/q modelPath\\input_data" is used for deleting a temp file at each run. If you remove this demand, the running results will be wrong.  
------------------------------------------------------

Format:

Format of the listfile:
This file starts with the number of the images to be tested.
Then each of the following line contains the image name, followed by the left, right, top and bottom of the face bounding box.
We suggest you use the face detector provided in http://mmlab.ie.cuhk.edu.hk/archive/CNN_FacePoint.htm to generate the face bounding box.

Format of the outputFile:
5 facial landmark locations (x1,y1,x2,y2...).
------------------------------------------------------

Example:
Run run.bat

Should you have any questions, then just contact with us through email, shaozhiwen@sjtu.edu.cn.