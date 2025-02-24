# Machine Learning Project Report - Muhammad Adin Palimbani
>### ***"Breast Tumor Prediction and Diagnosis Using Logistic Regression, Neural Network and Support Vector Machine Algorithms"*** - Predictive Analytics

<img src="https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/blob/02935c3aedf355fbce58e95d36dfaf547f90fab5/images/Histology-of-left-breast-cancer-The-tumor-is-composed-of-large-nests-with-central-comedo.png" width="490"/> <img src="https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/de1f9259-51cd-4e2f-afe1-9a1e9e55dbdf" width="320"/> 

## Project Domain 
1. Issue Focus? <br>
The significant advances in cancer research over the past decades has been carried out with the advent of new technologies in the field of medicine. Scientists have conducted a new approach with different methods for the early prediction of cancer treatment outcome particularly Breast Cancer. One of the example approaches applied is the growing trend on Machine Learning Techniques. However, a common problem in several research is the lack of external validation or testing regarding the predictive performance of their models and also handling imbalanced data.  This may lead to malformed prediction models and system failures at the production stage

2. Why does the issue need to be resolved? <br>
The accurate prediction models of a disease outcome is extremely depends on the medical data of the patient. Medical data contains the patient's details condition and diagnosis which hold unnecessary and interrelated data. Those data is high dimensional data as well in particular the integration of clinical and genomic mixed data. In several studies, scientists have proved that approaches related to the genomic characteristics provides promising results for cancer detection and identification, for instances, digitized image of a fine needle aspirate (FNA) of a breast mass which represent cell nuclear characteristics in Breast Tumor. However, these methods suffer from low sensitivity regarding their use in screening at early stages and difficulty to determine benign from malignant tumors. This is the reason why the cancer predictive performance models issue need to be resolved in order to prevent malformed prediction and system failures. 

3. How to address the issue? <br>
Interactive image processing techniques, along with a linear programming based inductive classifier, have been used to creeate a highly accurate system for diagnosis of Breast Tumors. A small fraction of a Fine Needle Aspirate Slide (FNA) is selected and digitized. The digitized image of a FNA of a Breast mass describe chracteristics of the cell nuclei present in the image. Those are computed and become features for this research. So we could possibily diagnosed whether it is Malignant or Benign through Nuclear Feature Extraction.

