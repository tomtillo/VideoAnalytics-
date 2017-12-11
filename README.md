# VideoAnalytics
Part 1 : Real Time object detection in video Using YOLO9000 on COCO dataset

![](https://github.com/tomtillo/VideoAnalycis-/blob/master/object_detection_1.jpg)
![](https://github.com/tomtillo/VideoAnalycis-/blob/master/object_detection_2.jpg)

## Steps 
1. Install Cython 
Pip install Cython

2. Run the setup.py 
python3 setup.py build_ext --inplace

3. Download tinyYolo weights ( from the origianal darknet website )
https://pjreddie.com/darknet/yolo/

4. Copy the weights to the /bin folder – relative to the base folder 

5. Make sure your cfg files are also present  in the /cfg folder 


## Points to watch out for .
1. Some weights are not compatible with the .cfg files. You might have to get it from the shared google drive ( darkflow yolo weights can be obtained from this location - https://drive.google.com/drive/folders/0B1tW_VtY7onidEwyQ2FtQVplWEU
 )
2. If you are running on windows, system PATH should include location to the cudnn64_6.dll file 
3. For the .dll file , use this version of cuda library - cudnn-8.0-windows7-x64-v6.0 ( from  https://developer.nvidia.com/rdp/cudnn-download )

## Common Errors 
```
'Over-read {}'.format(self.path)
AssertionError: Over-read bin/yolo-voc.weights
```
Cause & Solution : The weights and teh .cfg files donot match . Download the right weights+ .cfg file combination ( either from darknet homepage or from the google drive ( link in the previous section )

Reference 
darkflow project github - https://github.com/thtrieu/darkflow 
darknet project github - https://github.com/pjreddie/darknet
