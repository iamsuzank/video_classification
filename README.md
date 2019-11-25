# video_classification
video classification using resnet  resnet-50 is trained on street dataset images(dataset contains classes:robbery,accident,traffic jam,
protest and normal).After training the network,resnet can classify the different events in video with high accuracy.
There is no flickering problem during prediction.Also it can capture the images from video when prediction is accident in the input video.

Videos can be understood as a series of individual images but when we treat video classification
as image classification a total of N times, where N is the total number of frames in a video then it causes flickering effect.
In the original post new approach 'rolling average' is used in video classification by making the assumption that subsequent frames
in a video are correlated with respect to their semantic contents.
[Algorithm]
1.Loop over all frames in the video file
2.For each frame, pass the frame through the CNN
3.Obtain the predictions from the CNN
4.Maintain a list of the last K predictions
5.Compute the average of the last K predictions and choose the label with the largest corresponding probability
6.Label the frame and write the output frame to disk

The original post is based on sport dataset.i have made a new datset i.e. street dataset that contains the image class such 
as accident,traffic jam,robbery,protest and normal.
some modifications are made so that when the input is given to the network and if the network classify  the video as of accident class
then the images of accident are taken and stored in separate folder.
 
[original post]=>https://www.pyimagesearch.com/2019/07/15/video-classification-with-keras-and-deep-learning/
