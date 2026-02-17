# fault-detection-project
In industry 4.0, AI plays a huge role in identifying the faults in the machinery which results in reduced costs and downtime. In this project, a comparison of model fit of unsupervised models such as isolation forest and one class Support vector machine has been studied. The reason for selection of unsupervised models is because the fault type data in such projects are very rare and there is a significant class imbalance between the normal class and faulty class. So if the general classification using 2 classes has been done, then the models would not learn to discriminate the classes well and there is a high chanc eof overfitting or underfitting. So to efficiently classify faults from the normal sensor readings, the mabove mentioned models are onyl trained on a single class which is the normal class and then the traine models are used to predict for the test data containing both normal class and faulty class. The basic idea is that the model would only learn the normal class and anything that differs from the normal class would be classified as faulty class.

The dataset is aquired from kaggle, called as Industrial equipment monitoring dataset. It contains sensor readings such as Temperature.pressure,vibration and    . The data set contains a total of 2000 observations, where 1400 are the normal readings and 600 are faulty readings. For training only 80 percent of the normal class has been used and the rest 20 percent has been conbined with the 600 fobs of faulty class as a test dataset.

The intitalization of models are as the follows:

For isolation forest a contamination of 0.05 has been used and for one class SVM, the sensittivity parametzer has been set for 0.05.

The following are the results:

Heatmap comparison:
Both the models have delivered similar kind of performance. One class SVM has a little edge with the recall of the faulty class but it is minimal.


