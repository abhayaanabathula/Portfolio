Main Points:


* Compeleted 
    
    - I have the data 
    - EDA is pretty much done unless I think of some other visuals/models that could be helpful 
    - Basic modeling is done


* NLP analysis

    - Multinomial Naive Bayes Modeling
    - used for text classification 
    - had to convert target variable to int, not the desired goal
    - logistic regression?
        - https://stackoverflow.com/questions/36877675/naive-bayes-for-regression
        - Warning Message 
        - 'Increase the number of iterations (max_iter) or scale the data'
    - autokeras text regression: https://autokeras.com/tutorial/text_regression/


* Quantitative variable analysis 

    - OLS, KNN, LassoCV, RandomForest
    - OLS, LassoCV, and RandomForest all performed similarly
    - RandomForest performed the best with score of 0.46
    - KNN did worse than the others and the scores suggest overfitting 
    - No models look to be overfit 
    - RandomForest model actually may display signs of underfitting even though it scored the best 
    
* What's next 

    - autokeras text regression? 
    - neural network for quantitative analysis 
    - combine the data types into one analysis
    - Gridsearch?
    - streamlit app
    
    
* Notes from Caroline meeting
    
    - ADAboost model 
    - neural network
    - concat for datasets 
    

* Issues 

    - We'll see what happens when I try the neural network modeling, the NLP analysis took some time to run to completion
    - Honeslty, this dataset is weird, the models are not performing well even though I did my best in cleaning 
    - I'll just have to keep tweaking the models to get some better results (Gridsearch?)
    - At, the end of the day, my main priority will be to conceptually understand the issues as much as possible so I can at least explain         why these models are not performing well  
    

* One on one?

    - most likely, just depends on what issues are coming