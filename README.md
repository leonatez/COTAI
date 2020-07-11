| **Title**      | Home Credit Default Risk|
| ---------- |-------------------|
| **Team**       | Nguyễn Hải Linh - hailinh.leo@gmail.com
| **Predicting** | Predicting Default Risk of loan application, based on Home Credit dataset (it's a Kaggle Competition)
| **Data**       | I got data from Kaggle Competition, hosted by Home Credit. The dataset includes many csv files from many tables of their database, but for the purpose of making final project for ML course, plus the limitation in time and hardware, I took only 1 table for this practical essay: application.csv
| **Features**   | There are 122 features, which are raw input data. I created 4 more fields: train-error-mean, train-error-std, train-error-mean, test-error-std to measure the feature importance, then based on that reduced the dimension to only 49.
| **Models**     | I mainly use XGBoost: ∑𝑗=1𝑇[(∑𝑖∈𝐼𝑗𝑔𝑖)𝑤𝑗+12(∑𝑖∈𝐼𝑗ℎ𝑖+𝜆)𝑤2𝑗]+𝛾𝑇, which is believed to be one of the best model for controlling overfitting. I added cross-validation function: k-fold to utilise the power of XGBoost.
| **Results**    | 
|                | XGB training set 150679.000
|                | XGB test set 92254.000
|                | XGB auc score 0.748
|                | MLP training set 150679.000
|                | MLP test set 92254.000
|                | MLP auc score 0.605
| **Discussion** | Decision tree algorithsm is the best for making scoring model. Besides the accuracy / auc metrics that could be maximised by boosted trees (in this project is XGBoost), we can also clearly see feature importance, which is more difficult to find in other modern model like MLP. In financial institution, data is money. With feature importance, we can save a lot by reducing expense on buying personal data, optimise customer experience (less fields in loan application) and save cost for computing.
| **Future**     | There are still 5 more tables that haven't been exploited this time, due to limitation of time. There other tables will require more data processing skills, which could increase the auc score a little bit (based on other's result on Kaggle).
|**References**  | https://www.kaggle.com/c/home-credit-default-risk/overview/description
