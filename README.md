# indoor-action-recognizer
This repository includes a Deep Learning model that performa action classification from a video stream. 

### How to use it
- Firstly, download the Deep Learning model named **indoor_action_recognizer.hdf5** located at the `model` directory. 
- Then, install Tensorflow in your machine, you can follow this [guide](https://www.tensorflow.org/install). Tensoflow 2.2 is recommended.
- Then, load the model with Tensorflow and then you can perform inferences with it. You can also use to apply Transfer Learning from it.
- You can follow the guide in the [Jupyter Notebook File](Indoor Action Recognizer tutorial.ipynb)

### Feed the Deep Learning Network
The network is trained to accept 64 frames with a spatial resolution of 224x244 (x3 channels). Is recommended to sample the video feed at 25 frames per second. The video should also be normalized between -1 and 1. The number -1 refers to the 0 value and 1 refers to 254. 

### Optimized versions for embedded devices (Jetson Nano)
We provide an optimized version of the DL model named `indoor_action_recognizer.engine` in the `model` folder. It was optimized with TensorRT 7 to be able to run it on the low-power execution board Jetson Nano. If you want to optimize it for any other execution board you can do it using the `hdf5` model. 

## License
[BSD 3-Clause License](LICENSE)
