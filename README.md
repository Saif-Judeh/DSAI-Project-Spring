<<<<<<< HEAD
<!-- < Statistical Analysis Methodology
Methodology Choice,Inferential Statistical Analysis
Inferential Statistical Analysis was selected over time series analysis because the Spotify dataset is cross-sectional, each row represents a track with no temporal ordering or timestamps. Time series analysis requires data collected sequentially over time, which does not apply here. Inferential statistics is the appropriate choice as the goal is to test whether measurable differences in audio features exist across genres, and to identify which features significantly predict popularity.
=======
Statistical Analysis Methodology
Methodology Choice


Inferential Statistical Analysis was selected over time series analysis because the Spotify dataset is cross-sectional, with each row representing a track with no temporal ordering or timestamps. Inferential statistics is the appropriate choice as the goal is to test whether measurable differences in audio features exist across genres and to identify which features significantly predict popularity.

>>>>>>> 007d6e74601fe5fb90765d031646481629226b6b
Null Hypotheses


Three separate One-Way ANOVAs were conducted:

H₀₁: Mean danceability is equal across all music genres
H₀₂: Mean energy is equal across all music genres
H₀₃: Mean valence is equal across all music genres

Alternative hypothesis (all three): At least one genre differs significantly from the others.

Significance level: α = 0.05
Results


All three null hypotheses were rejected (p ≈ 0 in all cases). F-statistics of 714, 842, and 441 combined with large eta-squared values confirm that genre alone explains 30 to 46% of the variance in these audio features. Results were validated using the Kruskal-Wallis test, and Tukey HSD post-hoc testing identified which specific genre pairs differ significantly.


Four progressive regression models were built, from audio features only (R² = 0.023) up to a full model with genre encoding and interaction terms (R² ≈ 0.25). Genre was the dominant predictor, with k-pop, pop-film, and chill carrying the strongest positive effects, while instrumentalness and acousticness were the strongest negative audio signals.




Visualizations

Boxplots of danceability, energy, and valence across 10 representative genres
Tukey HSD pairwise mean-difference heatmaps
Regression coefficient plot with 95% confidence intervals
Regression diagnostic plots (residuals, Q-Q, histogram)
Model comparison bar chart (R² across all four models)
Genre coefficient plot showing which genres boost or reduce predicted popularity

Insights
<<<<<<< HEAD
The analysis confirms that genre is not just a label — it maps onto genuinely distinct and measurable audio profiles. However, audio features alone explain only 2.3% of the variance in popularity (R² = 0.023), meaning factors like artist fanbase, playlist placement, and platform promotion drive streaming success far more than how a track sounds. This is a non-obvious and actionable insight for a music platform: investing in audio-based recommendation engines has a ceiling, and artist/context-based signals should carry more weight. --> 


<!-- 
Power BI Dashboard


Preparation: 
Data preparation was performed using Power Query, including removal of the redundant index column, conversion of the explicit boolean field into readable Explicit/Clean labels, and creation of calculated columns for duration in minutes and popularity tier (High/Mid/Low based on popularity score thresholds).

DAX Measure explanation: 


"Explicit Track % = 
DIVIDE(
    COUNTROWS(FILTER('dataset', 'dataset'[explicit] = "Explicit")),
    COUNTROWS('dataset')
) * 100"

This measure uses FILTER to isolate only the rows where the explicit field equals Explicit, then counts those rows with COUNTROWS. This is divided by the total row count of the full table using DIVIDE, which handles any division by zero edge cases. The result is multiplied by 100 to make it a percentage. This demonstrates row context filtering, since FILTER evaluates the explicit condition for every row in the table before the count happens.




Dashboard Features:

The dashboard includes four KPI cards (total tracks, average popularity, high popularity track count, and explicit track percentage), a bar chart ranking genres by average popularity, a clustered bar chart comparing danceability, energy, and valence across genres, a scatter plot of danceability versus energy, a histogram of the overall popularity distribution, and a donut chart comparing explicit and clean tracks. Four interactive slicers (genre, explicit status, popularity tier, and danceability range) allow stakeholders to filter all visuals dynamically. -->
=======



Genre is not just a label, it encodes genuinely distinct and measurable audio profiles. Audio features alone explain only 2.3% of popularity variance, but adding genre as a predictor raises this to approximately 25%. The remaining 75% is attributable to factors like artist fanbase, playlist placement, and platform promotion. For a music platform, this means audio-based recommendation engines have a ceiling, and artist-level and contextual signals should carry more weight.
>>>>>>> 007d6e74601fe5fb90765d031646481629226b6b
