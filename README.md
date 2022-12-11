# Neural_Network_Charity_Analysis
## Overview of the analysis

 * The purpose of the project was to use machine learning and neural networks,and the features in the provided dataset 
   to  create a binary classifier that is capable of    predicting whether applicants would be successful if funded by Alphabet Soup.
   
 * The Analysis entails preprocessing the data for the neural network model, compile, train and evaluate the model optimize the model.

### Resources
 * Data Sources: charity_data.csv.
 * Software: Jupyter Notebook, Pandas, scikit-learn, tensorflow.
 
#### Results
 * Data Preprocessing
 
    * The variable "IS_SUCCESSFUL" was considered as the target of the neural network model.
    
    * The variables;"APPLICATION_TYPE","AFFILIATION","CLASSIFICATION","USE_CASE","ORGANIZATION",
     "STATUS","INCOME_AMT","SPECIAL_CONSIDERATIONS","ASK_AMT" are considered to be the features for the model.
     
    * "EIN" and "NAME" which were considered to be identification variables,were removed as they were considered neither features or targets
  
  * Compiling, Training, and Evaluating the Model.
    
     * The number of input features used for the initial neural network model was 43

     * Two hidden layers were added to the model with the first layer containing 30 hidden nodes and 
        the second layer containing 25 hidden nodes. The output layer contained 1 neuron.
        
     * "Relu" activation function was used in the hidden layers and "Sigmoid" activation function was used in the output layer
        
     * The above specifications of the neural network model were chosen in an effort to match the provided starter
       code for this challenge.It also followed the third rule of thumb method discussed in StackExchange to provide 
       some guidance regarding model selection parameters, where one of the methods indicated that the number of hidden
       neurons (e.g., 80 and 30 for the current analysis) should be less than twice the size of the input layer (e.g., 86
      
      https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw
      
    *  The Initial Neural Network Model Structure:
    
    ![image](https://user-images.githubusercontent.com/64270455/206886688-bb2a29da-3db5-49b0-a057-cf73926a8f57.png)
    
     * The model was not  able to achieve the target model performance,as the acccuracy of the model was less than 75%

    ![image](https://user-images.githubusercontent.com/64270455/206887195-1bf3a4e9-7e7f-4288-927d-151617e5f4ea.png)


    * Steps Taken to Improve Model Performance
    
     * First, additional feature  "SPECIAL_CONSIDERATIONS", was dropped with the identification columns ("EIN" and "NAME") 
       in an effort reduce the number of input features for the neural network model during preprocessing  of the data .
       
     ![image](https://user-images.githubusercontent.com/64270455/206888244-c759103b-4511-4970-9ef0-d158a9be3390.png)
     
     ![image](https://user-images.githubusercontent.com/64270455/206888262-b3a8fca9-dfef-4c0f-83b2-ba050e9cf264.png)


     
     * Adding a varying number of neurons to hidden layers
     
     ![image](https://user-images.githubusercontent.com/64270455/206888179-5153304c-c334-42b4-a419-7bb9c01608f1.png)


     ![image](https://user-images.githubusercontent.com/64270455/206888209-72d20fdf-145f-445a-970f-47b1d0facef9.png)

     


     * Adding new hidden layers 
     
     ![image](https://user-images.githubusercontent.com/64270455/206888297-7c2d326b-ac27-4e7c-8905-049ea0951741.png)

     
     ![image](https://user-images.githubusercontent.com/64270455/206888318-3c3fe551-c810-4b2b-9ab0-ec094d17e86d.png)

     
     
     * Adding different activation functions, "Tanh and the "Sigmoid" functions 
     
     ![image](https://user-images.githubusercontent.com/64270455/206888338-cd45f9e7-0c8c-41a9-aa2e-db73d21fbdd9.png)
     
     ![image](https://user-images.githubusercontent.com/64270455/206888366-80049a03-4a15-4c09-b308-9cfbbce3579b.png)

##### Summary
      This deep learning neural network model did not reach the target accuracy of 75%. We can conclude that the model 
      is not performing to the targetted accuracy.Since we are in a binary classification situation, we could use a 
      supervised machine learning model such as the Random Forest Classifier which combines a multitude of decision trees
      to generate a classified output and evaluate its performance against our deep learning model.

    
    
   
   