4. Related Research References from Credible Sources: <br> 
[Nuclear Feature Extraction For Breast Tumor Diagnosis](https://minds.wisconsin.edu/bitstream/handle/1793/59692/TR1131.pdf;jsessionid=0449D8C1D78CAAB2BF57B76AABE87312?sequence=1). <br>
[Prediction of parameters of liver tumor using feature extraction and supervised function](https://www.sciencedirect.com/science/article/pii/S2665917422000204). <br>
[Machine Learning Algorithms For Breast Cancer Prediction And Diagnosis](https://www.sciencedirect.com/science/article/pii/S1877050921014629). <br>
[Quantitative nuclear phenotype signatures predict nodal disease in oral squamous cell carcinoma](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8568158/). <br>

## Business Understanding
Breast Tumor Diagnosis has been conducted by [Fine Needle Aspiration (FNA)](https://cancer.ca/en/treatments/tests-and-procedures/fine-needle-aspiration-fna); a type of biopsy which uses a very thin needle and syringe to remove a sample of cells, tissue or fluid from an abnormal area or lump in the body. FNAs has been able to diagnose successfully in examining the cell nuclear phenotypes and become a features which indicates a higher likelihood of malignancy. The computer vision diagnostics system extracts 10 different features from the snake-generated cell nuclei boundaries. Those extracted features are numerically modeled which consist of ***Radius***, ***Perimeter***, ***Area***, ***Compactness***, ***Smoothness***, ***concavity***, ***Concave Points***, ***Symmetry***, ***Fratal Dimension*** and ***Texture***. In addition, there is a diagnosis breast tumor features which represent a malignant or bening so in this project there is a target labelled to predict whether it is a benign or malignant tumor. A Supervised Machine Learning model is suitable for solving this issue by using the quantitative cell nuclear phenotypes of Breast Tumor and followed by handling imbalanced data.

### Problem Statement
1. Does each feature in this dataset have an influence on breast tumor prediction model?
2. Which Machine Learning model present the best prediction model and could solve the issue?
3. How does handling imbalanced data give an affect to prediction model?

### Goals
1. Find features that have an influential on breast tumor prediction
2. Find the best Machine Learning Model that could possibly solve the problem
3. Find the affect of SMOTE in handling imbalanced data for model prediction

### Solution Statements
To reach out good Breast Cancer Prediction, using 3 different type of Binary Classification model for predicting whether the diagnosis is benign (0) or malignant (1) in Supervised Machine Learning Algorithms. Those algorithms are suitable for predicting one of two possible outcomes. In addtion, SMOTE will be implemented as well for handling imbalanced data. The algorithms for binary classification are as follows: <br>

- [Binary Logistic Regression](https://www.datascienceinstitute.net/blog/binary-logistic-regression-an-introduction#:~:text=Binary%20logistic%20regression%20models%20the,or%20presence%20and%20so%20on.) <br>
Binary Logistic Regression is the relationship between a set of independent variables; categorical or continous, and a binary dependent variables; like benign or malignant, deadth or survival, so on and so forth. Logistic regression is commonly used for classification issues which predict the values of target labelled 0 or 1. The logistic regression curve is a sigmoid curve. Common performance metrics to evaluate a binary classification model is Confusion metrics, accuracy score; ratios of correct predictions, Precision; proportion of the posivtive predictions is actual positive, Sensitivity (recall); the higher the recall score, the better the ML model is at identifying positives, Specificity; correctly predict the negatives out of actual negatives, F-Score(F1-Score);combine the precision and recall. In medical diagnosis, anything that doesn’t account for false negatives is serious, so [recall score](https://medium.com/javarevisited/evaluating-the-logistic-regression-ae2decf42d61) is a better measure than precision in this case.

- [Neural Network](https://medium.com/afblabs-data-science/a-simple-neural-networks-for-binary-classification-understanding-feed-forward-68c3c0659f78) <br>
Neural network is a simplistic form network to classify as well regress the input variable data so as to match the actual variable, referred as y or target variable. The predicted value is then improved over many iterations called epochs by computing and minimizing the error loss. There are 3 different layers in Neural Network; input layer, hidden layer and output layer. In neural network, Keras library is commonly used in Deep Learning models. For binary classification using Neural Network, Loss Function used is Binary Crossentrophy and Activation Function type is Sigmoid. Performance Metrics Evaluaion for Binary classification in Neural Network is [Accuracy](https://towardsdatascience.com/the-explanation-you-need-on-binary-classification-metrics-321d280b590f). 

- [Support Vector Machine](https://medium.com/@24littledino/support-vector-machine-svm-in-python-fc3a4ffd25b6) <br>
Support Vector Machine is a set of Supervised Learning Methods used for Binary classification problem, regression and outliers detection.In particular, SVM Projects data to higher dimension, finds the optimal hyperplane that can maximize the soft margin, and uses that hyperplane as a threshold to classify new data points. To evaluate SVM models for classification tasks, it's more appropriate to use classification-specific metrics such as accuracy, precision, recall, F1-score, and area under the ROC curve (ROC-AUC). These metrics provide insights into the SVM model's ability to classify instances correctly across different classes and account for the inherent characteristics of classification tasks.

## Data Understanding
Dataset used are collected from Kaggle. It is [Breast Cancer Wisconsin (Diagnostic) Dataset](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data/code). Dataset is in CSV File Format which total class contribution are 357 Benign and 212 Malignant. Dataset is consist of 569 rows and 33 Features; 1 Categorical Features and 32 Numerical Features. One Categorical Features will be converted into Binary Integer as Target Labelled. Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image. All feature values are recorded with four significant digits and none missing values. The extracted features are as follows: <br>
1. ***Radius***: The radius of and individual nucleaus is measured by averaging the length of the radial line segments defined by the centeroid of the snake and the individual snake points.
2. ***Perimeter***: The total distance between the snake point constitues the nuclear perimeter.
3. ***Area***: Nuclear area is measured simply by counting the number of pixels on the interior of the snake and adding one-hald of the pixels in the perimeter.
4. ***Compactness***: Perimeter and area are combined to give a measure of the compactness of the cell nuclei using the formula perimeter<sup>2</sup>/area.
5. ***Smoothness***: Quantified by measuring the difference between the length of a radial line and the mean length of the lines surrounding it.
6. ***Concavity***: Severity of concave portions of the contour
7. ***Concave points***: Number of concave portions of the contour
8. ***Symmetry***: In order to measure symmetry, the major axis, or longest chord through the center, is found.
9. ***Fractal Dimension***: Approximated using the "Coastline Approximation" described by Mandelbrot.
10. ***Texture***: meaasured by finding the variance of the gray scale intensities in the component pixels.<br>
11. ***Diagnostic***: Benign and Malignant

>Additional Notes:
>_mean, _se (standar error) and _worst (largest): mean of the 3 largest values of these features were computed for each image, resulting in 30 features. For instance: field 3 is mean radius, field 13 is radius_se, field 23 is worst radius.

 . | radius_mean | radius_se | radius_worst | 
 --- | --- | --- | --- | 
Definition | mean of distances from center to points on the perimeter | standard error for the mean of distances from center to points on the perimeter | "worst" or largest mean value for mean of distances from center to points on the perimeter | 
Values | 17.99 | 1.095| 25.38 | 

### Exploratory Data Analysis and Visualization
#### Check Data Type
```ruby
df.info()
```
![df info](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/34570f7b-7e16-414e-89f6-0599f85d0f78)

#### Check Missing Values
```ruby
print(df.isna().sum())
```
![df isna](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/e14838d5-5672-4119-95dd-fd14397d81d0)

#### Check Data Duplication
```ruby
print("Jumlah yang terduplikasi:", df.duplicated().sum())
```
![df duplicated](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/78819fb9-3ed0-47f7-97fa-da9328168a27)

#### Descriptive Statistics Analysis
```ruby
df.describe()
```
![df describe](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/9b0f5c49-5927-4b31-adad-21dcd35e6f67)

#### Check Outliers
Four Example Features used to Check Outliers:
```ruby
sns.boxplot(x=df['radius_mean'])
sns.boxplot(x=df['texture_mean'])
sns.boxplot(x=df['perimeter_mean'])
sns.boxplot(x=df['area_mean'])
```
| radius_mean | texture_mean | perimeter mean | area mean |
| :---: | :---: | :---: | :---: | 
| ![radius mean](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/319ae8e9-47d5-46df-b475-69291e915794)  | ![texture mean](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/2b529395-c8a8-4c5d-8dd4-68ab9de92e6a) |  ![perimeter mean](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/e3edbf37-30f9-4cca-88b8-06df171c8002)  | ![area mean](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/cac1e7b7-c579-4d9a-b860-67c326c7a144) |

#### Univariate Analysis
```ruby
df.hist(bins=50, figsize=(20,15))
plt.show()
```
![univariate analysis](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/ac1b6f89-6e0e-4a0f-a564-19ed276c37bc)

#### Multivariate Analysis
```ruby
# Observe relation among numerical features using pairplot() 
sns.pairplot(df, diag_kind = 'kde')
```
![pairplot](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/0b1edff5-93de-4089-8fdc-1fe13e92836f)

```ruby
plt.figure(figsize=(20, 18))
correlation_matrix = df.corr().round(2)
# parameter anot=true is used for printing value inside the box
sns.heatmap(data=correlation_matrix, annot=True, cmap='coolwarm', linewidths= 0.5, )
plt.title("Correlation Matrix untuk Fitur Numerik ", size=20)
```
![multivariate](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/06078f33-9f1a-4f04-849f-90fb6d9e97de)

## Data Preparation
At this stage, PCA feaures reduction, change target labelled type into binary integer, IQR Method, SMOTE and Feature Scalling are approriate techniques for this type of dataset. Moreover, the class contribution in dataset are indeed imbalanced; 357 Benign and 212 Malignant so SMOTE or Synthetic Minority Over-sampling Technique will be implemented. Removing outliers will be performed as well and followed by feature scaling or z-score normalization where they have a mean of 0 and a standard deviation of 1. The data size will be splitted into train set and test set with ratio 80:20. To understand deeply the ins and outs of data preparation is by looking at these several steps: <br>

1. Convert "Diagnosis" Feature "object" type into "binary integer" values 0 and 1.
>Why is it necessary for this technique to be carried out?
>>Answer: require input features to be numerical so the algorithms can be performed.
```ruby
df['diagnosis']=df['diagnosis'].map({'M':1,'B':0})
```
<img src="https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/a29b20da-b0f5-4b34-b066-2c2ed1e285d9"/> <img src="https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/89166fd5-dce2-499c-8a6d-3909cafa9db2"/> 

2. Remove outliers using IQR Method in all Features. Then, check data shape.
>Why is it necessary for this IQR Method to be carried out?
>>Answer: outliers can increase variance in the dataset and the Interquartile Range (IQR) method is a robust and commonly used technique for detecting and removing outliers as well. 
```ruby
Q1 = df_baru.quantile(0.25)
Q3 = df_baru.quantile(0.75)
IQR=Q3-Q1
df_baru=df_baru[~((df_baru<(Q1-1.5*IQR))|(df_baru>(Q3+1.5*IQR))).any(axis=1)]

# Check data shape after dropping outliers
df_baru.shape
```
![data shape after drop outliers](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/26534822-5f9f-451a-9efe-cbccc9b7c3eb) <br>
The dataset has been cleaned and has 398 samples

3. Reduce dimension of radius_mean, perimeter_mean, area_mean, radius_worst, perimeter_worst and area_worst feature using PCA
>Why is it necessary for reducing those features using PCA to be carried out?
>>Answer: The pairplot result shows those six features have a high correlation so they can be reduced using PCA which help to reduce noise and redundancy in dataset.
```ruby
from sklearn.decomposition import PCA
pca = PCA(n_components=1, random_state=123)
pca.fit(df_baru[['radius_mean', 'perimeter_mean', 'area_mean', 'radius_worst', 'perimeter_worst', 'area_worst']])
df_baru['dimension'] = pca.transform(df_baru.loc[:, ('radius_mean', 'perimeter_mean', 'area_mean', 'radius_worst', 'perimeter_worst', 'area_worst')]).flatten()
df_baru.drop(['radius_mean', 'perimeter_mean', 'area_mean', 'radius_worst', 'perimeter_worst', 'area_worst'], axis=1, inplace=True)
df_baru
```
![dimension](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/bf28fcf9-1c18-4ecd-8284-fd15c807384a)

4. Splitting Data into Train Set and Test Set + SMOTE For imbalanced data
>Why is it necessary for handling imbalanced data using SMOTE to be carried out?
>>Answer: To maximize overall accuracy and minimize MSE which can be misleading when classes are imbalanced and SMOTE (Synthetic Minority Over-sampling Technique) is one of the method used to address this issue.
```ruby
pip install imbalanced-learn
```
```ruby
from sklearn.model_selection import train_test_split
from imblearn.over_sampling import SMOTE

# Assuming X contains your features and y contains the corresponding labels
# Perform train-test split

X = df.drop(["diagnosis"],axis =1)
y = df["diagnosis"]
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Apply SMOTE only on the training data
smote = SMOTE(random_state=42)
X_train_resampled, y_train_resampled = smote.fit_resample(X_train, y_train)

# Now, X_train_resampled and y_train_resampled contain the resampled data using SMOTE,
# while X_test and y_test remain unchanged

# Proceed with model training and evaluation using the resampled training data and the original test data

# Count the number of samples in each class before and after SMOTE
unique_train, counts_train = np.unique(y_train, return_counts=True)
unique_train_resampled, counts_train_resampled = np.unique(y_train_resampled, return_counts=True)

# Create a DataFrame to display the results
data = {
    'Class': unique_train,
    'Original Count': counts_train,
    'Resampled Count': counts_train_resampled
}

df_result = pd.DataFrame(data)
print("Before SMOTE:")
print(df_result)

# Visualize the distribution of classes after SMOTE
print("\nAfter SMOTE:")
print("Classes:", unique_train_resampled)
print("Counts:", counts_train_resampled)
```
![output smote](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/0c0b9474-ad9f-4f9a-9482-8648a8642ae4)

5. Feature Scalling using Z-Score Normalization
>Why is it necessary for feature scalling to be carried out?
>>Answer: To ensures all features have a similar scale, typically between 0 and 1 or around a mean of 0 with a standard deviation of 1. 
```ruby
scaler = StandardScaler()
scaler.fit(X_train[numerical_features])
X_train[numerical_features] = scaler.transform(X_train.loc[:, numerical_features])
X_train[numerical_features].head()
X_train[numerical_features].describe().round(4)
```
![standarisation](https://github.com/adinplb/Belajar-Machien-Learning-Terapan-Dicoding/assets/61041719/ed2b1602-7ea1-4089-a6ed-c9d7c9037585)


## Modelling
To solve this Binary Classification of Medical Diagnosis issue, implementing Logistic Regression, Neural Network and Support Vector Machine Algorithms are the most appropriate model in classifying whether it is Benign (0) or Malignant (1) and having a great accuracy for predictions. The following is an explanation of each stage in each algorithms:
- [Logistic Regression Model:](https://medium.com/@akshayjain_757396/advantages-and-disadvantages-of-logistic-regression-in-machine-learning-a6a247e42b20) <br>
  Step 1. Import library <br>
  ```ruby
  from sklearn.linear_model import LogisticRegression
  from sklearn.metrics import classification_report, confusion_matrix
  from imblearn.over_sampling import SMOTE
  from sklearn.preprocessing import StandardScaler
  ```
  Step 2. Scale features (optional but often recommended)
  ```ruby
  scaler = StandardScaler()
  X_train_resampled_scaled = scaler.fit_transform(X_train_resampled)
  X_test_scaled = scaler.transform(X_test)
  ```
  Step 3. Initialize and train logistic regression model before SMOTE <br>
  ```ruby
  log_reg_before_smote = LogisticRegression()
  log_reg_before_smote.fit(X_train, y_train)
  ```
  Step 4. Make predictions on the test set before SMOTE <br>
  ```ruby
  y_pred_before_smote = log_reg_before_smote.predict(X_test)
  ```
  Step 5. Evaluate performance before SMOTE
  ```ruby
  print("Performance before SMOTE:")
  print(confusion_matrix(y_test, y_pred_before_smote))
  print(classification_report(y_test, y_pred_before_smote))
  ```

  ![LogReg_Before Smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/73a0b293-33a1-4855-ac9b-577a2adc33ac)

  Step 6. Initialize and train logistic regression model after SMOTE <br>
  ```ruby
  log_reg_after_smote = LogisticRegression()
  log_reg_after_smote.fit(X_train_resampled_scaled, y_train_resampled)
  ```
  Step 7. Make predictions on the test set after SMOTE
  ```ruby
  y_pred_after_smote = log_reg_after_smote.predict(X_test_scaled)
  ```
  Step 8. Evaluate performance after SMOTE
  ```ruby
  print("Performance after SMOTE:")
  print(confusion_matrix(y_test, y_pred_after_smote))
  print(classification_report(y_test, y_pred_after_smote))
  ```
  ![LogReg_After Smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/77ddc2a4-4a7c-43eb-8046-0a56a6caa393)

  Step 9. Plot Confusion Metrics Before and After SMOTE
  ```ruby
  # Compute confusion matrices before and after SMOTE
  confusion_matrix_before_smote = confusion_matrix(y_test, y_pred_before_smote)
  confusion_matrix_after_smote = confusion_matrix(y_test, y_pred_after_smote)

  # Plot confusion matrices
  fig, axes = plt.subplots(1, 2, figsize=(12, 6))

  # Plot confusion matrix before SMOTE
  axes[0].imshow(confusion_matrix_before_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[0].set_title('Confusion Matrix Before SMOTE')
  axes[0].set_xticks([0, 1])
  axes[0].set_yticks([0, 1])
  axes[0].set_xlabel('Predicted Label')
  axes[0].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[0].text(j, i, str(confusion_matrix_before_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center',   color='white')

  # Plot confusion matrix after SMOTE
  axes[1].imshow(confusion_matrix_after_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[1].set_title('Confusion Matrix After SMOTE')
  axes[1].set_xticks([0, 1])
  axes[1].set_yticks([0, 1])
  axes[1].set_xlabel('Predicted Label')
  axes[1].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[1].text(j, i, str(confusion_matrix_after_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center', color='white')

  plt.tight_layout()
  plt.show()
  ```

  ![LogReg Confusion Before and After smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/1d373926-f9db-4916-974a-127d1dd8c834)

  Step 10. Plot Accuracy Before and After SMOTE
  ```ruby
  # Get classification reports before and after SMOTE
  classification_report_before_smote = classification_report(y_test, y_pred_before_smote, output_dict=True)
  classification_report_after_smote = classification_report(y_test, y_pred_after_smote, output_dict=True)

  # Extract accuracy values
  accuracy_before_smote = classification_report_before_smote['accuracy']
  accuracy_after_smote = classification_report_after_smote['accuracy']

  # Plot accuracy before and after SMOTE
  labels = ['Before SMOTE', 'After SMOTE']
  accuracy_scores = [accuracy_before_smote, accuracy_after_smote]

  plt.bar(labels, accuracy_scores, color=['blue', 'green'])
  plt.xlabel('SMOTE')
  plt.ylabel('Accuracy')
  plt.title('Accuracy of Logistic Regression before and after SMOTE')
  plt.ylim(0, 1)  # Limit y-axis from 0 to 1 for accuracy range
  plt.show()
  ```
  ![LogReg_Accuracy_Before and after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/63740f0e-86f4-433d-bc0c-3cb69da4c3bf)

  > Advantages: <br>
  >> - Logistic Regression performs well when the dataset is linearly separable <br>
  >> - Logistic Regression not only gives a measure of how relevant a predictor (coefficient size) is, but also its direction of association (positive or negative) <br>
  
  > Disadvantages: <br>
  >> - Main limitation of Logistic Regression is the assumption of linearity between the   dependent variable and the independent variables <br>
  >> - If the number of observations are lesser than the number of features, Logistic Regression should not be used, otherwise it may lead to overfit  <br>



- [Neural Network Model](https://subscription.packtpub.com/book/data/9781788397872/1/ch01lvl1sec27/pros-and-cons-of-neural-networks): <br>
  Step 1. Import library <br>
  ```ruby
  from tensorflow.keras.models import Sequential
  from tensorflow.keras.layers import Dense
  ```
  Step 2. Scale features (optional but often recommended)
  ```ruby
  scaler = StandardScaler()
  X_train_resampled_scaled = scaler.fit_transform(X_train_resampled)
  X_test_scaled = scaler.transform(X_test)
  ```
  Step 3. Define the neural network model architecture before SMOTE <br>
  ```ruby
  lmodel_before_smote = Sequential([
    Dense(128, activation='relu', input_shape=(X_train.shape[1],)),
    Dense(64, activation='relu'),
    Dense(32, activation='relu'),
    Dense(1, activation='sigmoid')
  ])
  ```
  Step 4. Compile the model <br>
  ```ruby
  model_before_smote.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
  ```
  Step 5. Train the model before SMOTE
  ```ruby
  model_before_smote.fit(X_train, y_train, epochs=10, batch_size=32, verbose=1)
  ```
  Step 6. Make predictions on the test set before SMOTE <br>
  ```ruby
  y_pred_before_smote = (model_before_smote.predict(X_test) > 0.5).astype("int32")
  ```
  Step 7. Compute and print confusion matrix and classification report before SMOTE
  ```ruby
  print("Confusion Matrix and Classification Report before SMOTE:")
  print(confusion_matrix(y_test, y_pred_before_smote))
  print(classification_report(y_test, y_pred_before_smote))
  ```
  ![NN_Before Smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/b5dbe9b3-47b7-438a-bd50-7aa594a65a3e)

  Step 8. Define the neural network model architecture after SMOTE
  ```ruby
  model_after_smote = Sequential([
    Dense(128, activation='relu', input_shape=(X_train_resampled_scaled.shape[1],)),
    Dense(64, activation='relu'),
    Dense(32, activation='relu'),
    Dense(1, activation='sigmoid')
  ])
  ```

  Step 9. Compile the model
  ```ruby
  model_after_smote.compile(optimizer='adam', loss='binary_crossentropy', metrics= ['accuracy'])
  ```

  Step 10. Train the model after SMOTE
  ```ruby
  history_smote = model_after_smote.fit(X_train_resampled_scaled, y_train_resampled, epochs=10, batch_size=32, verbose=1)
  ```

  Step 11. Make predictions on the test set after SMOTE
  ```ruby
  y_pred_after_smote = (model_after_smote.predict(X_test_scaled) > 0.5).astype("int32")
  ```

  Step 12. Compute and print confusion matrix and classification report after SMOTE
  ```ruby
  print("Confusion Matrix and Classification Report after SMOTE:")
  print(confusion_matrix(y_test, y_pred_after_smote))
  print(classification_report(y_test, y_pred_after_smote))
  ```

  ![NN After Smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/5dbf196c-9751-43e7-a87c-e7541b3d0b12)


  Step 13. Plot confusion matrix before and after SMOTE
  ```ruby
  # Plot confusion matrix before SMOTE
  axes[0].imshow(confusion_matrix_before_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[0].set_title('Confusion Matrix Before SMOTE')
  axes[0].set_xticks([0, 1])
  axes[0].set_yticks([0, 1])
  axes[0].set_xlabel('Predicted Label')
  axes[0].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[0].text(j, i, str(confusion_matrix_before_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center', color='white')

  # Plot confusion matrix after SMOTE
  axes[1].imshow(confusion_matrix_after_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[1].set_title('Confusion Matrix After SMOTE')
  axes[1].set_xticks([0, 1])
  axes[1].set_yticks([0, 1])
  axes[1].set_xlabel('Predicted Label')
  axes[1].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[1].text(j, i, str(confusion_matrix_after_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center', color='white')

  plt.tight_layout()
  plt.show()
  ```

  ![NN_ConfusionMetrics](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/436f2328-888d-4abd-8ed2-397e03db62ca)


  Step 14. Plot Accuracy Before and After SMOTE
  ```ruby
  # Plot accuracy before and after SMOTE
  plt.plot(history_original.history['accuracy'], label='Original Dataset')
  plt.plot(history_smote.history['accuracy'], label='After SMOTE')
  plt.xlabel('Epochs')
  plt.ylabel('Accuracy')
  plt.title('Accuracy of Neural Network before and after SMOTE')
  plt.legend()
  plt.show()
  ```
  | Plot Accuracy 1 | Plot Accuracy 2 | 
  | :---: | :---: | 
  | ![NN_Accuracy Before after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/d88fa925-694f-47bf-a0f3-5edd86021790) | ![NN_Diagram Accuracy before after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/d7b4fb46-431c-46a7-9e85-fcd8128b0999) | 

  > Advantages: <br>
  >> - Neural Network can be trained with any number of inputs and layers <br>
  >> - Neural networks work best with more data points
  >> - One trained, the predictions are pretty fast
  
  >  Disadvantages: <br>
  >> - Neural networks are black boxes, meaning we cannot know how each independent variable is influencing the dependent variables <br>
  >> - It is computationally very expensive and time consuming to train with traditional CPUs  <br>
  >> - Neural networks depend a lot on training data





- [Support Vector Machine Model:](https://scikit-learn.org/stable/modules/svm.html) <br>
  Step 1. Import library <br>
  ```ruby
  from sklearn.svm import SVC
  ```
  Step 2. Initialize SVM classifier before SMOTE
  ```ruby
  svm_classifier_before_smote = SVC(kernel='rbf', random_state=42)
  ```
  Step 3. Train SVM classifier before SMOTE <br>
  ```ruby
  svm_classifier_before_smote.fit(X_train, y_train)
  ```
  Step 4. Make predictions on the test set before SMOTE <br>
  ```ruby
  y_pred_before_smote = svm_classifier_before_smote.predict(X_test)
  ```
  Step 5. Compute and print confusion matrix and classification report before SMOTE
  ```ruby
  print("Confusion Matrix and Classification Report before SMOTE:")
  print(confusion_matrix(y_test, y_pred_before_smote))
  print(classification_report(y_test, y_pred_before_smote))
  ```

  ![SVM_Before smote Confusion](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/5ca15720-e31d-4c6c-a0be-6e59297cb226)


  Step 6. Train SVM classifier after SMOTE <br>
  ```ruby
  svm_classifier_after_smote.fit(X_train_resampled_scaled, y_train_resampled)
  ```
  Step 7. Make predictions on the test set after SMOTE
  ```ruby
  y_pred_after_smote = svm_classifier_after_smote.predict(X_test_scaled)
  ```
  Step 8. Compute and print confusion matrix and classification report after SMOTE
  ```ruby
  print("Confusion Matrix and Classification Report after SMOTE:")
  print(confusion_matrix(y_test, y_pred_after_smote))
  print(classification_report(y_test, y_pred_after_smote))
  ```
  
  ![SVM_After SMOTE Confusion](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/071e71d2-8392-41c2-9f1a-0f4938a903e1)

  Step 9. Plot Confusion Metrics Before and After SMOTE
  ```ruby
  # Plot confusion matrices
  fig, axes = plt.subplots(1, 2, figsize=(12, 6))

  # Plot confusion matrix before SMOTE
  axes[0].imshow(confusion_matrix_before_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[0].set_title('Confusion Matrix Before SMOTE')
  axes[0].set_xticks([0, 1])
  axes[0].set_yticks([0, 1])
  axes[0].set_xlabel('Predicted Label')
  axes[0].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[0].text(j, i, str(confusion_matrix_before_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center', color='white')

  # Plot confusion matrix after SMOTE
  axes[1].imshow(confusion_matrix_after_smote, cmap=plt.cm.Blues, interpolation='nearest')
  axes[1].set_title('Confusion Matrix After SMOTE')
  axes[1].set_xticks([0, 1])
  axes[1].set_yticks([0, 1])
  axes[1].set_xlabel('Predicted Label')
  axes[1].set_ylabel('True Label')
  for i in range(2):
      for j in range(2):
          axes[1].text(j, i, str(confusion_matrix_after_smote[i, j]),
                       horizontalalignment='center', verticalalignment='center', color='white')

  plt.tight_layout()
  plt.show()
  ```

  ![Plot confusion metric SVM](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/e5a86814-f223-45ea-892e-22bda98e9af1)


  Step 10. Plot Accuracy Before and After SMOTE
  ```ruby
  # Get classification reports before and after SMOTE
  classification_report_before_smote = classification_report(y_test, y_pred_before_smote,   output_dict=True)
  classification_report_after_smote = classification_report(y_test, y_pred_after_smote, output_dict=True)

  # Extract accuracy values
  accuracy_before_smote = classification_report_before_smote['accuracy']
  accuracy_after_smote = classification_report_after_smote['accuracy']

  # Plot accuracy before and after SMOTE
  labels = ['Before SMOTE', 'After SMOTE']
  accuracy_scores = [accuracy_before_smote, accuracy_after_smote]

  plt.bar(labels, accuracy_scores, color=['blue', 'green'])
  plt.xlabel('SMOTE')
  plt.ylabel('Accuracy')
  plt.title('Accuracy of SVM before and after SMOTE')
  plt.ylim(0, 1)  # Limit y-axis from 0 to 1 for accuracy range
  plt.show()
  ```
  ![SVM Accuracy Before adn After SVM](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/0cee870f-92b6-4a87-87f0-d3ada2d971e9)

  > Advantages: <br>
  >> - Effective in High Dimensional Spaces <br>
  >> - Still effective in cases where number of dimensions is greater than the number of samples
  >> - Uses a subset of training points in the decision function/support vectors, so it is also memory efficient
  >> - Versatile: different kernel functions can be specified for the decision function.

  > Disadvantages: <br>
  >> - If the number of features is much greater than the number of samples, avoid over-fitting in choosing kernel functions and regularization term is crucial <br>
  >> - SVM do not directly provide probability estimates, these are calculated using an expensive five fold cross validation<br>

- Which algorithm is best for prediction? <br>
  | Logistic Regression | Neural Network | Support Vector Machine |
  | :---: | :---: | :---: | 
  | ![LogReg_Accuracy_Before and after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/051a8bc0-2c44-4e54-a377-18e6c0e9e5bb) | ![NN_Diagram Accuracy before after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/635bc08d-d78f-4b57-b6c2-c71549879242) | ![SVM Accuracy Before adn After SVM](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/ac82d963-2026-4273-bcdc-2ed9f84a5033) | <br>

  The best algorithms for predicion Binary Integer Data in this case is ***Neural Network + SMOTE*** with accuracy 98%. Based on the plotting of accuracy results between NN Before and After SMOTE, Neural Network can automatically learn relevant features from raw data and have a flexibility in various architectures which enables them to capture different types of patterns and structures in the data, making them adaptable to diverse classification tasks across various domains. In this model, impelenting Activation RelU Function in input layer, hidden layer and Acitvation Sigmoid Function in Output layer are the main reason why Neural Network is the most appropriate algorithms for classifying Target Labelled into binary ineteger data. <br>

   ![NN_Accuracy Before after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/6c8ead2e-918c-4eb4-ba1f-c364b1270279)

## Evaluation
- What metrics evaluation is used in this project and how it works? <br> 
The metrics evaluation used are [Confusion Metrics, Accuracy, Precision, Sensitivity(Recall), Specificity and F1-Score](https://medium.com/javarevisited/evaluating-the-logistic-regression-ae2decf42d61). Those performance metrics are commonly used to evaluate a Binary Classification Model. Let's define each metric and how they work below: <br>
1. Confusion Metric: <br>
   A Tabular summary of True/False and Positive/Negative prediction rates. It allows to compute various performance metrics. <br>

   ![Basic-Confusion-matrix](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/2fd76ef0-c24e-4ba3-ae8a-0959bf5b1e9a)
   
2. Accuracy: <br>
measures the ratio of correct predictions from all predicted results. <br>

   ![accurcay score measuring](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/dd2b037c-cb5d-4cbd-a49c-547d67154a16)

3. Precision: <br>
measures what proportion of the positive predictions is actually positive. The precision score is useful for the succes of prediction when classes are very imbalanced and when it's significantly cost-efficient to identify all positive examples without any false positive. <br>

   ![precision formula](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/8d654914-c0eb-4047-95f6-e72aa5e9efbb)

4. Sensitivity/Recall: <br>
represents the model’s ability to correctly predict the positives out of actual positives. The higher the recall score, the better the machine learning model is at identifying positives. <br>
   ![recall formula](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/8a47bebf-2e71-4b39-8147-8d90b0ff3673)

5. Specificity: <br>
represents the model’s ability to correctly predict the negatives out of actual negatives. The higher the specificity score, the better the machine learning model is at identifying negatives. <br>

   ![specificity](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/0a7141f5-3bf6-4c89-bfcf-51010985190a)

6. F1 Score: <br>
combine the precision and recall of the model, and it is the harmonic mean of the precision and recall. It’s used often when data is imbalanced. <br>

   ![f1 score](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/4a047010-c742-47c0-a375-015bf2b223c8)

 
- Explanation of The Metrics Evaluation Project Results! <br>
  | X | Logistic Regression | Neural Network |  Support Vector Machine | 
  | :---: | :---: | :---: | :---: | 
  | Plot Accuracy |  ![LogReg_Accuracy_Before and after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/051a8bc0-2c44-4e54-a377-18e6c0e9e5bb) | ![NN_Diagram Accuracy before after smote](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/635bc08d-d78f-4b57-b6c2-c71549879242) | ![SVM Accuracy Before adn After SVM](https://github.com/adinplb/Belajar-Machine-Learning-Terapan-Dicoding/assets/61041719/ac82d963-2026-4273-bcdc-2ed9f84a5033) |


  |   | Accuracy  | Precision  |  Recall |  F1-Score |
  |---|---|---|---|---|
  | Logistic Regression  | 0.81  | 0.86  | 0.81  | 0.82  |
  |  Logistic Regression +SMOTE | 0.95  |  0.95 | 0.95  | 0.95  |
  |  Neural Network | 0.81  | 0.86  | 0.81  | 0.82  |
  | Neural Network + SMOTE  |  0.97 | 0.98  | 0.97  | 0.97  |
  |  SVM | 0.69  | 0.47  |  0.69 | 0.56  |
  |  SVM +SMOTE | 0.95  | 0.95  | 0.95 | 0.95  |

  To racap, on the comparison of confusion matrix and accuracy values plot results above, Neural Network with SMOTE has the highest accuracy score and great confusion matrics so this algorithms is the most  suitable and approriate model for predictiong Breast Tumor Diagnosis using Quantitative Cell-Nuclear Phenotypes Features. The flexibility of Neural Network Architectures makes enables to capture different types of patterns/structures in dataset and learn relevant numerical features to predict Binary Integer Data whether it is Benign (0) or Malignant (1).

## Conclusion 
1. Not all features have an impact to the algorithms in the model prediction.
2. Neural Network with handling imbalanced data using SMOTE, give the greatest accuracy so this algorithm is the best model for predicting Breast Tumor Diagnosis.
3. Yes, SMOTE influences the high accuracy of the model.
