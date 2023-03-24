# Harmony Generation

This project aims to generate music harmony using the input music melody.

## Description

This project used several deep learning techniques to test out and compare the performance of each 

## Getting Started

How to run the project

To run the project, clone the repo and run the following commands:

cd FNet_with_BART_classification
pip install -r requirements.txt
python fnet.py



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
Above are the tranposed c-major music that are ready to be used to generate harmony. However, if you would like to test the performance of the models using different midi musics, run the below jupyter files:
* transpose_music.ipynb
Within this file, replace the <<filePath>> with 

filenames = extract.extract_all_music(<<filePath>>)


## Authors

Contributors names and contact info
Jingwen Wu
wujingwen0810@gmail.com


