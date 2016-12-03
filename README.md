# CSC522 Course Project
Allstate Claims Severity 

Data Exploration --> data exploration.ipynb

Single Model:

Data Precessing for single model -- > Data Precessing_single model.ipynb

4 output :

          training dataset features:  "train_x.csv"
          
          train traget attribut: loss : "train_label.csv"
          
          testing dataset features: "test_x.csv"  
          
          test dataset ID: "test_id.csv" // This one is used for kaggle submission
          
These files precessed data for the single model input. 


Data Precessing for stacking model --> Dataset_stacking.ipynb

4 output: 

          Layer1 training dataset: 'train_layer1_x.csv'
                                   "train_layer1_label.csv"
          Layer2 training dataset: 'train_layer1_x.csv'
                                   "train_layer1_label.csv"                        
                        

I am constructiong the pipeline for stacking, before that you need to run the stacking manually. 

For example, if you have 4 models in first layer, these 4 models need train first using the Layer1 training dataset that we get from Dataset_stacking.ipynb. Then prepare the data for the second layer: use the Layer2 training dataset as an input for first layer's model, the outputs are then the training data for second layer's model. 

Note: currently, dividing the whole dataset for training models in two layers separately is not the best idea. But due to time limit, it is the fastest one. Later, I will complete this part for future use. 

Note: Note: Although I first used four different models in my first layer's stacking. But I found you will you better result if you applied similar models in the first model, for example, two NN and two xgboost.



