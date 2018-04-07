# B&W Flower Image Colorization
<small>Elad Shabi, Nadav Dori, Chen Shmilovich</small>
<hr>

In the following code we built a convolutional neural network using keras library,<br>
that gets as an input 32X32 pixels grayscale images of flowers, and generates an output of 96X96 colored flowers images.

<hr>

* <b>Data-Sets</b><br>
We used a data set that contains 8189 pairs of grayscale and colored flower images<br>
The training set is consisted of 70% of the images, while the test set is consisted of 30% of them. 10% of the training images are used for validation.<br>

<hr>

* <b>Model's Network Architecture</b><br>
We've been experimenting with several different designs of the network.<br>
In every model we chose to use RELU activation function on the hidden layers of the network.<br>
On the output layer we used sigmoid function in order to output values between 0 and 1.<br>
Generally the network processed the input image in such a way that it has been shrinked on the first few layers and than upscaled to the desired output dimensions. We used strides and up-sampling in order to do so.<br>
We achieved the best results for this assignment using the described method.<br>
Overfitting on these kind of networks is a subjective matter, therefore we needed to examine the results and determine wether they match our expectations.
<hr>

* <b>Model's Training</b><br>
We normalized the input pixel values to be between 0 and 1, and used the mean square error loss function to measure our results.<br>
After that we also tried using the "msle" loss function which we found more suitable for our project.
On both occasions we used the "rmsprop" optimizer to minimize our loss.
<hr>

* <b>Performance</b><br>
We were suprised by our initial results, it seemed like the network recognized the shapes and textures of the input images, and also colored them nicely.<br>
The only issue we had is the lack of sharpness of the output images.<br>
We then added more convolutional layers to deepen our network and we increased the amount of filters in each layer dramatically. Furthermore we tested different batch sizes and number of epochs.<br>
The output images became more sharp and clear, the results were way over our expectations.
<hr>

* <b>Results:</b><br>
<table style="float:left">
    <tr>
        <th style="text-align:center">Input</th>
        <th style="text-align:center">Model A</th>
        <th style="text-align:center">Model B</th>
        <th style="text-align:center">Model C</th>
    </tr>
    <tr>
        <td><img src="b_model_examples/12_x_test.png"></img></td>
        <td><img src="b_model_examples/12_prediction.png"></img></td>
        <td><img src="c_model_examples/12_prediction.png"></img></td>
        <td><img src="d_model_examples/12_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/19_x_test.png"></img></td>
        <td><img src="b_model_examples/19_prediction.png"></img></td>
        <td><img src="c_model_examples/19_prediction.png"></img></td>
        <td><img src="d_model_examples/19_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/20_x_test.png"></img></td>
        <td><img src="b_model_examples/20_prediction.png"></img></td>
        <td><img src="c_model_examples/20_prediction.png"></img></td>
        <td><img src="d_model_examples/20_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/24_x_test.png"></img></td>
        <td><img src="b_model_examples/24_prediction.png"></img></td>
        <td><img src="c_model_examples/24_prediction.png"></img></td>
        <td><img src="d_model_examples/24_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/29_x_test.png"></img></td>
        <td><img src="b_model_examples/29_prediction.png"></img></td>
        <td><img src="c_model_examples/29_prediction.png"></img></td>
        <td><img src="d_model_examples/29_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/94_x_test.png"></img></td>
        <td><img src="b_model_examples/94_prediction.png"></img></td>
        <td><img src="c_model_examples/94_prediction.png"></img></td>
        <td><img src="d_model_examples/94_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/101_x_test.png"></img></td>
        <td><img src="b_model_examples/101_prediction.png"></img></td>
        <td><img src="c_model_examples/101_prediction.png"></img></td>
        <td><img src="d_model_examples/101_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/103_x_test.png"></img></td>
        <td><img src="b_model_examples/103_prediction.png"></img></td>
        <td><img src="c_model_examples/103_prediction.png"></img></td>
        <td><img src="d_model_examples/103_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/160_x_test.png"></img></td>
        <td><img src="b_model_examples/160_prediction.png"></img></td>
        <td><img src="c_model_examples/160_prediction.png"></img></td>
        <td><img src="d_model_examples/160_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/202_x_test.png"></img></td>
        <td><img src="b_model_examples/202_prediction.png"></img></td>
        <td><img src="c_model_examples/202_prediction.png"></img></td>
        <td><img src="d_model_examples/202_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/322_x_test.png"></img></td>
        <td><img src="b_model_examples/322_prediction.png"></img></td>
        <td><img src="c_model_examples/322_prediction.png"></img></td>
        <td><img src="d_model_examples/322_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/341_x_test.png"></img></td>
        <td><img src="b_model_examples/341_prediction.png"></img></td>
        <td><img src="c_model_examples/341_prediction.png"></img></td>
        <td><img src="d_model_examples/341_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/342_x_test.png"></img></td>
        <td><img src="b_model_examples/342_prediction.png"></img></td>
        <td><img src="c_model_examples/342_prediction.png"></img></td>
        <td><img src="d_model_examples/342_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/399_x_test.png"></img></td>
        <td><img src="b_model_examples/399_prediction.png"></img></td>
        <td><img src="c_model_examples/399_prediction.png"></img></td>
        <td><img src="d_model_examples/399_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/400_x_test.png"></img></td>
        <td><img src="b_model_examples/400_prediction.png"></img></td>
        <td><img src="c_model_examples/400_prediction.png"></img></td>
        <td><img src="d_model_examples/400_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/790_x_test.png"></img></td>
        <td><img src="b_model_examples/790_prediction.png"></img></td>
        <td><img src="c_model_examples/790_prediction.png"></img></td>
        <td><img src="d_model_examples/790_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/850_x_test.png"></img></td>
        <td><img src="b_model_examples/850_prediction.png"></img></td>
        <td><img src="c_model_examples/850_prediction.png"></img></td>
        <td><img src="d_model_examples/850_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/900_x_test.png"></img></td>
        <td><img src="b_model_examples/900_prediction.png"></img></td>
        <td><img src="c_model_examples/900_prediction.png"></img></td>
        <td><img src="d_model_examples/900_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/920_x_test.png"></img></td>
        <td><img src="b_model_examples/920_prediction.png"></img></td>
        <td><img src="c_model_examples/920_prediction.png"></img></td>
        <td><img src="d_model_examples/920_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/2065_x_test.png"></img></td>
        <td><img src="b_model_examples/2065_prediction.png"></img></td>
        <td><img src="c_model_examples/2065_prediction.png"></img></td>
        <td><img src="d_model_examples/2065_prediction.png"></img></td>
    </tr>
    <tr>
        <td><img src="b_model_examples/2058_x_test.png"></img></td>
        <td><img src="b_model_examples/2058_prediction.png"></img></td>
        <td><img src="c_model_examples/2058_prediction.png"></img></td>
        <td><img src="d_model_examples/2058_prediction.png"></img></td>
    </tr>
</table>
