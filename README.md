# V4RL Wide-baseline Place Recognition Dataset
This dataset provides synthetic and real outdoors sequences especially recorded for place recognition applications using both flying and hand-held setups. This dataset was made publicly available with the paper "Real-time Wide-baseline Place Recognition using Depth Completion", by Fabiola Maffra, Lucas Teixeira, Zetao Chen and Margarita Chli, published at IEEE Robotics and Automation Letters (RA-L) 2019 [[paper](https://doi.org/10.1109/lra.2019.2895826)].

#### Video:

<p align="center">
  <a href="https://youtu.be/iwxbxAsCJbM" target="_blank"><img src="https://i.imgur.com/mkeW2ML.png" 
alt="intro" width="480" height="270" border="10" /></a>
</p>




If you use this dataset, please cite the following publication:
 
```
@article{maffra2019real,
  title={Real-time Wide-baseline Place Recognition using Depth Completion},
  author={Maffra, Fabiola and Teixeira, Lucas and Chen, Zetao and Chli, Margarita},
  journal={IEEE Robotics and Automation Letters},
  year={2019},
  publisher={IEEE}
}
```

## L'Agout dataset

The L'Agout synthetic dataset was produced using aerial pictures of “Maisons sur l’Agout” visible in Fig. 5, depicting medieval houses with balconies over the river Agout. We produce 4 sequences of 100 meters with a laterally moving drone carrying a camera facing the houses at 0° (i.e. pointing forwards), 15° from the horizon, 30°, and 45° as shown in Fig. 6b. It is important to highlight that the position of the drone was chosen in a way that the camera frustum is completely filled by the buildings in order to guarantee that the only difference between these sequences happens in the viewpoint, without any changes in scale. By combining sequences at different angles, large changes in viewpoint can be simulated and a very challenging place recognition dataset is created. 


### Examples
<p float="left">
  <img src="https://i.imgur.com/jNGEKl5.png" width="200" />
  <img src="https://i.imgur.com/Zj2vLgd.png" width="200" /> 
  <img src="https://i.imgur.com/MkOKLyp.png" width="200" />
  <img src="https://i.imgur.com/L2R4i0D.png" width="200" />
</p>

### Data

**L'Agout Sequence 0°**  - [Bagfile](https://drive.google.com/open?id=1CwrioiK002Kdoheffrvw_xmz9QSAH_9G) - [Youtube](https://youtu.be/PCw3__0jq3c)

**L'Agout Sequence 15°** - [Bagfile](https://drive.google.com/open?id=1X3ebJEhJfKCKzflNB0GRF2xq8aO7l-9v) - [Youtube](https://youtu.be/1UdyCCpisGE)
 
**L'Agout Sequence 30°** - [Bagfile](https://drive.google.com/open?id=15oJRK8YYL75HlceV-1yU2ZZjs792rA0p) - [Youtube](https://youtu.be/pWrMnvU9B1Y)

**L'Agout Sequence 45°** - [Bagfile](https://drive.google.com/open?id=1XDvnIFYVhES_ahPY-yKdyrhBszdjJMW_) - [Youtube](https://youtu.be/Fy3zjycD6yY)

### Ground truth

The ground truth for each dataset was automatically annotated using 2 different sequences, a query sequence and a reference sequence. The sequences used as reference and query for the available ground truth are:

* L'Agout Sequence 0° & Sequence 15°:

  - Reference Dataset: L'Agout Sequence 0°
  - Query Dataset    : L'Agout Sequence 15°

* L'Agout Sequence 0° & Sequence 30°:

  - Reference Dataset: L'Agout Sequence 0°
  - Query Dataset    : L'Agout Sequence 30°

* L'Agout Sequence 0° & Sequence 45°:

  - Reference Dataset: L'Agout Sequence 0°
  - Query Dataset    : L'Agout Sequence 45°

More details about the ground truth are available on the links below.

**L'Agout Sequence 0° & Sequence 15°** - [Ground truth](https://drive.google.com/open?id=1kfb6PkQaVrCj5_oV3MhQIRMXc1ml8eAb)

**L'Agout Sequence 0° & Sequence 30°** - [Ground truth](https://drive.google.com/open?id=1C9nANtWhlPUVeNZgarYD-8z7OMg06BKJ)

**L'Agout Sequence 0° & Sequence 45°** - [Ground truth](https://drive.google.com/open?id=1UgwiexS9Y7fKAk8OW0OMUD_t-YNpC_eq)

### Calibration

The visual-inertial data reproduces the Skybotix VI-Sensor with the same resolution of the real datasets. Below are the calibration parameters used in the data generation. Note that T_SC is the transformation from the Camera to the Sensor (IMU).

```python

- {T_SC:     
    [1.0, 0.0, 0.0, 0.0,        
     0.0, 1.0, 0.0, 0.0,         
     0.0, 0.0, 1.0, 0.0,
     0.0, 0.0, 0.0, 1.0],
    image_dimension: [752, 480],
    distortion_coefficients: [0.0, 0.0, -0.0, 0.0],
    focal_length: [455.0, 455.0],
    principal_point: [376.5, 240.5]}

```

                                           
## Corvin dataset

The Corvin dataset was produced using aerial footage of the Corvin Castle visible in Figs. 4 and 6. We produced 3 sequences at 0° , 30° , and 45° , while doing a300-meter circular flight around the castle. These sequences capture a scene composed of a large range of different depths.

### Examples
<p float="left">
  <img src="https://i.imgur.com/86Bdwkp.png" width="200" />
  <img src="https://i.imgur.com/OtNZQCJ.png" width="200" /> 
  <img src="https://i.imgur.com/Cq8CzV3.png" width="200" />
</p>

### Data

**Corvin Sequence 0°**  - [Bagfile](https://drive.google.com/open?id=1EndghfpOmZ0M8qPtQRmv8amF8adPE1PG) - [Youtube](https://youtu.be/vAM2o0gxN3A)

**Corvin Sequence 30°** - [Bagfile](https://drive.google.com/open?id=1PaS5hv9UQVg5HAtcINDZw1kcR6PgC16x) - [Youtube](https://youtu.be/NMs-4A3hOTQ)
 
**Corvin Sequence 45°** - [Bagfile](https://drive.google.com/open?id=1fN_pegIMfqPn8-jJ21w7e9P9LX41r7nC) - [Youtube](https://youtu.be/0xjogG1ehlQ)

### Ground truth

The ground truth for each dataset was automatically annotated using 2 different sequences, a query sequence and a reference sequence. The sequences used as reference and query for the available ground truth are:

* Corvin Sequence 0° & Sequence 30°:

  - Reference Dataset: Corvin Sequence 0°
  - Query Dataset    : Corvin Sequence 30°

* Corvin Sequence 0° & Sequence 45°:

  - Reference Dataset: Corvin Sequence 0°
  - Query Dataset    : Corvin Sequence 45°

More details about the ground truth are available on the links below.

**Corvin Sequence 0° & Sequence 30°** - [Ground truth](https://drive.google.com/open?id=1BU_z95cR-nJLYLjnDrBS1kfxsrHiRtYt)

**Corvin Sequence 0° & Sequence 45°** - [Ground truth](https://drive.google.com/open?id=1Y1UWsbKZstzjsfwHjWVV9f2yHzfFpvQc)

### Calibration

The visual-inertial data reproduces the Skybotix VI-Sensor with the same resolution of the real datasets. Below are the calibration parameters used in the data generation. Note that T_SC is the transformation from the Camera to the Sensor (IMU).

```python

- {T_SC:     
    [1.0, 0.0, 0.0, 0.0,        
     0.0, 1.0, 0.0, 0.0,         
     0.0, 0.0, 1.0, 0.0,
     0.0, 0.0, 0.0, 1.0],
    image_dimension: [752, 480],
    distortion_coefficients: [0.0, 0.0, -0.0, 0.0],
    focal_length: [455.0, 455.0],
    principal_point: [376.5, 240.5]}

```


## Old City dataset

Two sequences were recorded at the end of the day in the old city of Zurich, exhibiting not only small, but also challenging viewpoint variations due to the presence of narrow passages in this area, providing wide range of viewpoints of the same places. This dataset comprises two traverses along the same route, each one covering a distance of approximately 230 meters. In total, 10 minutes of data were recorded for this dataset.

### Examples
<p float="left">
  <img src="https://i.imgur.com/kbFZAfE.png" width="200" />
  <img src="https://i.imgur.com/19ms6dI.png" width="200" /> 
  <img src="https://i.imgur.com/FFmhIqq.png" width="200" />
  <img src="https://i.imgur.com/3D3V8ry.png" width="200" />
</p>

### Data

**Old City Sequence 1** - [Bagfile](https://drive.google.com/open?id=1PUcothCjJdJSoHfOivhGWwI34wIuY71W) - [Youtube](https://youtu.be/thEHGiFyZtY)

**Old City Sequence 2** - [Bagfile](https://drive.google.com/open?id=1oRpmfjGQD59rvQnhrN0E2hc-5ZRRzamU) - [Youtube](https://youtu.be/YTIQgcEUXrg)

### Ground truth

The ground truth for each dataset was automatically annotated using 2 different sequences, a query sequence and a reference sequence. The sequences used as reference and query for the available ground truth are:

* Old City Sequence 1 & 2:

  - Reference Dataset: Old City Sequence 1
  - Query Dataset    : Old City Sequence 2

More details about the ground truth are available on the link below.

**Old City Sequence 1 & 2** - [Ground truth](https://drive.google.com/open?id=1cC9vanAzaL2FVPyu1zPpz55nKM1DPLWy)

### Calibration

The images were captured using a [VI-Sensor](http://wiki.ros.org/vi_sensor) and calibrated using [ETHZ ASL Kalibr](https://github.com/ethz-asl/kalibr). Below are the calibration parameters. Note that T_SC is the transformation from the Camera to the Sensor (IMU). The set of values correspond to camera0's intrinsics.

```python

- {T_SC:     
    [0.9997754002442455, -0.021161371053313276, -0.0011599317232830833, -0.03742703361193287,
     0.021167568626536626, 0.999760145165724, 0.00562015806284527, 0.0059817697251900205,
     0.0010407232579056848, -0.005643448711071745, 0.9999835340553093, 0.0005720705107382817,
     0.0, 0.0, 0.0, 1.0],
    image_dimension: [752, 480],
    distortion_coefficients: [0.00953484510402244, -0.017544574626951994, 0.0196682925507835, -0.006035463565306639],
    distortion_type: equidistant,
    focal_length: [470.9855284431703, 470.85690553639535],
    principal_point: [376.3839029041999, 247.67863814640694]}

```


## Clausius Street dataset (Air-Ground)

Clausius Street dataset consists of both an air-sequence and a hand-held sequence recorded on the same day along a residential street with the camera facing the buildings of one street side. These combined sequences present extreme viewpoint changes with images captured from a very wide baseline (air to ground).

### Examples

<p float="left">
  <img src="https://i.imgur.com/vrTF94V.png" width="200" />
  <img src="https://i.imgur.com/th8cFpr.png" width="200" /> 
  <img src="https://i.imgur.com/dQEYvfX.png" width="200" />
  <img src="https://i.imgur.com/9BKY6Mn.png" width="200" />
</p>

### Data

**Clausius Street Air Sequence**    - [Bagfile](https://drive.google.com/open?id=1E4rBqWzBeQ0c2ofsKib7lccI3sCDPkA8) - [Youtube](https://youtu.be/xe8gySTZfsw)

**Clausius Street Ground Sequence** - [Bagfile](https://drive.google.com/open?id=1aoQS3b9kgfIHvG3R_5wTBbgVMwtSj1Sb) - [Youtube](https://youtu.be/os2BbCOjha4)

### Calibration

The images were captured using a [VI-Sensor](http://wiki.ros.org/vi_sensor) and calibrated using [ETHZ ASL Kalibr](https://github.com/ethz-asl/kalibr). Below are the calibration parameters. Note that T_SC is the transformation from the Camera to the Sensor (IMU). The set of values correspond to camera0's intrinsics.

```python

- {T_SC:     
    [ 0.9999921569165363, 0.003945890103835121, 0.0003406709575200133, -0.030976405894694664,        
     -0.003948017768440125, 0.9999711543561547, 0.0064887295612456805, 0.003944069243840622,         
     -0.00031505731688472255, -0.0064900236445916415, 0.9999788899431723, -0.016723945219020563,
     0.0, 0.0, 0.0, 1.0],
    image_dimension: [752, 480],
    distortion_coefficients: [0.0038403216668672986, 0.025065957244781098, -0.05227986912373674, 0.03635919730588422],
    distortion_type: equidistant,
    focal_length: [464.2604856754006, 463.0164764480498],
    principal_point: [372.2582270417875, 235.05442086962864]}

```

### Contact

For any questions or bug reports, please create an issue or contact me at fmaffra@mavt.ethz.ch.
