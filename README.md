Check the output of the outputcolumns https://docs.microsoft.com/en-us/dotnet/machine-learning/resources/tasks in all trainers:

**binaryclassification**: outputs range from 0 to 1 - wether the given data is or is not something (rows labeled 0 or 1).
**multiclassclassification**: outputs an array which contain ranges of 0 to 1 - wether the given data is or is not something. Rows are labeled 0 - N - in the order of the numbers given in the labels. (So if label number 0 is pizza, label number 1 is hamburger and label number 2 is kebab, output array[0] is wether or not the given data is pizza, raging 0.0 - 1.0, and array[1] 0.0 - 1.0 wether it is being hamburger, array[2] 0.0 - 1.0 wether it is being kebab).

