<img height='175' src="https://user-images.githubusercontent.com/37406965/51083189-d5dc3a80-173b-11e9-8ca0-28015e0893ac.png" align="left" hspace="1" vspace="1">

# PPI-Vision :iphone:

Vision PPI is a computer vision and machine learning based app to help in filling out the PPI Survey. There are two broad aspects to this project - The android app which provides the interface to the field officer for conducting the survey and the machine learning models which will be used to analyze the images captured. 

For more information about the usecases of the project and details about PPI, the API used and demo credentials, please take a look at the [project wiki](https://github.com/openMF/ppi-vision/wiki). 

## Screenshots :camera:

| <img src="https://user-images.githubusercontent.com/41234408/91012906-80992800-e604-11ea-960f-7956ed1c6b30.png" width="250" />  | <img src="https://user-images.githubusercontent.com/41234408/91012933-8ee74400-e604-11ea-8dca-4056855e25d5.png" width="250" />   | <img src="https://user-images.githubusercontent.com/41234408/91012972-a1fa1400-e604-11ea-92d2-5ba6ef186fa4.png" width="250" />  |
|---|---|---|
| <img src="https://user-images.githubusercontent.com/41234408/91013027-b2aa8a00-e604-11ea-8d46-41b63ecff38b.png" width="250" />  | <img src="https://user-images.githubusercontent.com/41234408/91013053-bccc8880-e604-11ea-8670-9fe584d11b61.png" width="250" />   | <img src="https://user-images.githubusercontent.com/41234408/91013076-c9e97780-e604-11ea-8c47-c965e401c1ab.png" width="250" />  |
| <img src="https://user-images.githubusercontent.com/41234408/91013128-db328400-e604-11ea-8ba8-3d6603424b7b.png" width="250" />  | <img src="https://user-images.githubusercontent.com/41234408/91013158-e5548280-e604-11ea-8049-a3fc2a391af8.png" width="250" />   | <img src="https://user-images.githubusercontent.com/41234408/91013194-ef768100-e604-11ea-9c6c-c76c520b85bd.png" width="250" />  |

## Contributions :information_desk_person:

We welcome contributions in form of issues, as well as pull requests. Please go though the contribution guidelines over [here](https://github.com/openMF/ppi-vision/blob/master/CONTRIBUTING.md) and also through our Code of Conduct [here](https://github.com/openMF/ppi-vision/blob/master/CODE_OF_CONDUCT.md).

## Development Setup :triangular_ruler:

Before you begin, you should have already downloaded the Android Studio SDK and set it up correctly. You can find a guide on how to do this here: [Setting up Android Studio](http://developer.android.com/sdk/installing/index.html?pkg=studio)

### Setting up the Android Project :black_nib:

1. Download the project source. You can do this either by forking and cloning the repository (recommended if you plan on pushing changes) or by downloading it as a ZIP file and extracting it.

2. Install the NDK in Android Studio.

3. Open Android Studio, you will see a **Welcome to Android** window. Under Quick Start, select *Import Project (Eclipse ADT, Gradle, etc.)*

4. Navigate to the directory where you saved the ppi-vision project, select the root folder of the project (the folder named "vision-ppi"), and hit OK. Android Studio should now begin building the project with Gradle.

5. Once this process is complete and Android Studio opens, check the Console for any build errors.

    - *Note:* If you receive a Gradle sync error titled, "failed to find ...", you should click on the link below the error message (if available) that says *Install missing platform(s) and sync project* and allow Android studio to fetch you what is missing.

6. To Build the app, go to *Build > Make Project* (or alternatively press the Make Project icon in the toolbar).

7. If the app was built successfully, you can test it by running it on either a real device or an emulated one by going to *Run > Run 'app'* or pressing the Run icon in the toolbar.

### Image Labelling :framed_picture:

#### Data Collection 

For data collection, [this](https://github.com/hardikvasa/google-images-download) tool can be used. In order to increase the size of the dataset, we have used image augmentation techniques present in [GeneratedImages.py](https://github.com/openMF/ppi-vision/blob/master/DataCollection/GenerateImages.py). You can see how each technique works [here](https://github.com/openMF/ppi-vision/blob/master/DataCollection/ImageAugmentation.ipynb) in the sample notebook. 

#### Model Training

We use [Google's MLKit SDK](https://developers.google.com/ml-kit) for image labelling. In order to train the model used further, we use transfer learning on our collected data. 

**Useful Resources for getting started with MLKIt if you are interested in contributing to this project:**

- [Label images with ML Kit on Android](https://developers.google.com/ml-kit/vision/image-labeling/android)
- [MLKIt Quickstart Sample](https://github.com/googlesamples/mlkit/tree/master/android/vision-quickstart)
- [MLKit Custom Models](https://developers.google.com/ml-kit/custom-models)
- [Labelling images with a custom model on Android](https://developers.google.com/ml-kit/vision/image-labeling/custom-models/android)
- [Converting an existing TensorFlow object detection model into a TensorFlow Lite model](https://www.tensorflow.org/lite/convert)

### License :page_with_curl:

This project adhers to the [MIT License](https://github.com/openMF/ppi-vision/blob/master/LICENSE).
