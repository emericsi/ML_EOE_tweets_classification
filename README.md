# ML_EOE_tweets_classification
Project 2 repository for the ML course (EPFL, autumn 2018)

## Modules and packages 
 First of all we worked on anaconda, if you do not use this navigator you ca, download it at https://www.anaconda.com/download/, we also worked using the latest update of python 3. To run all of our codes you need the following packages. 

- Pandas (avalaible in the basic version of anaconda)
- scikit-learn (avalaible in the basic version of anaconda) 
- matplotlib (avalaible in the basic version of anaconda) 
- string (avalaible in the basic version of anaconda) 
- wordcloud (for download and install write : conda install -c conda-forge wordcloud on the anaconda prompt or on the terminal. 

## Main organitaion
Our work is organised as follow :

- report : this report explains our work and comments the results we obtained. 
- code folder :
	- twitter-datasets :  contains all the datasets we used to create models
	- notebook data_analysis.ipynb : is a notebook which provides the data description and further analysis that the one performed in the repport.
	- py_functions : folder with all the python functions we created for this project
	- create_fast_datasets.py : run this script in order to create the datatest for the fasttext methods, make sur you deleted before the file trainfold1.txt, trainfold2.txt, trainfold3.txt, testfold1.txt, testfold2.txt, testfold3.txt, testFast.txt and Full.txt before. This files are in Fasttext\fT-datasets (see the section fastText for more information). 
	- Fasttext folder with all the script and results about fasttext method. 
	- all the scripts and folder used in the glove based approach (see glove based approach for more information).
	
## Glove based Approach
All the files relative to this approach are in the folder code. Two differents embbedings were tested. 


For the embeddings we created. we have the following files and folders : 
- vect : folder with all the scripts usefull for the creation of our word emebdding
- data_format_trained.py : script used to compute the coordinate of each tweet for this method 

for the twitter embeddings method : 
- data_format_pretrained.py : script used to compute the coordinate of each tweet for this method 
- Prediction_pretrained : folder with two csv : test_prediction_notnull.csv (final predciction for this method with some missings prediction) Final8prediction_pretrained.csv (final prediction for thi method can be submit on crowdAI but not our best). 
- Final_prediction.py compute the preciction for our best models for this method (there are some missing values). 
- Test_prediction_pretrained_Glove_approach.ipynb fills the missing values of the previous script. 
- Coss_val_pretrained.py run the last gridsearch for this method parameters can be changes in the grid seach and the import can be change to find the result of the method based on our own embeddings

All the results of the cross validation arre in the CVresult folder (pretrained for twitter trained for our embbedings).

## Fasttext 
Due to encoding of some caracters this method can only be run on Linux.  
This folder contained all our work with fasttext, there are some scripts and folders for the method itself, and specific one we created.
- grid_fasttext.py is the script to cross-validate the parameters of fasttext
- Logistic_grid.py is the script to cross-validate the logistic regression fitted afterr the fasttext
- run.py simply the script to obtain the final submission for the crowdAI 
- fT-datasets is a folder which conatains all the datasets usefull for this methods. 
- errors : folder with err1.npy to err5.npy corresponding to various gridsearch for grid_fasttext.py put together in grid_fastText.csv using error_inspection.py (err.npy is the result of the last grid-search)  
