# Cross_Sell_Prediction
## JantaHack Cross Sell Prediction  using CatBoost Classifier Model

### LB - https://datahack.analyticsvidhya.com/contest/janatahack-cross-sell-prediction/#LeaderBoard
#### Public Rank - 72 (0.8584736363)
#### Private Rank - 58 (0.8632359852)
#### Kaggle - https://www.kaggle.com/ullaskm/cross-sell-prediction-using-catboost-classifier

### Problem Statement
Your client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.
For example, you may pay a premium of Rs. 5000 each year for a health insurance cover of Rs. 200,000/- so that if, God forbid, you fall ill and need to be hospitalised in that year, the insurance provider company will bear the cost of hospitalisation etc. for upto Rs. 200,000. Now if you are wondering how can company bear such high hospitalisation cost when it charges a premium of only Rs. 5000/-, that is where the concept of probabilities comes in picture. For example, like you, there may be 100 customers who would be paying a premium of Rs. 5000 every year, but only a few of them (say 2-3) would get hospitalised that year and not everyone. This way everyone shares the risk of everyone else.

Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.
Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code type), Vehicles (Vehicle Age, Damage), Policy (Premium, sourcing channel) etc.

### Model approach
1) it is a binary classification problem to predict whether the customer is interested in Vehicle insurance or not.
2) Data had more categorical features than numerical features which were encoded using label encoder.
3) firstly tried with LGBM classifier which resulted only 83.2 AUC Score.
4) Therefore it was obivious to select Catboost classifier which deals categorical features better without even required to preprocessing.
5) By hyperparameter tuning with max_depth,l2 regularizer and learning rate it was possible to achieve the maximum AUC score and minimize Logloss.
