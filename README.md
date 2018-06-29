# Info-RandomForest
Some useful links and info on random forest methods

* [RF+Clustering+MDS](https://stats.stackexchange.com/questions/134095/how-to-get-class-probabilities-for-unsupervised-random-forest/183116)

Nice example of how to attach a probability to predictions based on RF. Key idea: 1) build a cluster based on RF proximity metric; 2) then you can use your clusters as classes to train a supervised model; 3) adopt your supervised model to make prediction on new data.
