# Challenge 2 Submission Instructions

Load the training data within the /data/ folder and code scripts in Python or R that develops predictive models that predict the response of 4 drugs or 2 drug combinations that are included in the training data. Your model must be interpretable in the sense where you are at least able to identify the important features underlying predictions made. After developing models for each drug or combination, predictions must be made on provided Test Set Data (to be released), as well as identification of the key features of these predictions.

## Scoring

Submissions will be scored automatically based on accuracy of model predictions with a set of test data. Additionally, short answer questions will be evaluated by judges at Lantern for 20% weight (only top performing scores will be evaluated). It is required to submit specific files described below into a Results folder and for scripts used for model generation to be in participant's Code Ocean capsule. 

## Submission files

Two separate tables will be submitted to both describe each model used and give their prediction results on the test set. For the submission, only a single chosen model should be described for each of the 6 drug or drug/combinations to be modeled. If more than one model is available for different drug or drug/combination predictions, choose the model believed to be the best. Details of expected output for table submissions are described below.


### File Overview
Required submission files are provided with blank answers which are to be modified with the participant's ID (team name or individual name) and copied into the Results folder. If you have a team ID of "xyz" and the base file of "short_answers.txt", the final file copied into results after answers are included should be "xyz_short_answers.txt".  
Tables provided in a .tsv file have NA values which will be replaced with answers based on the drug combination challenge results. Short answer questions are provided in a text file, which should be edited so that submission answers are typed directly below.

1. Model Information Table  
The **"model_info.tsv"** (base file name) file will contain a basic description of the final model developed for the 6 different drug/drug-combination types. See Table 1 Fields section below for instructions on answer input.  

2. Model Prediction and Analyis Table  
The **"model_output.tsv"** (base file name) file will contain predictions made on test data as 1 for a responsive sample prediction and 0 for a prediction of an absence of drug efficacy (as in the training data), as well as a string input to indicate the most important feature involved in that prediction.  

3. Short Answer Text File  
The **"short_answers.txt"** (base file name) file contains a few answers that can be edited directly below the question, and must be within the specified word limit.  

To submit files, copy each of the modified files with the appropriate file name indicating participant ID into the Results folder and share results as a data asset.  


#### Table 1 fields
*Filename*: Respective models should be saved in the Code folder. Put the filename of the model file, including the extension (e.g., .rds).  

*Algorithm used*: Write a description of the algorithm used for the specific model. It can be a custom algorithm, or an algorithm from public packages. For algorithms from a public package that have more than one algorithm available, input them with the following format: package_algorithm (e.g., caret_rf, or sklearn_svm).  

*Training accuracy*: Overall accuracy of models on the entire training set as a fraction (e.g.: 0.55).  

*Number of Features*: Number of features used by model to make predicitons as an integer.  

*Feature evaluation method*: Describe the method used to determine the key feature for your models. This could be a popular method such as using public packages to calculate Shapley values, a custom approach, or any method of choice--there are no limitations on method used.  

*Overall key feature*: Input the feature most important for predictions for the entire training set when using the method described in "Feature evaluation method". Either provided features (e.g., mut_gene1 or rna_gene2) or custom/engineered features are allowed.  

*Cancer-type specific key feature*: The same as above, but determined with distinct cancer type categories. There will be separate rows for "BrainCNS key feature", "Prostate key feature", etc.  


#### Table 2 fields
Each entry into Table 2 will be either a prediction of response (as 1 or 0, as in the training data), and a string that indicates the most important feature. For example, there will be a "Fulvestrant_response" column, and a "Fulvestrant_key_feature" column. The response will be 1 or 0 for test set samples, and the key feature is the most important feature. The feature should be derived using the same methodology as in identification of key features in Table 1 - but corresponding to only a single sample. In general terms, the "key feature" should indicate what feature was most important for the prediction in that sample.  

### Short answers
In the Challenge 2 data asset, type in responses to the questions in "short_answers.txt" within the word limit and save them to the Submission folder.

## Submission 
Launch a Reproducible run which will execute the code needed to fill in the results for the tables and manually edit text files for short answers. When creating a Data Asset after a reproducible run to share your submission, use the format of Challenge2_participantID and the folder should be /data/Challenge2. After the data asset is created, make sure it is shared with participant judges from Lantern. The final name of the files should follow the format describe above. See the base Challenge 2 capsule Run file for an example of how to use a script to copy results create_sample_submission.py, which can be edited as needed. 
