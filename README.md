# tribe3_emotions

This is a repository dedicated for training machine learning models for voice files with emotions (angry, disgust, fear, happy, neutral, or surprised) from video files downloaded from Youtube.

![](https://media.giphy.com/media/3o6nUNpJn4VznakjKM/giphy.gif)

## Weekly meeting time 

We plan to do slack updates every week 8 PM EST on Fridays. If we need to do a work session, we will arrange for that. Active members of the team working on this repo include:

* Bineeta Gupta (TRIBE 3 Fellow, Arizona State University) 
* Luke Lyon (Boulder, CO)
* Anwar Akkari (Yale University) 
* Jim Schwoebel (Boston, MA) 

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

## Dataset summary 

TBA, will post more about this this weekend. 

## Downloading data

TBA, will post more about this this weekend. 

## Making new datasets 

TBA, will post more about this this weekend. 

## References 
* [librosa](https://github.com/librosa/librosa)
* [spacy](https://spacy.io/)
* [numpy](http://www.numpy.org/)
* [scikit-learn](http://scikit-learn.org/stable/index.html)
* [keras](https://keras.io/)
