Check the output of the outputcolumns https://docs.microsoft.com/en-us/dotnet/machine-learning/resources/tasks in all trainers:

**binaryclassification**: outputs range from 0 to 1 - wether the given data is or is not something (rows labeled 0 or 1).
**multiclassclassification**: outputs an array which contain ranges of 0 to 1 - wether the given data is or is not something. Rows of the label column are integers 0 - N. (If label number 0 is pizza, label number 1 is hamburger and label number 2 is kebab, output array[0] is wether or not the given data is pizza, raging 0.0 - 1.0, and array[1] 0.0 - 1.0 wether it is being hamburger, array[2] 0.0 - 1.0 wether it is being kebab).

**regression**: outputs a predicted float - based on trained data where one column (of float) was marked as label - with new data missing the corresponding label column.

**clustering**: outputs a uint - the id of the nearest cluster, and a float array containing the distances to each cluster where index is cluserid - 1. The metrics given from `mlContext.Clustering.Evaluate()` contains `DaviesBouldinIndex`. To find the most suitable numberOfClusters for the data - find value of DaviesBouldinIndex where it is being the lowest.

**anomalydetection**: outputs a double array with dimension depending on the type of transform used from the `TimeSeries` namespace, for instance DetectSpike or DetectChangepoint. Alert 0 or 1 specifies if the data point with 1 indicating it is spike/is changepoint, score is the input column of the data (in float), P-Value indicate how likely the point is being an anomaly, between 0 and 1 where towards 0 indicate anomaly, and Martingale value of how "weird" the data point is: https://docs.microsoft.com/en-us/dotnet/machine-learning/tutorials/sales-anomaly-detection  
