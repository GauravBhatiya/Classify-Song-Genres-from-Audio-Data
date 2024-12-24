# Classify Song Genres from Audio Data

This project focuses on classifying songs into two genres, **Hip-Hop** and **Rock**, using machine learning techniques and audio feature data. The aim is to develop a model that can accurately classify songs based on features extracted from raw audio, without listening to the tracks themselves.


## **Motivation**
With the increasing volume of music available on streaming platforms, categorizing songs effectively is critical for personalized recommendations and playlist generation. This project explores the use of machine learning to automate the genre classification process, showcasing how audio features can drive intelligent music recommendations.



## **Dataset**
The datasets used in this project are sourced from The Echo Nest:
- **Track Metadata (CSV)**: Contains song information such as `track_id` and `genre_top` (Hip-Hop or Rock).
- **Audio Features (JSON)**: Includes numerical metrics like `danceability`, `acousticness`, and more.

### **Data Processing**
1. **Merge Datasets**:
   - The CSV and JSON files are merged on `track_id` to combine features and labels.
2. **Feature Selection**:
   - Numerical features are selected for training, excluding non-relevant columns.
3. **Standardization**:
   - Features are scaled using `StandardScaler` to normalize the data for better model performance.


## **Techniques and Workflow**
### **1. Exploratory Data Analysis (EDA)**
- **Correlation Matrix**:
  - Analyzed feature relationships to understand data structure and reduce redundancy.
- **Principal Component Analysis (PCA)**:
  - Reduced dimensionality while retaining significant variance, ensuring efficient model training.

### **2. Machine Learning Models**
- **Decision Tree**:
  - Used for its interpretability and simplicity in classification tasks.
- **Logistic Regression**:
  - Applied as a baseline for comparison due to its effectiveness in binary classification.

### **3. Pipeline Implementation**
To streamline preprocessing and model training, a robust **machine learning pipeline** was implemented using `scikit-learn`:
1. **Steps in the Pipeline**:
   - **Preprocessing**: Scaling features with `StandardScaler`.
   - **Dimensionality Reduction**: Applying PCA to retain key components.
   - **Model Training**: Using Logistic Regression or Decision Tree as the classifier.
2. **Advantages**:
   - Automates repetitive tasks, making the workflow efficient and reproducible.
   - Allows easy hyperparameter tuning and model experimentation.

### **4. Train-Test Split**
- Features (`X`) and labels (`y`) were split into training and testing sets (75%-25% ratio).

### **5. Evaluation Metrics**
- **Accuracy**:
  - Measured the proportion of correctly classified songs.
- Additional metrics such as precision and recall can be explored in future iterations.


## **Results**
- The models demonstrated the ability to classify songs with reasonable accuracy, with logistic regression serving as a strong baseline.
- PCA contributed to improved performance by reducing noise and dimensionality.


## **Deployment**
This project can be extended to deploy a web app for interactive genre classification. A future version could:
1. Allow users to upload audio files for real-time predictions.
2. Visualize feature importance and classification results interactively.


## **Future Work**
1. **Enhanced Feature Engineering**:
   - Incorporate additional audio metrics (e.g., tempo, energy).
2. **Advanced Models**:
   - Experiment with ensemble methods like Random Forest or Gradient Boosting.
3. **Scalability**:
   - Expand the dataset to include more genres and multilingual tracks.

