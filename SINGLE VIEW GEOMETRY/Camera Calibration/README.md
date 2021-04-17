# Camera Calibration: MATLAB Camera Calibrator

> For the calibration I designed a Checkerboard pattern myself using Adobe Photoshop, which has 30mmx30mm squares. You can download it from [here](https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/SINGLE%20VIEW%20GEOMETRY/Camera%20Calibration/checkboard-30mm.pdf). Later I found that out there are checkerboard pattrens readily available on the internet😅. Here is the [link](https://markhedleyjones.com/projects/calibration-checkerboard-collection). Don't waste your time on designning the checkeboard.

<p align="center">
  <img src="https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/SINGLE%20VIEW%20GEOMETRY/Camera%20Calibration/cc.png" />
</p>


```
 Standard Errors of Estimated Camera Parameters of a Huawei Y5-2017 Phone's Back Camera
---------------------------------------------------------------------------------------			

Intrinsics
----------
Focal length (pixels):   [ 2625.0714 +/- 6.0435     2656.0118 +/- 5.7201  ]
Principal point (pixels):[ 1176.5715 +/- 4.3481     1342.5772 +/- 3.5103  ]
Radial distortion:       [    0.0567 +/- 0.0096       -0.2138 +/- 0.0359  ]

Extrinsics
----------
Rotation vectors:
     [    0.1700 +/- 0.0069        0.0621 +/- 0.0067        1.5079 +/- 0.0009  ]
     [   -0.2104 +/- 0.0041        0.4402 +/- 0.0040        1.5229 +/- 0.0010  ]
     [    0.2477 +/- 0.0036        0.7418 +/- 0.0034        1.5615 +/- 0.0011  ]
     [   -0.5428 +/- 0.0036       -0.0571 +/- 0.0037        1.3857 +/- 0.0010  ]
     [    0.5814 +/- 0.0028       -0.3401 +/- 0.0026        1.4464 +/- 0.0010  ]
     [    0.7025 +/- 0.0025        0.5467 +/- 0.0021        1.4362 +/- 0.0008  ]
     [   -0.3633 +/- 0.0022       -0.5122 +/- 0.0022        1.4601 +/- 0.0009  ]
     [    0.4561 +/- 0.0033       -0.2956 +/- 0.0031        1.5067 +/- 0.0009  ]
     [   -0.0094 +/- 0.0031       -0.4297 +/- 0.0029        0.0108 +/- 0.0008  ]
     [    0.0625 +/- 0.0025        0.7340 +/- 0.0025       -0.0321 +/- 0.0009  ]
     [   -0.1133 +/- 0.0046        0.4269 +/- 0.0045        1.5722 +/- 0.0010  ]
     [   -0.3884 +/- 0.0027       -0.3917 +/- 0.0028        1.4266 +/- 0.0009  ]
     [    0.7873 +/- 0.0026        0.5271 +/- 0.0022        1.4277 +/- 0.0009  ]
     [    0.0241 +/- 0.0029       -0.5952 +/- 0.0027        1.5897 +/- 0.0011  ]
     [    0.1689 +/- 0.0053       -0.0489 +/- 0.0052        1.5443 +/- 0.0008  ]
     [   -0.2664 +/- 0.0029        0.4326 +/- 0.0026        1.5205 +/- 0.0009  ]
     [    0.0740 +/- 0.0024        0.7686 +/- 0.0024        0.0473 +/- 0.0009  ]
     [    0.4414 +/- 0.0024       -0.4594 +/- 0.0024        0.0729 +/- 0.0008  ]
     [    0.3170 +/- 0.0018        0.7216 +/- 0.0020       -0.1555 +/- 0.0008  ]
     [   -0.8950 +/- 0.0022        0.1068 +/- 0.0023       -0.0458 +/- 0.0011  ]

Translation vectors (millimeters):
     [  156.5352 +/- 0.8558     -142.1361 +/- 0.6828      489.9408 +/- 1.4992  ]
     [  177.0393 +/- 1.0356     -159.7594 +/- 0.8358      618.5397 +/- 1.4334  ]
     [  182.8178 +/- 0.8520     -127.2946 +/- 0.6655      497.3671 +/- 1.2524  ]
     [   85.2089 +/- 1.0808     -140.5887 +/- 0.8680      654.7028 +/- 1.3501  ]
     [  120.0734 +/- 0.6349      -82.2827 +/- 0.5392      372.7998 +/- 1.1307  ]
     [   83.4689 +/- 0.4883     -130.2688 +/- 0.3824      283.5182 +/- 0.8167  ]
     [  123.6431 +/- 0.6778     -145.7546 +/- 0.5431      419.2150 +/- 0.9115  ]
     [  123.3105 +/- 0.6102     -126.9356 +/- 0.5381      357.5151 +/- 1.0769  ]
     [ -103.6184 +/- 0.6891     -111.1653 +/- 0.5341      395.9376 +/- 1.0893  ]
     [  -66.8696 +/- 0.8675      -98.7360 +/- 0.6800      519.7027 +/- 1.0167  ]
     [  153.3927 +/- 0.9997     -149.8585 +/- 0.8024      598.3399 +/- 1.4108  ]
     [  108.0664 +/- 0.8176     -171.9490 +/- 0.6520      499.9306 +/- 1.0847  ]
     [   77.1138 +/- 0.5383     -150.5135 +/- 0.4301      313.9741 +/- 0.9169  ]
     [  164.4851 +/- 0.7784     -100.0033 +/- 0.6455      471.4640 +/- 1.2113  ]
     [  123.4742 +/- 0.7564     -130.8235 +/- 0.6274      440.0215 +/- 1.2997  ]
     [  121.6460 +/- 0.8347     -200.8470 +/- 0.6852      502.4894 +/- 1.1208  ]
     [  -56.8049 +/- 0.8715     -114.2302 +/- 0.6826      521.4934 +/- 1.0168  ]
     [  -51.6614 +/- 0.5961     -118.0420 +/- 0.5028      344.1645 +/- 1.0668  ]
     [ -126.1515 +/- 0.6692      -75.4279 +/- 0.5473      414.5757 +/- 0.8322  ]
     [ -112.0351 +/- 0.9179      -33.6990 +/- 0.7649      566.4666 +/- 1.1665  ]
```

<p align="center">
  <img src="https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/SINGLE%20VIEW%20GEOMETRY/Camera%20Calibration/showExtrinsics.png" width="700px"/>
</p>

<p align="center">
  <img src="https://github.com/bimalka98/Computer-Vision-and-Image-Processing/blob/main/SINGLE%20VIEW%20GEOMETRY/Camera%20Calibration/showReprojectionErrors.png" width="700px" />
</p>


## Converting Focal Length from Pixels to Millimeters: (Have to be done)

1. To convert a known focal length in pixels to mm:

F(mm) = F(pixels) * SensorWidth(mm) / ImageWidth (pixel).

For an X4S, the image width in pixels is 5472. Context Capture indicates the sensor width is 13.2 mm, so the equation is simply:

F(mm) = F(pixels) * 13.2 / 5472;

2. can find the focal length(mm) by multiplying the size of the pixel on the sensor by the focal length(pixel)
