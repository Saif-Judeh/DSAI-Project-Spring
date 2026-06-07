Statistical Analysis Methodology
Methodology Choice


Inferential Statistical Analysis was selected over time series analysis because the Spotify dataset is cross-sectional, with each row representing a track with no temporal ordering or timestamps. Inferential statistics is the appropriate choice as the goal is to test whether measurable differences in audio features exist across genres and to identify which features significantly predict popularity.

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



Genre is not just a label, it encodes genuinely distinct and measurable audio profiles. Audio features alone explain only 2.3% of popularity variance, but adding genre as a predictor raises this to approximately 25%. The remaining 75% is attributable to factors like artist fanbase, playlist placement, and platform promotion. For a music platform, this means audio-based recommendation engines have a ceiling, and artist-level and contextual signals should carry more weight.
