# Pokemon-Identification

## Dataset
Import the dataset from https://www.dropbox.com/sh/s9r1av3m4eatd3y/AAA8zYti5b5tnyKfcah2Reaja. Due to storage constrains, I couldn't upload the whole data here.

## Data Preprocessing
- As the data contained the images of different sizes, they were reshaped to have the same shape. They were reshaped as (100, 100, 3).
- The training and testing data of each image was reshaped to an array of size 30000 (Just to keep in 1D).
- Each type of Pokemon was assigned a integer label {0, 1, 2}.

## Model Selection and training
- The model was a Sequential CNN.
- It had 4 layers:
  - Dense, 512 neurons, activation funtion as relu and input size of each image array as (30000,)
  - Dense, 256 neurons, activation funtion as relu 
  - Dense, 128 neurons, activation funtion as relu 
  - Dense, 128 neurons, activation funtion as relu 
  - Dense, to finally classify the pokemon type, 3 neurons(As we had only 3 classes), activation function as softmax
- The model is then compiled with adam optimizer and loss function as categorical crossentropy.
- It is trained by the training data for 25 epochs.

## Model Testing and evaluation

- On testing with the test data, the metrices were:
  - Accuracy with training data -> 0.9079
  - Accuracy with testing data -> 0.9431
  - loss with training data -> 9.322
  - Loss with tesiting data -> 10.022
 
