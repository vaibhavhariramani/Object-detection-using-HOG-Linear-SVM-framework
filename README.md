# object_detector
Object Detector using HOG as descriptor and Linear SVM as classifier


## Prerequisites
Install [OpenCV 3](https://github.com/opencv/opencv) with Python 3 bindings


## Dependencies
You can install all dependencies by running
```shell
pip install -r requirements.txt
```


## Run the code
To test the code, run the lines below in your terminal

```shell
git clone https://github.com/vladkha/object_detector.git
cd object_detector/bin
python test_object_detector.py
```

_The `test_object_detector.py` will download the
[CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and [WIDER FACE](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/)
datasets and train a classifier to detect faces in an image.
The SVM model files will be stored in `data/models`,
so that they can be reused later on in `test_classifier.py`_


## Configuration File
All the configurations are in the `data/config/config.cfg` configuration files.
You can change it as per your need.
Here is what the default configuration file looks like

```bash
[hog]
window_size: [178, 218]
window_step_size: 20
orientations: 9
pixels_per_cell: [8, 8]
cells_per_block: [3, 3]
visualise: False
normalise: None

[nms]
threshold: 0.4

[paths]
model_path: ../data/models/model_name.model

[general]
pyramid_downscale = 1.5
pos_samples = 1000
neg_samples = 1000
```


## About modules
* `config.py` -- imports the configuration variables from `config.cfg`
* `create_neg_samples_WIDER.py` -- module to create negative samples (images of non-faces from WIDER dataset)
* `extract_features.py` -- module used to extract HOG features of the training images
* `train_classifier.py` -- module used to train the classifier
* `test_classifier.py` -- module used to test the classifier using a test image
* `utils.py` -- module containing helper functions


## Some results
_Detections before NMS_             |  _Detections after NMS_
:-------------------------:|:-------------------------:
![](images/1.png) |  ![](images/2.png)
![](images/3.png) |  ![](images/4.png)
![](images/5.png) |  ![](images/6.png)
![](images/7.png) |  ![](images/8.png)
![](images/9.png) |  ![](images/10.png)
![](images/11.png) |  ![](images/12.png)
![](images/13.png) |  ![](images/14.png)


## Built With
* [OpenCV 3](https://github.com/opencv/opencv) - Computer vision library
* [Scikit-learn](https://github.com/scikit-learn/scikit-learn) - Machine learning library
* [scikit-image](https://github.com/scikit-image/scikit-image) - Image processing library


## TODO
Possible ways to improve the project:
* Make the sliding window computation run in parallel - can dramatically speedup the code
* Split processing of the image pyramid in `test_classifier.py` to different cores of the processor, that way each core can process a separate layer of the pyramid independently
* Add bootstrapping (Hard Negative Mining)


## Acknowledgments
* Credit for base project structure and image processing goes [bikz05](https://github.com/bikz05) for his [object-detector](https://github.com/bikz05/object-detector)
* [Adrian Rosebrock](https://github.com/jrosebr1) for his great blog [www.pyimagesearch.com](https://www.pyimagesearch.com/) and particular series of articles regarding object detection topic:
    - [Histogram of Oriented Gradients and Object Detection](https://www.pyimagesearch.com/2014/11/10/histogram-oriented-gradients-object-detection/)
    - [Non-Maximum Suppression for Object Detection in Python](https://www.pyimagesearch.com/2014/11/17/non-maximum-suppression-object-detection-python/)
    - [(Faster) Non-Maximum Suppression in Python](https://www.pyimagesearch.com/2015/02/16/faster-non-maximum-suppression-python/)
    - [Intersection over Union (IoU) for object detection](https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection/)
    - [Image Pyramids with Python and OpenCV](https://www.pyimagesearch.com/2015/03/16/image-pyramids-with-python-and-opencv/)
    - [Sliding Windows for Object Detection with Python and OpenCV](https://www.pyimagesearch.com/2015/03/23/sliding-windows-for-object-detection-with-python-and-opencv/)
    - [Pedestrian Detection OpenCV](https://www.pyimagesearch.com/2015/11/09/pedestrian-detection-opencv/)
    - [HOG detectMultiScale parameters explained](https://www.pyimagesearch.com/2015/11/16/hog-detectmultiscale-parameters-explained/)
# Resources 

[https://sites.google.com/view/geeky-traveller/computer-vision/histogram-of-oriented-gradients-and-object-detection](https://sites.google.com/view/geeky-traveller/computer-vision/histogram-of-oriented-gradients-and-object-detection}



## To learn more about these Resources you can Refer to some of these articles written by Me:-

- [Medium](https://medium.com/geeky-bawa)
- [geeky Traveller](https://sites.google.com/view/geeky-traveller/)
- [Blogs](https://github.com/vaibhavhariaramani/blogs)
- [Youtube](https://www.youtube.com/channel/UCy7amUpLnsRLEMIaJGGBYog)[![Youtube Badge](https://img.shields.io/badge/-Geeky_Bawa-1ca0f1?style=flat-circle&labelColor=d54b3d&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UCy7amUpLnsRLEMIaJGGBYog)](https://www.youtube.com/channel/UCy7amUpLnsRLEMIaJGGBYog)

### Don't forget to tag us

if you use this repo in  your project don't forget to mention us as Contributer in it . And Don't forget to tag us [Linkedin](https://www.linkedin.com/in/vaibhav-hariramani-087488186/),[ instagram](https://www.instagram.com/geeky_baba_/?hl=en),[ facebook](https://www.facebook.com/jayesh.hariramani.3) ,[ twitter](https://www.linkedin.com/in/vaibhav-hariramani-087488186/), [ Github](https://github.com/vaibhavhariaramani) 

============================================================================
# Made with ❤️by Vaibhav Hariramani
#### About me

I am a Machine Learning enthusiast, an Actions on Google, Internet of things, Alexa Skills, and Image processing developer.
I have a keen interest in Image processing and Andriod development.
I am Currently studying at  Chandigarh University, Punjab.

[My PortFolio](https://vaibhavhariaramani.github.io/)
You can find me at:-
[Linkedin](https://www.linkedin.com/in/vaibhav-hariramani-087488186/) or [Github](https://github.com/vaibhavhariaramani) .

Email: [vaibhav.hariramani01@gmail.com](mailto:vaibhav.hariramani01@gmail.com)


# Download [THE VAIBHAV HARIRAMANI APP](https://github.com/vaibhavhariaramani/The-Vaibhav-Hariramani-App/raw/master/vaibhav%20hariramani%20app.apk)

# [<img src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/gh-bannner-light.png">](https://github.com/vaibhavhariaramani/The-Vaibhav-Hariramani-App/raw/master/vaibhav%20hariramani%20app.apk) 
<p align='center'>
<a href="https://www.linkedin.com/in/vaibhav-hariramani-087488186/"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/linkedin.png"></a>&nbsp;&nbsp;
<a href="https://twitter.com/vaibhavhariram2"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/twitter.png"></a>&nbsp;&nbsp;
<a href="https://www.instagram.com/vaibhav.hariramani/?hl=en"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/instagram.jpg"></a>&nbsp;&nbsp;
<a href="https://www.buymeacoffee.com/vaibhavJii"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/by-me-a-coffee.png"></a>
<a href="https://wa.me/+917790991077"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/whatsapp.png"></a>&nbsp;&nbsp;
<a href="mailto:vaibhav.hariramani01@gmail.com"><img height="30" src="https://github.com/vaibhavhariaramani/vaibhavhariaramani/blob/master/icon/email.png"></a>&nbsp;&nbsp;
</p>


[<img width="150" align='center' src="https://archive.org/download/download-button-png/download-button-png.png">The Vaibhav Hariramani App (Latest Version) ](https://github.com/vaibhavhariaramani/The-Vaibhav-Hariramani-App/raw/master/vaibhav%20hariramani%20app.apk)

Download [THE VAIBHAV HARIRAMANI APP](https://github.com/vaibhavhariaramani/The-Vaibhav-Hariramani-App/raw/master/vaibhav%20hariramani%20app.apk) consist of Tutorials,Projects,Blogs and Vlogs of our Site developed Using Android Studio with Web View try installing it in your android device.

Happy coding ❤️ .

### Follow me
  
[![Linkedin Badge](https://img.shields.io/badge/-VaibhavHariramani-blue?style=flat-circle&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/vaibhav-hariramani-087488186/)](https://www.linkedin.com/in/vaibhav-hariramani-087488186/) [![Instagram Badge](https://img.shields.io/badge/-VaibhavHariramani-e02c73?style=flat-circle&labelColor=e02c73&logo=Instagram&logoColor=white&link=https://www.instagram.com/vaibhav.hariramani/?hl=en)](https://www.instagram.com/vaibhav.hariramani/?hl=en) [![Twitter Badge](https://img.shields.io/badge/-VaibhavHariramani-1ca0f1?style=flat-circle&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/vaibhavhariram2)](https://twitter.com/vaibhavhariram2) [![GitHub Badge](https://img.shields.io/badge/-@Vaibhavhariaramani-24292e?style=flat-circle&labelColor=24292e&logo=github&logoColor=white&link=https://github.com/vaibhavhariaramani)](https://github.com/vaibhavhariaramani) [![Gmail Badge](https://img.shields.io/badge/-VaibhavHariramani-d54b3d?style=flat-circle&labelColor=d54b3d&logo=gmail&logoColor=white&link=mailto:vaibhav.hariramani01@gmail.com)](mailto:vaibhav.hariramani01@gmail.com) [![Medium Badge](https://img.shields.io/badge/-VaibhavHariramani-d54b3d?style=flat-circle&labelColor=d54b3d&logo=medium&logoColor=white&link=https://medium.com/geeky-bawa)](https://medium.com/geeky-bawa) 



## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details
