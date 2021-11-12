# Challenge-14

## Algo Trading 

We are financial advisors working for a top five financial advisory firm. We are planning on improving our trading algorithms by using different types of machine learning.   

Step 1: Import the OHLCV dataset into a Pandas DataFrame.

Step 2: Generate trading signals using short- and long-window SMA values.

Step 3: Split the data into training and testing datasets.

Step 4: Use the SVC classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. Review the predictions.

Step 5: Review the classification report associated with the SVC model predictions.

Step 6: Create a predictions DataFrame that contains columns for “Predicted” values, “Actual Returns”, and “Strategy Returns”.

Step 7: Create a cumulative return plot that shows the actual returns vs. the strategy returns. Save a PNG image of this plot. This will serve as a baseline against which to compare the effects of tuning the trading algorithm.

Step 8: Write your conclusions about the performance of the baseline trading algorithm in the README.md file that’s associated with your GitHub repository. Support your findings by using the PNG image that you saved in the previous step.

## Tuning the Model

Step 1: Tune the training algorithm by adjusting the size of the training dataset. To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your README.md file. Answer the following question: What impact resulted from increasing or decreasing the training window?

Step 2:  Tune the trading algorithm by adjusting the SMA input features. Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your README.md file. Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?

Step 3: Choose the set of parameters that best improved the trading algorithm returns. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your README.md file.

## Evaluating a new model 

Step 1: Import a new classifier, such as AdaBoost, DecisionTreeClassifier, or LogisticRegression. (For the full list of classifiers, refer to the Supervised learning page (Links to an external site.) in the scikit-learn documentation.)

Step 2: Using the original training data as the baseline model, fit another model with the new classifier.

Step 3: Backtest the new model to evaluate its performance. Save a PNG image of the cumulative product of the actual returns vs. the strategy returns for this updated trading algorithm, and write your conclusions in your README.md file. Answer the following questions: Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?


---

## Technologies
This application is written in Python 3.7  

this application uses the following packages:

Pandas  https://pandas.pydata.org

Pathlib https://docs.python.org/3/library/pathlib.html

Numpy https://numpy.org

Hvplot https://hvplot.holoviz.org/index.html

Matplotlib https://matplotlib.org

Sklearn https://scikit-learn.org/stable/index.html

---

## Installation Guide

Before running the application first install the following dependencies.
See the associated Screenshot for what to Install 

![imports](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/imports%20.jpg)




---

## Evaluation Report

During our evaluation of the current model the following imputs were used.

The first time frame looked at was 3 months.

![original time sample](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/time%20sample%20original.png)

The first set of moving averages looked at where 4 days and 100 days 
![original SMAs](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/SMA%20original.png)

The original classification report shows that the model should be useful with a weighted average of 77 and very high recall and precision in longing and shorting respectively

![original classification report](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/original%20classification%20report%20.png)

While the numbers seem good the performance of this strategy is not desirable as it underperforms 

![original returns graph](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/plotted%20returns.png)

I set out to tune the model to find some better performance.

One of the things I did was to increase the time horizon that was used for testing, from 3 months to 6 months.

This was coupled with adjusting the moving averages used as trading signals. We decided on using a shorter SMA horizon with 14 days being our "Fast" SMA and 30 being our "Slow" SMA 

These changes together produced this classification report which on the surface looks worse than the original classification report with a whole 20 points lower on weighted average and much worse recall and precision.

![new classification report](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/New%20classifciation%20report.png)

Despite this the returns were much better and outperformed. As this new model outperformed on nearly all times frames, I believe that changing the moving averages had a greater effect than increasing the time period that we looked at originally  

![new plotted returns](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/new%20plotted%20returns.png)

Another model was used on the original time frame and original moving averages to see if more performance could be gained. I used Logisitic Regression to see if that created any improvements. 

While the classification report showed a lower weighted average than the previous model with time frame changes, we have seen that better weighted average does not guarantee better trading results 

![logisitic regression classfication report](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/lr%20classifcation%20report.png)

But this model is no good. It lags actual returns to such an extent, I am of the opinion that logistic regression is not suitable for a trading algorithms

![lr returns plotted ](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/new%20model%20graph.png)


### Conclusions 

I would appear that Support Vector Machine (SVM) learning is suitable for putting together a trading strategy. 

The updated model appears to work well enough, that it should be fitted to other assets to see what sort of performance gains could be found. 

It would also be useful to look at the returns of the model over a very long time horizon to see how well it does. 

During a 6 month timeframe the new 14 and 30 SMA SVM is a winning trading algo.


---

## Usage

To use the data simply clone the repository. This can also be used via Google Collab but I chose jupyter notebook 

Different layers could be added as well ad different values of the layers 
```
---

## Contributors

Sean Patel (myself) seanpatel076@gmail.com
---

## License

License is public anyone can use or make changes to this application
