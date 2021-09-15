Self Supervised Learning

# Obj：

- Resource Sharing (videos & papers)

- Course project & Research

  

## general practice of traffic light detection:

- 3-STEP [info](https://zhuanlan.zhihu.com/p/25623678)

1. **Detection** to identify regions of interest in an image where a traffic sign is likely to be found
2. **Tracking** of the detected region of interest
3. **Classification** of the traffic sign based on internal datasets and neural network algorithms.

After the classification is done, the system informs the driver by displaying a symbol representing th



# self-supervised Lidar Points denoising 

- 什么是点云：根据激光测量原理得到的点云，包括三维坐标（XYZ）和激光反射强度（Intensity），强度信息与目标的表面材质、粗糙度、入射角方向以及仪器的发射能量、激光波长有关。根据摄影测量原理得到的点云，包括三维坐标（XYZ）和颜色信息（RGB）。结合激光测量和摄影测量原理得到点云，包括三维坐标（XYZ）、激光反射强度（Intensity）和颜色信息（RGB）。

- ### 点云的属性：

  - 空间分辨率、点位精度、表面法向量等。
  - 点云可以表达物体的空间轮廓和具体位置，我们能看到街道、房屋的形状，物体距离摄像机的距离也是可知的；其次，点云本身和视角无关，可以任意旋转，从不同角度和方向观察一个点云，而且不同的点云只要在同一个坐标系下就可以直接融合。

- 点云denoise可以用self-supervised learnnig


# Objective 1：影响traffic sign 的雨水阳光雾气很重要

- Traffic signs are characterized by a wide variability in their visual appearance in real-world environments. For example, changes of illumination, varying weather conditions and partial occlusions impact the perception of road signs. In practice, a large number of different sign classes needs to be recognized with very high accuracy. （Man vs computer,J. Stallkampa,∗ , M. Schlipsing a , J. Salmena , C. Igel )
- bad weather & av里大段描写

# obj 2:A video from CMU: self supervised learning and autonomous driving

- [CMU VIDEO](http://www.ipam.ucla.edu/abstract/?tid=16711&pcode=AVWS1)

- ![image-20210205184447617](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210205184447617.png)

  

- Light Curtain:only trace depth on the curtain profile with control points![image-20210206150522659](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206150522659.png)

- Self supervised scene flow prediction: 

  ![image-20210206145754579](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206145754579.png) 

  Same network&parameters

- ![image-20210206145811903](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206145811903.png)

  ![image-20210206145934714](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206145934714.png)

  In order to make predictions more stable, move predictions towards to nearest neighbor

  ![image-20210206150128705](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206150128705.png)

- Stanford: self supervised learning to generate depth image from camera photos **pseudo-LiDAR ** (self supervised monocular depth estimation)

  ![image-20210206151121104](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206151121104.png)

  ![image-20210206151613864](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206151613864.png)

  ![image-20210206151917024](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206151917024.png)

- derain不一定有利于obj detection:all existing deraining algorithms will deteriorate
  the detection performance compared to directly using
  the rainy images4 (CVPR image derain review , Tianjin U, and also 51th ref in this paper)
  ,

# Obj 3：去雨算法学习一下

- photometric loss

- stereo camera: RGB-D images, generate depth maps

- self supervised learning 结构， 和评价方法

- self supervised learning principles ![image-20210206091157148](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210206091157148.png)

- Transfer Learning

  # Noise2Noise

  - idea behind: *L*2 loss, the network learns to output **the average** of all plausible explanations (e.g., edges shifted by different amounts)
  - When training: noise input + noise target
  - noise are not statistically avaliable (Mente Carlo rendering)
  - Results:![image-20210209215224097](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210209215224097.png)

  

  # Noise2Void

  - Both input and output are noise itself.
  - Assumption: pixel wise independent noise
  - in order to avoid learning identity, the perceptive field of a piexcel exclude the pixel itself.

  ![img](https://pic4.zhimg.com/80/v2-10e163282429b231de0659714f7c2613_1440w.jpg)

![image-20210209215306082](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210209215306082.png)

- implementation:
- ![img](https://pic2.zhimg.com/80/v2-dac296da9ffdaa49f7f0daeca1730ec1_1440w.jpg)

# Noise2Self:Video denoising

- x:data, y:noisy label, z: ground truth
- ![image-20210210102730500](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210210102730500.png)
- [youtube](https://www.youtube.com/watch?v=jwp1MsSXOZ4)
- 

# Self-supervised training for blind multi-frame video denoising



# The Story:

在交通监控现场，交警需要通过监控图像来识别车牌、违章行为、驾驶人等要求，模糊的图像在这种场合根本无法应

- video dataset:Derf [40] and Vid3oC-10 [26] datasets

- outdoor CRVD dataset [61].

- This dataset consists in raw sequences of 50 frames with real noise from a surveillance camera with the sensor IMX385, at fifive ISO levels.

- CVRD dataset: noise-clean pairs

- # VIRAT 做监控录像的

- [交通监控](https://github.com/alnfedorov/traffic-analysis)

- [纽约交通监控](http://www.andrew.cmu.edu/user/shanghaz/)

- UAVDT其实也能用

# rain noise 添加办法

- rain steak: most common, ![image-20210216133721041](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210216133721041.png)
- rain drops:
- ![image-20210216133821550](C:\Users\zonga\AppData\Roaming\Typora\typora-user-images\image-20210216133821550.png)
