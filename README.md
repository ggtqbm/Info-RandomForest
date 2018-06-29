# Info-RandomForest
Some useful links and info on random forest methods

* [[RF+Clustering+MDS]](https://stats.stackexchange.com/questions/134095/how-to-get-class-probabilities-for-unsupervised-random-forest/183116) - Nice example of how to attach a probability to predictions based on RF. Key idea: 1) build a cluster based on RF proximity metric; 2) then you can use your clusters as classes to train a supervised model; 3) adopt your supervised model to make prediction on new data.
```
library(mlR)

n = nrow(iris)
iris.train = iris[seq(1, n, by = 2), -5]
iris.test = iris[seq(2, n, by = 2), -5]
task = makeClusterTask(data = iris.train)
mod = train("cluster.kmeans", task)

newdata.pred = predict(mod, newdata = iris.test)
newdata.pred
#> Prediction: 75 observations
#> predict.type: response
#> threshold: 
#> time: 0.00
#>    response
#> 2         2
#> 4         2
#> 6         2
#> 8         2
#> 10        2
#> 12        2
#> ... (#rows: 75, #cols: 1)

```


