# Basic-Transfer-Learning-model

Basic transfer learning with cats and dogs data

# There will be a training folder and a testing folder.
# Each of these will have a subfolder for cats and another subfolder for dogs.

# Split data into training and test sets
# The following code put first checks if an image file is empty (zero length)
# Of the files that are not empty, it puts 90% of the data into the training set, and 10% into the test set.
# Data augmentation (try adjusting the parameters)!
# Here, you'll use the ImageDataGenerator to perform data augmentation.

# Things like rotating and flipping the existing images allows you to generate training data that is more varied, and can help the model generalize better during training.
# You can also use the data generator to apply data augmentation to the validation set.
# You can use the default parameter values for a first pass through this lab.

# Later, try to experiment with the parameters of ImageDataGenerator to improve the model's performance.
# Try to drive reach 99.9% validation accuracy or better.


# Get and prepare the model
# You'll be using the InceptionV3 model.

# Since you're making use of transfer learning, you'll load the pre-trained weights of the model.
# You'll also freeze the existing layers so that they aren't trained on your downstream task with the cats and dogs data.
# You'll also get a reference to the last layer, 'mixed7' because you'll add some layers after this last layer.
# Add layers
# Add some layers that you will train on the cats and dogs data.

# Flatten: This will take the output of the last_layer and flatten it to a vector.
# Dense: You'll add a dense layer with a relu activation.
# Dense: After that, add a dense layer with a sigmoid activation. The sigmoid will scale the output to range from 0 to 1, and allow you to interpret the output as a prediction between two categories (cats or dogs).
# Then create the model object.

# Train the model
# Compile the model, and then train it on the test data using model.fit

# Feel free to adjust the number of epochs. This project was originally designed with 20 epochs.
# For the sake of time, you can use fewer epochs (2) to see how the code runs.
# You can ignore the warnings about some of the images having corrupt EXIF data. Those will be skipped.

# Predict on a test image
# You can upload any image and have the model predict whether it's a dog or a cat.

# Find an image of a dog or cat
# Run the following code cell. It will ask you to upload an image.
# The model will print "is a dog" or "is a cat" depending on the model's prediction.
