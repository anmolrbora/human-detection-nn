# Human Detection
Implemented the Histograms of Oriented Gradients (HOG) feature and a Two-Layer Perceptron (Neural Network) for detecting human in 2D color images.

#### Instructions: <br>

* Run the source code in Jupyter Notebook. <br>
* Make sure the path to the images (Human folder) is correctly set. (Currently set according to my location) <br>
* The training function is not called because I have already trained the model. If you wish to train it yourself then you need to uncomment the weight and bias initialisation part (which is currently commented) and uncomment the part where the weights and biases are read from the respective .csv files. And then call the ```NN.begin()``` function which will train the model.<br>

#### About:<br>
1. Converted color image into grayscale using the formula ```I=Round(0.299R+0.587G+0.114B)``` where R, G and B are the pixel values from the red, green and blue channels of the color image.<br>
2. Used Prewitt's operator to compute x and y image gradients from the grayscale image and then compute edge magnitude and gradient angles.<br>
3. Quantized the gradient angle into one of the 9 bins to calculate the HOG descriptor.<br>
4. Finally used the HOG descriptor as the input to the two-layer neural network.<br>
