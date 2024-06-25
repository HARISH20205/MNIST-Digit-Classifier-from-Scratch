# Neural Networks and Handwritten Digits!

### Introduction

Hey there! Ever wondered how computers can recognize handwritten numbers like magic? Well, buckle up as we embark on a journey through neural networks and the famous MNIST dataset using Python and NumPy!

### Unveiling the MNIST Dataset

Imagine a treasure trove of 70,000 handwritten digits eagerly waiting to be classified! This treasure trove is the MNIST dataset, boasting 60,000 training images and 10,000 test images of digits ranging from 0 to 9. Each image is like a little 28x28 pixel snapshot, grayscale of course, with a label telling us exactly which digit it is. With TensorFlow Keras, we effortlessly load and prep these images, normalizing pixel values to fit snugly between 0 and 1 and transforming labels into one-hot encoding for optimal learning.

### Crafting Our Neural Network

Now, onto our secret weapon: the neural network! Picture this: our network starts with 784 neurons (one for each pixel in those flattened images), then adds a layer of 64 neurons, each with a special sigmoid activation—perfect for capturing complex patterns. Finally, our network wraps it up with 10 neurons, employing softmax activation to crisply classify each image into its digit category.

### Training Adventures

Here’s where the real fun begins! We kick off training by initializing weights and biases and set our network loose with a trusty learning rate of 0.1. Over 1000 epochs, our network eagerly learns from its mistakes, using gradient descent to minimize errors and fine-tune its performance.

### Insights from Training

Join us on the rollercoaster of model training! With each epoch, our network crunches through forward passes to make predictions, computes cross-entropy losses, and then skillfully adjusts its parameters in the backward pass. Every 100 epochs, we pause to marvel at the progress—watching as our accuracy and loss metrics shape up!

### Evaluating Our Model

After all that training, it’s showtime! We unleash our model on the test set to see how well it performs. Metrics in hand, we scrutinize accuracy and cross-entropy loss, gaining insights into how our model stacks up against real-world challenges.

### Predicting the Future

Here’s where the magic unfolds! With our display_prediction function, we peek into the crystal ball of predictive analytics. Pick any random test image, and voila! Witness our model confidently predict the digit, complete with probabilities for that extra touch of insight. Compare it against the true label—just for fun!

### Testing

#### Generating Random Index

The `random.randint(0, 9999)` line selects a random index within the range of your test set. This allows you to test the model on different images each time you run the code.

#### Making Predictions

Once you have the random index, `x_test[index]` retrieves the corresponding test image. The neural network then processes this image through its layers (`W1`, `b1`, `W2`, `b2`) to generate predictions (`single_image_prediction`).

#### Displaying Results

The `display_prediction` function visualizes the test image, displays the predicted digit along with its probability score, and optionally shows the true label (`np.argmax(y_test[index])`). This helps you visually assess how well the model performs on unseen data.

### Conclusion

Using this approach, you can interactively test your MNIST digit classification model in Google Colab or any Python environment. It’s a fun and insightful way to see how your neural network learns to recognize handwritten digits and to gain confidence in its accuracy across various test cases. Enjoy exploring the world of neural networks and the fascinating realm of machine learning!
