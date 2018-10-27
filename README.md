# Train emotions

This is a repository dedicated for training machine learning models for voice files with emotions (angry, disgust, fear, happy, neutral, or surprised) from video files downloaded from Youtube.

![](https://media.giphy.com/media/3o6nUNpJn4VznakjKM/giphy.gif)

## Team members

Active members of the team working on this repo include:

* Bineeta Gupta (Arizona State University) 
* Luke Lyon (University of Colorado - Boulder, CO)
* Anwar Akkari (Yale University) 
* Jim Schwoebel (Boston, MA) 
* Shivani Reddy (Clemson University) 

## Meeting times 

We plan to do slack updates every week 8 PM EST on Fridays. If we need to do a work session, we will arrange for that. 

## Goal / summary or prior models (how they were formed)  

Here are some goals to try to beat with demo projects. Below are some example files that classify various emotions with their accuracies, standard deviations, model types, and feature emebddings. It will give you a good idea on what to brush up on as you think about new embeddings for audio and text features for models. 

| Model Name	| Feature embedding | Accuracy	| Standard Deviation	| Modeltype| 
| ------------- | ------------- | ------------- | ------------- |------------- |
| disgust.pickle |	character, polarity, rhythm, spectral| 0.9775293015 |	0.009225004885	| random forest|
| surprise.pickle | character, polarity, onset, spectral, power |	0.8971036205 |	0.008219397678	| knn | 
| fear.pickle	| pos, polarity, spectral | 0.8406798246	| 0.003728070175	| knn |
| happy.pickle	| character, polarity, spectral, power | 0.68	| 0.03479685397	| hard voting |
| angry.pickle |	polarity, rhythm, spectral, power| 0.6548830038 |	0.04924646135	| gradient boosting |
| happy_sad.pickle	| power | 0.6543740573 |	0.01507843069 |	logistic regression |
| sad.pickle | character, polarity, rhythm, spectral, power |	0.6313155529	| 0.02186253158	| hard voting |
| happy_sad_neutral.pickle	| pos, spectral | 0.4698875525	| 0.02512849173	| logistic regression |
| all_emotions.pickle | character, pos, polarity, onset, rhythm, spectral |	0.2875083655	| 0.0358943377 |	knn | 

## Downloading the data

Make sure you have roughly 24 GB of free space on your hard disk.

Once you know you have this much space, you can download the dataset by clicking [this link](https://drive.google.com/open?id=1aWr0AsvYm2okmirbUqy4Ql2xQgEuyDzf). After you click on the link go to the top right corner of the page and click download (the icon with the down arrow). After this, the download should start. This could take a while based on your internet connection.

## Dataset summary / feature array 

The data is arranged in three folders: Audio, emotion_train_set, and training_audio_files. The file emotionsDfV1.csv is the result of running MFCC analysis on the emotion_train_set data. The file allemotions.csv is the result of running MFCC analysis on the training_audio_files. It is recommended that you only download the allemotions.csv file if you want to train a model yourself.
 
## Summary of results

The most accurate model tested is called model_v5.h5. Results from training this model are shown below.

| Training Epoch | Training Accuracy | Training Loss | Validation Accuracy | Validation Loss |
| --- | --- | --- | --- | --- |
| 5 | 56.48% | 114.85% | 68.97% | 85.70% |
| 10 | 67.50% | 86.57% | 77.87% | 61.35% |
| 15 | 71.69% | 72.14% | 82.18% | 54.66% |
| 20 | 75.55% | 65.52% | 84.48% | 45.62% |
| 25 | 79.64% | 57.24% | 82.47% | 46.75% |
| 30 | 82.23% | 50.39% | 84.48% | 40.41% |
| 35 | 83.29% | 47.96% | 79.60% | 57.19% |
| 40 | 84.38% | 43.01% | 86.21% | 36.51% |
| 45 | 85.44% | 41.76% | 86.49% | 33.85% |
| 50 | 86.32% | 39.01% | 86.49% | 35.93% |
| 55 | 86.53% | 36.50% | 87.36% | 32.43% |
| 60 | 87.62% | 34.08% | 86.49% | 39.63% |
| 65 | 87.93% | 33.44% | 87.36% | 45.29% |
| 70 | 87.89% | 31.50% | 88.79% | 33.19% |
| 75 | 88.85% | 31.47% | 87.93% | 32.94% |
| 80 | 89.67% | 27.63% | 86.49% | 41.41% |
| 85 | 89.73% | 27.68% | 87.07% | 33.21% |
| 90 | 90.08% | 26.63% | 88.51% | 35.59% |
| 95 | 89.90% | 26.53% | 87.64% | 33.43% |
| 100 | 91.30% | 25.00% | 87.36% | 36.27% |

## Comparison of results to goal

One goal of this project was to beat prior models' performances. The model "model_v5.h5" was trained for accuracy in correctly identifying all emotions. 

| Model | Feature embedding | Accuracy | Modeltype|
| --- | --- | --- | --- |
| all_emotions.pickle | character, pos, polarity, onset, rhythm, spectral | 28.75% | knn |
| model_v5.h5 | spectral | 87.36% | Keras Sequential Neural Network |

With an increase in accuracy of 58.61%, the Keras Sequential model thoroughly out-performs NeuroLex's current all-emotion detection. 


## References 
* [librosa](https://github.com/librosa/librosa)
* [spacy](https://spacy.io/)
* [numpy](http://www.numpy.org/)
* [scikit-learn](http://scikit-learn.org/stable/index.html)
* [keras](https://keras.io/)
