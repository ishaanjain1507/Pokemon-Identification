# Pokemon-Identification

## Dataset
Import the dataset from https://www.dropbox.com/sh/s9r1av3m4eatd3y/AAA8zYti5b5tnyKfcah2Reaja. Due to storage constrains, I couldn't upload the whole data here.

## Data Preprocessing
- As the data contained the images of different sizes, they were reshaped to have the same shape. They were reshaped as (100, 100, 3).
- The training and testing data of each image was reshaped to an array of size 30000 (Just to keep in 1D).
- Each type of Pokemon was assigned a integer label {0, 1, 2}.

## Model Selection
- The model was a Sequential CNN.
- It had 4 layers:
  - Dense, 512 neurons, activation funtion as relu and input size of each image array as (30000,)
  - Dense, 256 neurons, activation funtion as relu 
  - Dense, 128 neurons, activation funtion as relu 
  - Dense, 128 neurons, activation funtion as relu 
  - Dense, to finally classify 
