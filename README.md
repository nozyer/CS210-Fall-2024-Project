# CS210-Fall-2024-Project

 Netflix and Spotify Data Analyzing Project



## PROJECT IDEA

- **Mood Analysis of Netflix and Spotify Preferences:**

    - The idea is to understand how different types of movies or series I watch on Netflix affect my mood and how this influences my music preferences on Spotify. By examining the relationship between my streaming choices across these two platforms, I can gain insights into how my mood is shaped by my entertainment habits.



## DATASET
- **Netflix Data:** This will include Title, Start Time, Watch Duration, Type, and Genre.
- **Spotify Data:** This will include Genre, Listen Duration, and Start Time.


## PROJECT PLAN
- **Data Preprocessing:**
    - Collect data from both Netflix and Spotify and clean it for analysis.
    - Synchronize the data from both platforms to match specific time periods.


- **Mood Classification:**

        - Assign mood labels to different Netflix content genres. For example:

        Drama: Melancholic or emotional mood.
        Comedy: Relaxed or joyful mood.
        Action: Energetic or excited mood.

        - Use Spotify song attributes (energy, valence, danceability) to classify their mood impact.

- **Correlation Analysis:**

        - Analyze correlations between Netflix genres and Spotify music preferences. For instance, determine if watching dramas leads to a preference for calmer, more emotional music, or if action movies lead to a preference for more energetic music.

- **Visualization:**

        - Create visualizations to showcase the relationship between the type of Netflix content I watched and the subsequent music choices on Spotify.

        - Use time series graphs to depict changes in mood and music genre preferences over time.

        - Utilize heatmaps to show correlations between content genres and music preferences.

- **Expected Outcomes**

        - Gain insights into how my mood is influenced by different types of content on Netflix and how it affects my Spotify music preferences.

        - Develop a mood-based recommendation system that suggests music after specific genres of movies or series are watched, enhancing my overall entertainment experience.

- **Tools and Technologies**

        - Data Collection: Use Netflix and Spotify data export tools.

        - Data Analysis: Python with libraries like Pandas for data manipulation and Scikit-learn for analysis.

        - Visualization: Matplotlib or Seaborn for creating insightful visualizations.
