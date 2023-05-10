# Neural_Network_Charity_Analysis
## Purpose
To create a neural network model that can aide in predicting the success of charitable donations made to people or organizations. 

## Results
- Data Processing: 
<b>Target: </b>"IS_SUCCESSFUL" variable</p>
<b>Features and others: </b> In the initial deliverable (#2) it was clear the EIN and NAME columns were to be dropped. The other features were to be left alone aside from  any categoricals that needed binning such as CLASSIFCATION and APPLICATION TYPE. I would later on attempt to remove more columns during optimization with little to no improvement.
- Compiling, Training, and Evaluation: 
<b>Initial model: </b> This model contained 2 hidden layers with 80 and 30 neurons, both with a "relu" activation. The output has a "sigmoid" activation. This did not achieve the goal of 75% accuracy. However, this met the requirements of the deliverable as suggested by the "template".</p>
<b>Optimization attempts: </b> </p>
1) I kept all cleaning steps taken in Deliverable #1 and adjusted the neurons to 15 and 20 respectively. After research and viewing the simplicity of the data, I took the less is more approach. The accuracy hung at around <b>72.3%</b> (LINK).</p>
2) In this attempt I added a third hidden layer with 25 neurons and an activation of "tanh". This SLIGHTLY improved the accuracy to just above <b>73%</b> (LINK).
3) In this attempt dropped the ORGANIZATION and STATUS columns, since their data wasn't diverse. I also added a fourth hidden layer with a relu activation and still did not meet the threshold (LINK).
4) I did attempt one more time, this time utilizing the Kerastuner library. We ran through this in class and I wanted to see what results I recieved.  As you can tell it also, did not workout. (LINK)

## Summary
Despite the time and effort, I could not get my model at a 75% accuracy level. I feel like I did exhaust all of my knowledge (while very little, still) of the neural network method and even attempted the tuner method to no avail. In my opinion and after performing research online, this dataset could be best served using a less complex model like RandomForest or another form of machine learning, I also believe that we may simply not have enough data to support a neural network just yet and need to pull in more fields. This could be what is contributing to the accuracy and loss issues.
