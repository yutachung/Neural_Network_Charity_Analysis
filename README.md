# Neural_Network_Charity_Analysis

## Overview of the Analysis
     In this analysis, we take a look at the csv file and preprocess the data, compile, train, and evaluate
the model, and then make further attempts to optimize the model. We create the model in attempt to predict
whether the the loan is successful or not by cleaning up the data through methods such as binning and scaling
the data.

## Results
     For the dataframe we have created from the csv file, we consider the "IS_SUCCESSFUL" column to be the
target for our model since that is the value we would like to correctly predict. The features would be the
rest of the columns with an exception for "NAME" and "EIN" since they do not contribute anything valuable
to the data that would help our model. Aside from "NAME" and "EIN" being removed from the data, other features
that could be put into consideration for being removed could be "AFFILIATION". Another additional way to
filter the data would be to remove rows which show inactive organizations.
     When compiling, training, and evaluating the model, the number of layers was two to run a deep neural
network rather than a basic one, and had 8 and 5 for hidden layer 1 and layer 2 respectively. These values
were assigned arbitrarily to test the waters of how the model would perform. Afterwards, to judge whether
these values were enough, they would be roughly doubled to 20 and 10 respectively. However, the change did not
have any significant impact on the model's performance. Another step that was taken in an attempt to improve
the accuracy rate was to bin the "ASK_AMT" column. The count for amounts of 5000 dominated the column in which
any value that was greater or less than 5000 was binned into separate categories. This was done in the first
attempt to see if this had any impact on the model, but unfortunately it did not make much of a difference.
Ultimately in the end, despite changing the layers and changing activations could not bump up the model's
performance to 75% and stubbornly maintained an accuracy rate of roughly 72%.

## Summary
     Overall, the model's performance was mediocre at best with an accuracy rate hovering around 72%. The
model had struggled to reach a performance of 75% with additional measures taken to optimize it through
additional data cleaning, additional layers, and increased inputs in the hidden layers. The data did not
see any signifcant changes regardless of changing the activation from relu to different methods. Since
these methods did not make any noticeable changes, it could be advised to push towards a random forest
classifier model since the model is able to handle outliers and nonlinear data which may possibly seem to
be the issue of what the current model is struggling to deal with.
     