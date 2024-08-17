# deep-learning-challenge

## Module 21 Challenge - Neural-Networks-Deep_Learning

### Alphabet Soup Charity Fundraiser
#### Overview
The purpose of this analysis is to help a nonprofit foundation called Alphabet Soup find a tool that can help it select the applicants for funding with the best chance of success in their ventures, specifically to decide which companies should recieve loans from Alphabet Soup. Alphabet Soup has supplied me with a dataset csv file that they gathered from previous loans. I will use the features in the provided dataset to create with my knowledge of machine learning, neural networks, and Python's Tensorflow, a binary classification model that can predict if an Alphabet Soup-funded organization will be successful if funded by Alphabet Soup.
## Results
#### Data Preprocessing
* What variable(s) are the target(s) for your model?
    * The target variable is the 'IS_SUCCESSFUL' column from application_df, in which the output indicates a successful funding application. A "1' means yes, and a '0' means no.
* What variable(s) are the features for your model?
    * The variable features for the model are 'EIN', 'NAME', 'APPLICATION_TYPE',	'AFFILIATION',	'CLASSIFICATION', 'USE_CASE',	'ORGANIZATION', 'STATUS', 'INCOME_AMT',	'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
* What variable(s) should be removed from the input data because they are neither targets nor features?
    * I originally thought that 'EIN', 'NAME', 'STATUS', and 'SPECIAL_CONSIDERATIONS' were irrelevant to the outcome. But after 7 unsuccessful attempts at a 75% accuracy, I decided to leave them all in there, except for 'EIN'. 'EIN' had no significance in the outcome, they were all unique, and I didn't want to take the chance that an error would occur just because it was a number. However on the other three, 'STATUS', and 'SPECIAL_CONSIDERATIONS', there were small numbers of unique values for them, almost insignificant. I took them out, thinking that they were irrelevant, also. I left 'NAMES' in because there were a tremendous amount of unique values, some of which belonged to the same organization. Which made all of the other variables relevant.
#### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * My initial model had two hidden_nodes, 80 in layer1 and 30 hidden-nodes in layer2, and using "relu" for my input activation, "sigmoid" for my output, and I used "adam as the optimizer throughout the optimizations. I started off with these numbers and activations because they are what was used in my class. The accuracy was right at 73%. From there I went to three hidden layers, basically because I thought that they would eventually be better than two. The hidden layers were 100, 30, and 10. Everything was the same, including the third hidden layer, which I kept the activation at "relu". I kept the epochs situated at 100 througout the exercise, as well.
* Were you able to achieve the target model performance?
  *  The target model performance level of 75% and above was not achieved until the last two optimizations.
* What steps did you take in your attempts to increase model performance?
  * I was trying all sorts of different neurons, activations, and cutoff values when binning the data, but nothing got me over the 75% threshold. On the eighth optimization, I took a look at the columns, and realized that I needed to do some binning on the "NAMES" column. I had been overlooking this for every run, and realized that I needed to include it. I set up a cutoff value, changed my activation models for input back to my original choice, "relu", my output back to the original of "sigmoid", and my deep layers back to 100-30 and 10. After I ran the optimization. the accuracy level then shot up to 79.36%. I then tried a ninth optimization, just to check on what would happen if I changed my input activation model to "relu". with the rest of the input layers, and output layer, set to "sigmoid" It didn't change much, just moved sightly downward to 79.30% accuracy.
#### Summary
This was an interesting outcome, because I was so sure that by changing the optimization parameters would drastically improve upon my original accuracy of 73.00%. I tried adding a third or fourth hidden layer, adjusting my activation functions from "relu", "sigmoid", and "swish", adjusting the number of neurons for each hidden layer, and the cutoff values when binning the categories. Nothing that I did moved the accuracy that much, until I realized that I needed to keep the "NAMES" column back in the dataset. I realized that "NAMES" needed to be put back in because it had many unique values, including when I put alot of them into the "Other" column (20043). I used the pd.get_dummies command, along with dtype=int) function to convert the name data to integers, to be useful as a data for my target outcome. That was the main difference, as my accuracy shot up to almost 80%. Which translates into that an applicant has almost an 80% chance of being successful by using this model. I didn't bother removing the 'STATUS' and 'SPECIAL_CONSIDERATIONS' columns because they were so insignificant to the outcomes.

As far as using other models as a classifier, I could have tried using a decision trees, or random forests classifiers. A decision tree is simpler and more interpretable, but prone to overfitting. A random forest is more complex and prevents the risk of overfitting. Random forest utilizes many decision trees classifiers whithin, which would work well with a dataset like this one. I would like to experiment with the difference between these two, to see which one would be more accurate, compared to our model here. That would be for another day.







 





