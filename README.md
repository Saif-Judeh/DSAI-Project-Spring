Statistical Analysis Methodology
Methodology Choice — Inferential Statistical Analysis
Inferential Statistical Analysis was selected over time series analysis because the Spotify dataset is cross-sectional — each row represents a track with no temporal ordering or timestamps. Time series analysis requires data collected sequentially over time, which does not apply here. Inferential statistics is the appropriate choice as the goal is to test whether measurable differences in audio features exist across genres, and to identify which features significantly predict popularity.
Null Hypotheses
Three separate One-Way ANOVAs were conducted, each with the following null and alternative hypotheses:

H₀₁: Mean danceability is equal across all music genres
H₀₂: Mean energy is equal across all music genres
H₀₃: Mean valence is equal across all music genres

Alternative hypothesis (all three): At least one genre differs significantly from the others.
Significance level: α = 0.05
Results
All three null hypotheses were rejected (p ≈ 0 in all cases). The F-statistics were extremely large (714, 842, and 441 respectively), and eta-squared values confirmed large effect sizes — meaning genre alone explains 30–46% of the variance in these audio features. Results were validated using the non-parametric Kruskal-Wallis test, which confirmed all findings independent of normality assumptions. Tukey HSD post-hoc testing identified which specific genre pairs differ significantly from one another.
A multiple linear regression was also fitted to predict track popularity from all audio features. The model confirmed that danceability and loudness positively predict popularity, while instrumentalness, speechiness, and valence are negative predictors.
Visualizations

Boxplots of danceability, energy, and valence across 10 representative genres
Tukey HSD pairwise mean-difference heatmaps
Regression coefficient plot with 95% confidence intervals
Regression diagnostic plots (residuals, Q-Q, histogram)

Insights
The analysis confirms that genre is not just a label — it maps onto genuinely distinct and measurable audio profiles. However, audio features alone explain only 2.3% of the variance in popularity (R² = 0.023), meaning factors like artist fanbase, playlist placement, and platform promotion drive streaming success far more than how a track sounds. This is a non-obvious and actionable insight for a music platform: investing in audio-based recommendation engines has a ceiling, and artist/context-based signals should carry more weight.