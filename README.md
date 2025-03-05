
# Overview of the analysis: 
The purpose of this analysis was to create a machine learning model for the nonprofit foundation, Alphabet Soup, that can help select the applicants with the best chance of success to be funded by the foundation.

# Results: 
Data Preprocessing

* Processing the data, it was found that the "IS_SUCCESSFUL" column becomes the target for the machine learning model, using the features to predict if the funded money was used successfully.
* The other columns were all utilized as features to create correlations and predict the target.

Compiling, Training, and Evaluating the Model

* The model was created with 100 neurons for 3 different layers, each containing a different activation including relu, tanh, and sigmoid. This variety was chosen in hopes to utilize multiple methods, and many neurons to optimize the model.

After revising a model trained on all original data, there were some changes made in an attempt to optimize the model. These changes included:
* Dropping the columns 'SPECIAL_CONSIDERATIONS', 'ASK_AMT', 'ORGANIZATION', 'STATUS', and 'AFFILIATION'. These columns were dropped in an attempt to alleviate lesser relevant data from the model to increase accuracy.

* Grouping the various "ASK_AMT" column values into value ranges of '5,000-8,000', '8,001-100,000', '100,001-1,000,000', '1,000,000-100,000,000', '100,000,001-8,600,000,000'. This took the 8,747 unique values in this column into placed them into 5 bins for grouping. A statistics summary was performed on this column which revealed units such as the maximum, average, percentile, and minimum values for the column. It was discovered that over 50% of the values alone were 5,000. This stats summary became the bases for creating the bin value ranges as they are.

* After performing these changes from the original model that contained all original data, the accuracy actually decreased in the model below 65%.

# Summary:
It was suprising that in an attempt to clean the data of potentially irrelavent features, that decreasing them also decreased the accuracy of the model. After performing a few scenarios of increasing Neurons up to 200 for each layer, it did not seem to increase the accuracy, showing there is a limit that more neurons does not mean the accuracy will increase without furthur manipulation of data.

To further increase the accuracy of the data, different activation methods might need to be explored, more layers, and/or receiving more data from Alphabet Soup to feed the model with more data.
