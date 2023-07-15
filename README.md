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


# Dataset used
MRL eye datset has been used to train the model.
The dataset consists of 84,898 images consisting of both drowsy and non drowsy images with different lighting conditions, to make the model versatile.
The dataset can be downloaded from here: http://mrl.cs.vsb.cz/eyedataset

# Results
The model was trained for 9 epochs and attained a test accuracy of 93%.
More epochs can be ran to train the model furthermore and achieve a better accuracy.

![Screenshot 2023-07-15 222629](https://github.com/Chandan-h-509/Driver-Drowsiness-Detection/assets/76171489/8bfffd69-200b-4a50-a10b-e966a0201791)
