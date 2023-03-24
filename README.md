# Harmony Generation

This project aims to generate music harmony using the input music melody.

## Description

This project used several deep learning techniques to compare the performance of each models. 

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
There are total 3 models of generating music harmony and they are listed below:
* harmony_transformer_sequence.ipynb
* harmony_transformer_matrix.ipynb
* harmony_lstm.ipynb

The default midi files used to generate music are tranposed c-major music which are inside of the directory:
```
./data/transposed/classical
```
You can train the models and generating harmony musics by simply running the entire jupyter files. Be aware that the training process might take up to 10 hours. 
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
The above codes are included in all three files.

### Try it out with your own midi files
If you would like to test the performance of the models using different midi musics, run the below jupyter files:
* transpose_music.ipynb
Within this file, replace the "filePath" in the block 4 + 5 in the transpose_music.ipynb, with your own file paths:
```
filenames = extract.extract_all_music("filePath")
extract.transpose_music("data/transposed/classical", "filePath", filenames)
```
Then the transposed musics will be stored under the directory.
```
./data/transposed/classical
```
Then you should be able to tun the models as usual.

## Authors

Contributors names and contact info
Jingwen Wu
wujingwen0810@gmail.com


## Reference
***************************************************************************************/
*    Title: GraphicsDrawer source code
*    Author: Smith, J
*    Date: 2011
*    Code version: 2.0
*    Availability: http://www.graphicsdrawer.com
*
***************************************************************************************/


