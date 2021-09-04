# Neural_Network_Charity_Analysis

## Project Overview
Alphabet Soup, an organization that provides charity funding has compiled a list of applications from charities, including features/characteristics of the charity,funding amount requested, and whether or not that charity was able to successfully secure funding.

Neural Network Layers (Deep Learning) will be applied to the model to see if any predictive values can be obtained from the dataset. Performance of the models will be compared against multiple settings, such as number of layers, neurons, features, and activation modes.

## Results
### Data Preprocessing
- Target Column: "IS_SUCCESSFUL" as we are trying to determine the liklihood in which charities funding requests are successful
- Feature Columns: (unique count of) 
  <br>![image](https://user-images.githubusercontent.com/79720695/132086020-e29988cb-485a-4981-ba8f-65b5e28e9aee.png)
- Removed Columns: EIN, Name
  - These columns were removed as they were simply names with no categorical value

### Compiling, Training, and Evaluating
#### Initial Model
In the initial model, two layers were used. The number of nuearons first layer contained 2x the number of input features using relu, and the second layer contained half the first layer using sigmoid.
<br>
![image](https://user-images.githubusercontent.com/79720695/132086113-1b2af1fb-f2ca-4ccc-a1a6-1cfd87f01470.png)
![image](https://user-images.githubusercontent.com/79720695/132086107-6df65c31-db4a-4776-a347-4b959eabf044.png)
As seen, the obtained loss and accuracy is 66.9% and 60.5% respectively. Thus, optimizations to the model will be attmpted.

#### Optimization Attempts
Firstly, the number of features were removed, 'APPLICATION_TYPE','CLASSIFICATION','STATUS', were removed fromt he model.

#### Optimization Attempt 1
Next, the neural network structure was also changed from the original. In this attempt, 3 layers were used, and the number of neurons increased from 2x the features to 2.5
<br>
![image](https://user-images.githubusercontent.com/79720695/132086349-d80184ba-0605-41e2-9593-10a47f12c749.png)
![image](https://user-images.githubusercontent.com/79720695/132086355-92762905-02d5-4298-915d-3131fb5479fe.png)

#### Optimization Attempt 2
In this attempt, the number of neurons and layers remained the same as the initial network, however the activation modes in the first layer was changed. 
<br>
![image](https://user-images.githubusercontent.com/79720695/132086432-d00c58ff-fc4b-490a-8ed5-e3c03e425d42.png)
![image](https://user-images.githubusercontent.com/79720695/132086434-0bc30b67-9563-495a-aa2f-841f28f33db2.png)

#### Optimization Attempt 3
In this attempt, the previous attempts were comnbined.
<br>
![image](https://user-images.githubusercontent.com/79720695/132086459-1551817d-1900-4798-b7e4-8f24ebc59214.png)
![image](https://user-images.githubusercontent.com/79720695/132086462-1349bf80-b255-46eb-b43a-d3aedb5dcba9.png)

## Summary
It is seen that Optimization Attempt #1 was most successful by increasing the original accuracy from 60.5% to 65.7%. In this attempt, additional columns deemed not useful were dropped, and the number of neurons were increased. 

It was further seen that as the neural network began to grow in complexity, the worse the model was actually performing.




