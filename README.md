<a name="readme-top"></a>

<div align="center">
  <h3 align="center">License Plate Recognition</h3>
</div>

<!-- ABOUT THE PROJECT -->

### About The Project

The goal of the project is to develop a license plate recognition system to identify and capture Japanese vehicle plate numbers.

#### Use Cases
##### Crime Prevention
The rise in vehicles on the road makes identifying criminal activity increasingly challenging. License plate recognition assists law enforcement by enabling quick identification of stolen or suspicious vehicles. 

##### Smart Garage Opener
License plate recognition can be used to automate opening the garage door when it detects your car is heading toward the garage, essentially a virtual key to your garage.

#### Approach
The proposed approach is using a Convolutional Neural Network model (CNN). CNN models excel in processing spatial data, such as images, especially when much noise or additional entities obscure the key features. In the dataset, many of images consists of features (text) shifted in different angles, different lighting, and different image quality. CNN is a great option to extract these features by training on the dataset through many of its layers.

#### Important Layers

##### Layer 2 - First Convolutional Layer (32 filter)

The purpose of this layer is to detect features from edges and shapes.

##### Layer 3 - First Max Pooling Layer

The purpose of this layer is to reduce the spatial size which helps the model focus closer to the features (text).

##### Layer 4 - Second Convolutional Layer (64 filter)

The purpose of this layer is to allow the model to better detect complex patterns.

##### Layer 5 - Second Max Pooling Layer

The purpose of this layer is to again reduce spatially and the main benefit of this is to help detect the text invariance.


### Dataset 

The data set is sourced from [Kaggle](https://www.kaggle.com/datasets/nickyazdani/license-plate-text-recognition-dataset).

Characteristics of the dataset:
- cropped images of Japanese license plates
- license plate photos are captured in various angles and lighting
- license plate exist various styles and color

**Note** - Notebook consists of borrowed code from [published CNN Model](https://keras.io/examples/vision/captcha_ocr/) and adjusted to fit application.