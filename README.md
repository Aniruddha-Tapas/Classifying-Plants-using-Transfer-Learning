<hr>

## Link to the Publication:

[IJARCET-VOL-5-ISSUE-11-2664-2669.pdf](http://ijarcet.org/wp-content/uploads/IJARCET-VOL-5-ISSUE-11-2664-2669.pdf)


<hr>

# Classifying Plant types using Transfer Learning

We intend to perform image segmentation on the plant phenotyping dataset. The dataset contains images(rgb coloured and masked labels) of 3 different classes of plants(1 and 2 : both consisting of top-view time-lapse images of Arabidopsis thaliana rosettes; and 3 : Tobacco plants).

The images of these 3 classes of plants are stored in the sub-folders A1, A2 and A3 inside the folder LSCData.

The accuracy obtained via transfer learning using Google's Inception-v3 model was 98%.

1. Firstly, we set up docker.
2. Then we install and run the Tensorflow docker image.
3. We organise our dataset.
4. Retrain the inception model for our own dataset.
5. Test our classifier using the label_image.py script.

You can use this [CodeLab](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0) by Google as a guide. Also this [tutorial](https://www.tensorflow.org/versions/r0.9/how_tos/image_retraining/index.html) is quite helpful.

##Dataset

The dataset can be downloaded from [here](http://www.plant-phenotyping.org/CVPPP2014-dataset).
The technical report included with the dataset describes the data acquisition, plant material, and environmental conditions in detail.
 

##Requirements

* [docker](https://www.docker.com/products/docker-toolbox)

##Usage 

1. Start the docker image `docker run -it -v ~/projects/tf_files/:/tf_files/ gcr.io/tensorflow/tensorflow:latest-devel`

2. Run the label_image script to label the image. `python /tf_files/label_image.py <path_to_file>`

<hr>


