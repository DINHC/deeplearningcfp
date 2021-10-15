# deeplearningcfp

Overview: 

- This code was made to read a charity data csv and train a machine learning to predict whether applicants for fundign will be successful. 
- Once the initial code was done a follow up code was made in an attempt to boost the accuracy rate to higher than 75%.


Results: 

Data Preprocessing

-What variable(s) are considered the target(s) for your model?
   
    Starting Code:
        The variable we are focusing on is ["IS_SUCCESFUL"] column 
        
    Optimized Code: 
        Same as Starting Code

-What variable(s) are considered to be the features for your model?

     Starting Code: 
     
     Optimized Code:

-What variable(s) are neither targets nor features, and should be removed from the input data?
   
    Starting Code: 
        The columns ['EIN'] anmd ['NAME'] were dropped as they held no use 
        
    Optimized Code:
        Same as Starting Code
        

Compiling, Training, and Evaluating the Model

-How many neurons, layers, and activation functions did you select for your neural network model, and why?

    Starting Code:
    Three layers were used with the first having 50 units and input dim=36 having a relu activation. 
    The second layer having 30 units and having a relu activation and the last 
    being a sigmoid activation with 1 unit. 
    The reason for using this was to stay simple and produce a "simple" result that 
    can be used as a jumping off point for later optimization. 
   
    Optimized Code:
    With the optimized code, I attempted the optimization three time.
    
    -Attempt 1: Same as the starting code with the only difference being the input_dim=32 
    
    -Attempt 2: Five layers were used with the first four layers being relu activation and the last layer being sigmoid activation. The increase in layers
                 was an attempt to increase accuracy above 75% but did not work. The activation was kept similar to the previous attempt as to keep things simple
                 and because relu cna help speed up the training. 
    
    -Attemp 3: This is where things changed. Instead of using a similar method as the previous attempts, here I applied a create_model function and used kerastuner
                to make an auto optimization. Five layers were used with an input_dim=28 and min_value=1 and max_value=50 for each iteration and the code ran through 
                relu, tanh, and sigmoid to find the best results. The reason why I used auto optimization for the last attempt was due to how my previous attempts yielded
                little change to accuracy and by applying a code where it optimizes itself I hoped to find one model that could predict higher than 75%. 

-Were you able to achieve the target model performance?

    Starting Code:
    
    Optimized Code:

-What steps did you take to try and increase model performance?

    Starting Code:
    
    Optimized Code: 


Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
