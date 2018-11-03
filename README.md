# webcam_point_features
Detection of ORB features from online webcam imges.

With ORB open_cv features you can obtain the most important points in a webcam image, and see them how they change during the time if you move the object, for example, your hand.

![ORB Descriptor Hand](https://github.com/chuski92/webcam_point_features/blob/master/images/Peek%2003-11-2018%2012-05.gif?raw=true)

If I move my hand the points maintain in the same place.

It works by selecting some points (it is done by the same ORB detector), gives them a direction, angle and position, and it searches the points in the next frame and see if they changed. So you can know if the object has changed the postition and it's direction or not and you can position it in the space.

You can also specify a "mask", a matrix that contains 0s into the non important pixels of the image, and any other value in the ones that you can use to search for.

References:

[1] Hian-Kun Tenn. "OpenCV ORB feature matching" 2014.
https://www.youtube.com/watch?v=j2fLqKvbgpM

[2] OpenCV. ORB (Oriented FAST and Rotated BRIEF) 2014.
https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_orb/py_orb.html

[3] Ben Williams at Quora. What is ORB in computer vision? 
https://www.quora.com/What-is-ORB-in-computer-vision

[4] Gil. A tutorial on binary descriptors – part 3 – The ORB descriptor. 2013
https://gilscvblog.com/2013/10/04/a-tutorial-on-binary-descriptors-part-3-the-orb-descriptor/
