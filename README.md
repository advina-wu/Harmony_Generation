# Harmony Generation

This project aims to generate music harmony using the input music melody.

## Description

This project used several deep learning techniques to test out and compare the performance of each 

## Getting Started


### Dependencies
You can install all the **required dependencies** by running
```
pip install -r dependencies.txt
```


### Executing program

To run the project, clone the repo and run the following commands:

```
cd Harmony_Generation
```

There are total 3 methods of generating music harmony and they are listed below:
* harmony_transformer_sequence.ipynb
* harmony_transformer_matrix.ipynb
* harmony_lstm.ipynb

The default midi files are used to generate music is inside of the directory:
```
./data/transposed/classical
```
You can train the models and generating some harmony musics by simply running the entire jupyter files. Be aware that the training process might take up to 10 hours. 
If you would like to skip the training part, you can comment the 

```
model.fit(training_dataset,
            epochs=100,
            callbacks=callbacks,
            validation_data=vali_dataset)

```
and uncomment the 
```
# Include the epoch in the file name (uses `str.format`)
checkpoint_path = './lstm_training_checkpoints/ckpt_{epoch}'
checkpoint_dir = os.path.dirname(checkpoint_path)
latest = tf.train.latest_checkpoint(checkpoint_dir)
latest

model.load_weights(latest)
```


Above are the tranposed c-major music that are ready to be used to generate harmony. However, if you would like to test the performance of the models using different midi musics, run the below jupyter files:
* transpose_music.ipynb
Within this file, replace the "filePath" in the following code with your own file paths:
```
filenames = extract.extract_all_music("filePath")
extract.transpose_music("data/transposed/classical", "filePath", filenames)
```
Then the transposed musics will be stored under the directory and you can run the 
```
./data/transposed/classical
```
## Authors

Contributors names and contact info
Jingwen Wu
wujingwen0810@gmail.com


