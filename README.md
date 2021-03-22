# Self_driving_car
Self driving car model using self trained CNN with additional NN layers trained on the left side,centre and right view pics of the car

I used udacity's car simulator to generate the training data for the car. I took left, centre and right view pictures and concatenate their image array 
together to get a continous flushed image as if it as from the driver's POV. I also used the ImageDataGenerator too randomly zoom and increase the brightness
of the pics wich can be expected to happen in real time application. 

I trained a Convolutional Neural Network with additional NN layers. It has 5 CNN layers (with a resnet in layer 2) and 3 NN layers. I applied dropout in NN as they have more number of weights which tend to overfit more than the convolutional kernel weights. I also have written the code for a learnig rate function called decay_rate but didn't need to use it since the model found the minimum without overshooting. Adam optimizer with standard B1(beta 1) and B2 (beta 2) were used.

# Results
I got 99.8% training accuracy and a 100% test accuracy(test cases were randomly split and hence weren't the toughest for the model). I also used a completely different race track with different road shapes and terrain(train terrain was plane while cross validation set has mountain terrain). I ended up getting 98.6% accuracy which I'm very impressed with since I myself was having difficulty while driving the car on track 2 for cross validation set data.
