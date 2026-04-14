# tc_dsa210_project
### Project Note on Data Limitations and Feature Insights

At this stage of the project, it is important to acknowledge several key observations and practical constraints that shape both the interpretation of the results and the direction of the next steps.

First, the initial analysis shows that single-variable correlations between financial ratios and returns do not produce strong or consistent results. However, this outcome is not unexpected—especially in financial markets and particularly over shorter time horizons. Returns are rarely driven by a single factor in isolation; instead, they tend to emerge from the interaction of multiple variables. This observation is further supported by the hypothesis testing results, where individual features fail to show strong statistical significance. Together, these findings motivate a shift toward using multiple ratios simultaneously in the machine learning stage, where non-linear relationships and interactions can be better captured.

Second, there were practical challenges related to data collection. Due to limitations with APIs and scraping (which were present in earlier versions of the data collection pipeline but are not fully reflected in the final main script), it was difficult to consistently retrieve complete and high-quality financial data. As a result, I had to reduce the time horizon and work with a smaller set of available financial ratios. While this constrains the depth of the analysis, it ensures that the dataset remains reliable and usable.

Finally, I also encountered issues in collecting news and sentiment data. At the moment, this component is not fully integrated into the project. However, incorporating news-based features remains an important objective, and I plan to address these data access challenges in the later stages of the project.

Overall, these limitations have influenced the current scope of the analysis, but they also provide clear direction for the next phase: focusing on multi-factor modeling, improved feature engineering, and more robust data integration.

