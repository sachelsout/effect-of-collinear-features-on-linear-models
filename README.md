# effect-of-collinear-features-on-linear-models
This repository shows, how linear models behave if the features of the dataset are collinear in nature. Support Vector Machine(SVM) and Logistic Regression(LR) algorithms are used as linear models. Weights and accuracy scores are recorded in different scenarios.
<h1>What are collinear features</h1>

![image](https://user-images.githubusercontent.com/86348193/227203985-b8cd1614-53ae-48da-a77e-55a79aee129a.png) <br>
Collinear features are the features which are correlated with each other. A change in one feature can cause changes in the correlated features as well which is not good. Due to multicollinearity, we cannot interpret feature importances correctly as we can't trust the model's weights/coeffecients. Also, due to presence of collinear features, small change in the data can impact comparatively larger change in the weights of the trained model. Also, multicollinearity does not impact accuracy of the model which can act as a disguise metric to make us believe everything is correct. <br>
<h1>Perturbation test</h1>
Perturbation means adding noise, usually to the training data. This is done to detect the multicollinearity in machine learning. Here in this project, a small gaussian noise is added (mean of 0.01 and variance 0) to the original data and the accuracy, weights/coeffecients are compared with that of original data.<br>
The above process is done for both Logistic Regression and SVM trained models and the results obtained are nearly same for both the linear models. There is no change in accuracy observed (got 1.0 accuracy for original data as well as modified data). But there are changes in the weights of both the models for original data and modified data, which indicates presence of multicollinearity.
