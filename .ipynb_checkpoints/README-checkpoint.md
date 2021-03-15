
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone:

## Dog Breed Image Classifier
### By Chris Burger

### Problem Statement
Can I create a dog-breed image classifier?
This could be used in situations where a rescue dog may show up but noone knows what breed it is. This has actually happened to myself.
So, using Machine Learning and a Convolutional Neural Network, can I accurately predict the breed of a dog from an image?
"What kind of dog IS this??"

---
### Datasets Used

*This Data originated from the Stanford Dogs Dataset 
he dataset used is the ‘Stanford Dogs Dataset’ found at http://vision.stanford.edu/aditya86/ImageNetDogs/. This prevented me from having to scrape images, which saved an amazing amount of time. There is also a smaller dataset for use on kaggle, but I chose the larger one for this model.

---

### Data Dictionary
As this dataset consists of purely images, only images and annotations/labels(breed names) are used.

---

### Analysis Summary
data details: 20,580 total images of 120 different Dog Breeds (around 170 pics per breed. A Good size of data to work with).

I ended up using InceptionV3 as the pre-trained model/base layer for each of my models, which seemed to be the best for multiple reasons. I tested using different image dimensions, batch sizes and more...but the best working dimensions seemed to be around 180x180(pixels) and batch size of 32 is preferred.

With 10 Epochs, I got 66.5% training and 70.45% testing accuracies.
With 20 Epochs: 81.92% training accuracy and 76.61% testing accuracy.
&
With 100 Epochs: 91.27% Training Accuracy and 70.63% testing Accuracy. Better, but way overfit!
These came as quite the surprise as I was used to seeing the model improve as the # of epochs increased. This definitely is not the case when it came to the parameters that I ended up using.

---

### Conclusions & Considerations
In conclusion, running my Inception V3 CNN model with Global Average Pooling seemed to work the best, with my computational power anyway. I REALLY want to make the model better and did not get to my personal end goal of creating my own demonstration that would allow an image to be uploaded and then it would be resized and checked for breed -- unfortuntately, there were time constraints and I also ran into some technical issues/programming bugs later on in the process -- so I wasn’t able to create my own but *as I will be continuing to work on this project/model, I should have one up and running some time in the near future. 

Regarding the ASPCA and other dog shelters or rescues, this tool could be invaluable to have a more effective alternative to help determine what kind of breed a found dog is….as opposed to a vet or shelter-worker just guessing based on the appearance. Computers are probably better than humans when it comes down to recognizing the more discreet characteristics of each breed -- and that’s just one example


---

### Sources Cited:
*# Citations:
#### Dataset: http://vision.stanford.edu/aditya86/ImageNetDogs/
*InceptionV3: https://keras.io/api/applications/inceptionv3/
*TF Keras: https://www.tensorflow.org/api_docs/python/tf/keras
#### Assistance with coding:
*Lesson 7.04
*https://machinelearningmastery.com/handwritten-digit-recognition-using-convolutional-neural-networks-python-keras/
*Then found this and it was extremely useful to help guide me through creating my own models: https://awesomeopensource.com/project/stormy-ua/dog-breeds-classification (examples of others doing the kaggle competitions/using a similar data set)
*(for example):https://www.kaggle.com/linhlpv/image-deteciton-dog-stanford

