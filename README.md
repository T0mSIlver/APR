# APR 2023
Labs and individual project work for the "Deep learning" elective I was enrolled in for 3 months in Ecole Centrale de Lille in 2023.

## Fil rouge (individual course project)

It is a project to classify images of characters from the Chars74K[^1] dataset using convolutional neural networks (CNNs).
It was run on Kaggle[^2] using a Nvidia P100 GPU. The total runtime is several hours.

- Model 1: A simple CNN inspired by TensorFlow tutorial, with 62 output neurons for 62 classes. Achieved 89% accuracy and 0.33 loss on validation set, but suffered from overfitting.
- Data augmentation and dropout: Techniques to prevent overfitting by applying random transformations to the training images and randomly dropping out some neurons during training. Improved accuracy to 90% and loss to 0.26.
- Model 2: A more complex CNN inspired by another Kaggle notebook, with more filters, pooling layers, and a larger hidden layer. Increased accuracy to 91% and loss to 0.25.
- Model 3: An optimized version of model 2 using Hyperband tuner to find the best hyperparameters, such as number of filters, dropout rate, and number of hidden units. Obtained similar performance as model 2 but with faster convergence.
- Predictions on new data:
  - Tested the model on images from MNIST, with mixed results. Remember that MNIST digits are hand-drawn conversely to the digits and letters from the Chars74K dataset which are computer-made.
  - Test on the Alphabet Characters Fonts Dataset[^3], with mixed results. More convetional-looking fonts are well-recognized, contrary to exotic fonts which are even complicated for a human to decipher.


## TPs (labs)
The labs were conceived by the elective's teachers : Vincent Ledda and Benoît Trouillet.
The notebooks in each folder are my personal work. Sometimes, hints were given in the form of a function skeleton for instance.  

### TP1
- Comparison of the numpy.add() and a custom matrix addition function on pandas DataFrames
- Implementation of a script for determining the companion matrix of a numpy.polynomial Polynomial
- Merging tables and pivot tables
- Visualization of the penguins[^3] dataset

### TP2
- Construction of a simple gradient descent algorithm from scratch
- Optimization of the number of iterations necessary to reach the desired precision
- Add a moment term in the gradient descent step and optimization of the moment coefficient value
- Change the point where the gradient is calculated for the Yurii Nesterov point = x<sub>n</sub> + m(x<sub>n</sub>-x<sub>n-1</sub>)
- Data visualization, standardization
- Study of features using their coefficient in a linear regression
- Linear regression coefficient calculation using the gradient descent algorithm we implemented

### TP3 
- Construction of simple neural networks to approximate various distributions :
  - a set of 100 000 points around a straight line
  - a set of 100 000 points around a 4th degree polynomial
- Construction from scratch of a training loop allowing for real-time visualization of the model's progress 
- Construction from scratch of a training loop for the classification of MNIST digits images
- Validation of the model on a manually drawn image chiffre.png
- Interpretation of the model's shortcomings, production of relevant metrics
- Creation of a development environment
  - model function parameters:  image size and number of classes
  - train step function parameters : model, optimizer
  - main function parameter : number of epochs

 
## Course Material and SGD Visualization
The visualizations are mainly comprised of animations 

- Gradient descent visualization in 1D, 2D 
- Gradient descent with optimal step size 
- Visualization of gradient descent on the Rosenbrock function 
- Visualization of the orthogonality of successive steps when the step size is optimal 
- Stochastic gradient descent



[^1]: http://www.ee.surrey.ac.uk/CVSSP/demos/chars74k/
[^2]: https://www.kaggle.com/code/tomvaucourt/fil-rouge-apr-2023
[^3]: https://www.kaggle.com/datasets/thomasqazwsxedc/alphabet-characters-fonts-dataset
[^4]: https://github.com/allisonhorst/palmerpenguins
