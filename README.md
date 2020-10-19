# Background Statement

Breast cancer is the most common cancer in women worldwide and the second most common cancer overall. It is a leading cause of cancer death in less developed countries and the second leading cause of cancer death in American women, exceeded only by lung cancer. In 2018, nearly 2 million new breast cancer cases were diagnosed. It is the most frequently diagnosed cancer among women in 140 of 184 countries worldwide.

Globally, breast cancer now represents one in four of all cancers in women. Since 2008, worldwide breast cancer incidence has increased by more than 20 percent. Mortality has increased by 14 percent. ​According to the World Cancer Research Fund International, Breast Cancer is the most common cancer for women in the U.S after skin cancer.  In the U.S. in 2020, it is estimated that 42,690 breast cancer deaths (42,170 women, 520 men) will occur.

Source: https://www.bcrf.org


It is estimated that in 2020:

- 27,400 women will be diagnosed with breast cancer. This represents 25% of all new cancer cases in women in 2020.
- 5,100 women will die from breast cancer. This represents 13% of all cancer deaths in women in 2020.
- On average, 75 Canadian women will be diagnosed with breast cancer every day.
- On average, 14 Canadian women will die from breast cancer every day.
- 40 men will be diagnosed with breast cancer and 55 will die from breast cancer.

Source: https://www.cancer.ca/en/cancer-information/cancer-type/breast/statistics/?region=on


# Problem Statement
The key challenge in cancer detection is how to classify tumors into malignant or benign using machine learning. Early diagnosis can significantly increases the chances of survival of Breast cancer patient. Machine learning techniques can dramatically improves the accuracy of diagnosis. Research indicates that most experienced physicians can diagnose cancer with 79 percent accuracy while 91 percent correct diagnosis is achieved using machine learning techniques.


In this case study, the task is to classify tumors into malignant or benign tumors using features from several cell images. 30 features are used, examples:
- radius (mean of distances from center to points on the perimeter)
- texture (standard deviation of gray-scale values)
- perimeter
- area
- smoothness (local variation in radius lengths)
- compactness (perimeter^2 / area - 1.0)
- concavity (severity of concave portions of the contour)
- concave points (number of concave portions of the contour)
- symmetry 
- fractal dimension ("coastline approximation" - 1)

The datasets are linearly separable using all 30 input features
- Number of Instances: 569
- Class Distribution: 212 Malignant, 357 Benign
- Target class:
    - Malignant
    - Benign


https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)


The following steps are followed for the data analysis and Prediction:
- Step 1: Import Libraries and datasets
- Step 2: EDA - Explore/Visualize Dataset
- Step 3: Prepare the data for training
- Step 4: Model Training 
- Step 5: Model Testing
- Step 6: Model Accuracy
- Step 7: Further Improvement of Model

![Image1](https://github.com/mayorofdata/Breast-Cancer-Classification-using-Support-Vector-Machine/blob/main/bc1.PNG)

# The model is created using Support Vector Machine
- A Support Vector Machine is a supervised algorithm that can classify cases by finding a separator.

- SVM works by mapping data to a high-dimensional feature space so that data points can be categorized,
even when the data are not otherwise linearly separable.
Then, a separator is estimated for the data.
The data should be transformed in such a way that a separator could be drawn as a hyperplane.

- Basically, mapping data into a higher dimensional space is called kernelling. The mathematical function used for the transformation is known as the kernel function, and can be of different types, such as: Linear, Polynomial, Radial basis function (or RBF), and Sigmoid.

- Each of these functions has its own characteristics, its pros and cons, and its equation, but the
good news is that you don’t need to know them, as most of them are already implemented in libraries of data science programming languages.

- The hyperplane is learned from training data using an optimization procedure that maximizes the margin; and like many other problems, this optimization problem can also be solved by gradient descent. You can make classifications using this estimated line. It is enough to plug in input values into the line equation, then, you can calculate whether an unknown point is above or below the line.
- If the equation returns a value greater than 0, then the point belongs to the first class, which is above the line, and vice versa.
- The two main advantages of support vector machines are that they’re accurate in high dimensional spaces; and, they use a subset of training points in the decision function (called support vectors), so it’s also memory efficient.
- The disadvantages of support vector machines include the fact that the algorithm is prone for over-fitting, if the number of features is much greater than the number of samples. Also, SVMs do not directly provide probability estimates, which are desirable in most classification
problems. In addition, SVMs are not very efficient computationally, if your dataset is very big, such as when
you have more than one thousand rows.
- SVM is good for image analysis tasks, such as image classification and handwritten digit recognition. Also SVM is very effective in text-mining tasks, particularly due to its effectiveness in dealing with high-dimensional data. For example, it is used for detecting spam, text category assignment, and sentiment analysis. Another application of SVM is in Gene Expression data classification, again, because of its power in high dimensional data classification. SVM can also be used for other types of machine learning problems, such as regression, outlier detection, and clustering.

![Image2](https://github.com/mayorofdata/Breast-Cancer-Classification-using-Support-Vector-Machine/blob/main/svm.PNG)

# Conclusion
Machine learning techniques(SVM) was able to classify tumors effectively into malignant and benign tumors with 99 percent accuracy. The technique can rapidly evaluate breast masses and classify them in an automated fashion.

Early breast cancer detection can dramatically save lives especially in the developing world. This technique can further improved by combining computer vision and machine learning and deep learning techniques to classify cancer directly using tissue images.



