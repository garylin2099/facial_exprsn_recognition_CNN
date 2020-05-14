Deep CNN implemented with Keras to recognize seven types of human facial expressions from the FER2013 dataset, achieving a test accuracy of 58.6%, close to 65.5% of human readers in recognizing the expressions. Our model was a lighter but faster version of VGG19, plus batch normalization and dropout layers. While the accuracy is lower than that of the state-of-the-art full VGG model (~72%), our model is 6 times faster and retains 70%+ of the state-of-the-art accuracy, and thus is an effective and cheap alternative to VGG19 for local machines with limited computing powers. Full project report: https://github.com/garylin2099/facial_exprsn_recognition_CNN/blob/master/project_report.pdf

### Dataset: FER2013
48 by 48 pixel grayscale images of faces. Seven expressions: 0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutra). The training set, public test set, and the private test set consist of 28,709, 3,589, and 3,589 examples, respectively. https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data

![image example](/img/eg_img.png)

### Architecture
Lighter but faster VGG19 structure. We also add batch normalization and dropout layer to the VGG19 structure to improve the performance.

![CNN architecture](/img/archtct.png)

### Prediction
Overall test accuracy: 58.6%. From the confusion matrix, we see that our model yields 75%+ for happiness and surprise, whereas has hard time recognizing disgust.

![confusion matrix](/img/cm.png)
