# TV-Script-Generator
Use LSTM models to generate 'fake' tv scripts given tv scripts for serials.

# About
- This project uses LSTM model to generate 'fake' tv script by recoginizing pattern, given a dialogue-based script as training data.
- The LSTM neural network is built form scratch and trained on an episode scriot of TV show 'seinfield'.
- The general approach used in building this project was -
  - Download the data from the given source.
  - Create lookup tables which wil provide embeddings to the words in the script based on the given data.
  - Tokenize the punctuation present in the data by converting them to words with similar syntax.
  - Save the pre-processed data to load them at a later point.
  - Train and save the model after training, if the train_loss is low-enough.
  - Generate different texts using trained model and evaluate the performance. Save the best model.

# Procedure to run the notebook
- First, Clone the repository.
- Download a script from any trusted source for datasets. One such source is (kaggle)[https://www.kaggle.com/datasets].
- An example tv script for the show seinfield is provided. You can download using [this](https://www.kaggle.com/thec03u5/seinfeld-chronicles#scripts.csv) link.
- Store the downloaded text file in a created directory named 'data'.
- Run all the notebook cells provided in the notebook. It is recommended to use 'GPU' while training the RNN model.
- You can modify the architecture of the give model according to your needs. For example, adding an extra layer in order tolearn more complex patterns.
- You can modify the hyper-parameters according to your needs and available gpu/cpu instance to reduce training time if needed.
- Code is written to generate new scripts using the trained model. You can modify the code according to your needs.

# Results Obtained
  *Following script was generated from the trained model against seinfield scripts dataset* -

  "elaine: player: period!

  hoyt: oh, hi.

  jerry: oh, hi, jerry, what happened to the stand?

  hoyt: what is the difference?

  vandelay: yes, i think i have to get it.

  george: you know, you know what i mean, you know that i was in mortal danger.

  hoyt: oh!

  hoyt: what do you mean?

  hoyt: no, no!

  george: no, no, no.

  vandelay: i don't think that would have been to law..

  hoyt: you know what i think that was going to die?

  george: no! you wanna go see?

  jerry: yeah.

  hoyt: oh, i don't want any idea........."
