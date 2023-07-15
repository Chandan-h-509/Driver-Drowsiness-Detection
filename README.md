# Driver-Drowsiness-Detection

Road accidents resulting from driver drowsiness pose a 
significant threat to public safety, leading to a substantial loss of 
lives worldwide. Detection of drowsiness and providing 
appropriate alerts can play a pivotal role in preventing these 
accidents.

# Methodology 
A Multi-Tasking Convolutional neural network (CNN) is used, which extracts 
eye features to accurately identify the onset of drowsiness. By 
extracting facial features using the Haar cascade classifier, we feed 
the obtained data into a transfer learning model (InceptionV3) which detects 
drowsiness accurately.

![Screenshot 2023-07-15 221956](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/78c35b99-cdd6-4c31-bcce-16ec53ab0502)

# Standarad used: EAR(Eye Aspect Ratio)
EAR is a mathematical formula for calculating the eye closing 
and opening state. Strating at the left-hand side and going 
clockwise the points are labelled from P1 to P6. With |P2-
P6|+|P3-P5| in the numerator and |P1-P6| in the denominator. If 
the ratio is close to 0, this means that the eye is closed and open 
if the value is slightly above 0. By setting a threshold value, if the 
value is lower than the threshold, then eye is labelled as closed 
and if above the threshold its labelled as open. In this case it will 
also be labeled as closed which will in turn be inferred as 
drowsy, but that should not be the case. This edge condition can 
be solved by setting a threshold time. If the eye is closed for a 
time exceeding threshold only then it should be set as drowsy.

![Screenshot 2023-07-15 222951](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/4d64d690-8cd1-4b1b-b826-ee1808837623)



# Dataset used
MRL eye datset has been used to train the model.
The dataset consists of 84,898 images consisting of both drowsy and non drowsy images with different lighting conditions, to make the model versatile.
The dataset can be downloaded from here: http://mrl.cs.vsb.cz/eyedataset

# Results
The model was trained for 9 epochs and attained a test accuracy of 93%.
More epochs can be ran to train the model furthermore and achieve a better accuracy.

![Screenshot 2023-07-15 223405](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/303e3617-094b-467e-87cb-1a66827daeb5)

# When Eye is Opened:

![Screenshot 2023-07-15 223619](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/0b8653b8-0284-4c71-8bbd-6a740b013794)


# When Eye is Closed:

![Screenshot 2023-07-15 223710](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/c0b45b02-91ac-4cc4-9b06-df1a6c68d3c4)


If the eye is closed for a substantial amount of time, an alarm sound is produced alerting the driver.

