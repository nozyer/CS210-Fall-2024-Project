# CS210-Fall-2024-Project

## Netflix and Spotify Data Analyzing Project

---

### **Project Overview**
This project aims to explore the relationship between Netflix and Spotify preferences and how moods transition between these platforms. By analyzing viewing habits on Netflix and listening behaviors on Spotify, we uncover insights into how entertainment affects mood and identify patterns that can help build a mood-based recommendation system.

---

### **Datasets Used**

1. **Netflix Data**:
   - Columns:
     - `Title`: Name of the watched content.
     - `Start Time`: Time the content was played.
     - `Watch Duration`: Duration of viewing.
     - `Type`: Movie or series.
     - `Genre`: Genre of the content.
     - `Mood_x`: Represents the inferred mood from the genre (e.g., Joyful/Relaxed, Energetic/Excited).

2. **Spotify Data**:
   - Columns:
     - `Genre`: Music genre.
     - `Listen Duration`: Duration of listening.
     - `Start Time`: Time the song or playlist was played.
     - `Mood_y`: Represents the inferred mood from the song or playlist (e.g., Neutral, Melancholic/Emotional).

3. **Merged Dataset**:
   - Combines Netflix and Spotify data, aligned by timestamps, and includes moods (`Mood_x` for Netflix, `Mood_y` for Spotify).

---

### **Project Plan**

#### **1. Data Preprocessing**
- Merged Netflix and Spotify datasets into a unified structure for easier analysis.
- Cleaned and synchronized the data using timestamps, ensuring meaningful mood correlations.

#### **2. Mood Classification**
- **Netflix Moods**:
  - Assigned moods to genres:
    - Drama → Melancholic/Emotional.
    - Comedy → Joyful/Relaxed.
    - Action → Energetic/Excited.
- **Spotify Moods**:
  - Assigned moods based on listening data and song attributes:
    - High danceability and energy → Energetic/Excited.
    - Low tempo and high acousticness → Calm/Neutral.

#### **3. Correlation Analysis**
- Examined correlations between Netflix moods and Spotify moods.
- Key patterns:
  - **Mood Alignment**: Watching joyful content aligns with listening to joyful music.
  - **Mood Compensation**: Watching energetic content may lead to listening to calmer music.

#### **4. Visualization**
- Created heatmaps and charts to explore:
  - Relationships between Netflix moods and Spotify moods.
  - Correlations among Spotify song attributes like energy, danceability, and valence.

#### **5. Expected Outcomes**
- Understand how Netflix content influences Spotify music preferences.
- Identify whether users prefer mood alignment or compensation when switching between platforms.

#### **6. Mood-Based Recommendation System**
- Developed a machine learning model using **Balanced Random Forest Classifier** to predict Spotify moods based on Netflix moods.
- Provided mood-based music recommendations to complement Netflix viewing experiences.

---

### **Results and Insights**

#### **Model Performance**
- **Accuracy**: **40%**
  - The model correctly predicted 2 out of 5 samples in the test set.
  - Precision, recall, and F1-scores varied significantly across classes.

#### **Key Findings**
1. **Energetic/Excited**:
   - Precision: **1.00**
   - Recall: **0.50**
   - The model was confident in its predictions but missed half of the true occurrences.
   
2. **Neutral**:
   - Precision and Recall: **0.50**
   - The model moderately predicted the occurrences of Neutral mood.

3. **Underrepresented Classes**:
   - **Joyful/Relaxed**, **Melancholic/Emotional**, and **Mysterious/Tense** had insufficient data in the training or test sets, leading to poor or no predictions.

#### **Behavioral Insights**
- **Mood Alignment**:
  - Users often maintain their mood between platforms. For instance, watching joyful content on Netflix aligns with listening to joyful music on Spotify.

- **Mood Compensation**:
  - Some users switch to contrasting moods. After watching energetic or tense Netflix content, users often listen to calming or neutral music.

- **Class Imbalance**:
  - The dataset's imbalance caused the model to favor dominant classes like **Energetic/Excited** and **Neutral**, which had better representation.

---

### **Future Enhancements**

1. **Data Improvements**:
   - Collect additional samples for underrepresented moods.
   - Incorporate richer features like Spotify song attributes (e.g., valence, tempo).

2. **Algorithm Optimization**:
   - Experiment with alternative models like **XGBoost** or **LightGBM**.
   - Optimize hyperparameters to improve model accuracy.

3. **Cross-Platform Integration**:
   - Integrate Netflix and Spotify APIs to provide real-time recommendations.

4. **Behavioral Insights**:
   - Analyze how mood preferences evolve throughout the day.

---

### **How to Use**

#### **Run the Code**
1. Load the dataset: `"Cleaned_Netflix_and_Spotify_Merged_Data.csv"`.
2. Train the machine learning model to predict Spotify moods based on Netflix moods.

#### **Make Predictions**
- Use the `recommend_mood()` function to predict Spotify moods based on a given Netflix mood.
- Example:
  ```python
  recommendation = recommend_mood("Joyful/Relaxed")
  print(f"Recommended Spotify Mood: {recommendation}")