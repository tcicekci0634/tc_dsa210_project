# tc_dsa210_project
### Project Note on the 'Data Collection - EDA - Hypothesis' Part

At this stage of the project, it is important to acknowledge several key observations and practical constraints that shape both the interpretation of the results and the direction of the next steps.

First, the initial analysis shows that single-variable correlations between financial ratios and returns do not produce strong or consistent results. However, this outcome is not unexpected—especially in financial markets and particularly over shorter time horizons. Returns are rarely driven by a single factor in isolation; instead, they tend to emerge from the interaction of multiple variables. This observation is further supported by the hypothesis testing results, where individual features fail to show strong statistical significance. Together, these findings motivate a shift toward using multiple ratios simultaneously in the machine learning stage, where non-linear relationships and interactions can be better captured.

Second, there were practical challenges related to data collection. Due to limitations with APIs and scraping (which were present in earlier versions of the data collection pipeline but are not fully reflected in the final main script), it was difficult to consistently retrieve complete and high-quality financial data. As a result, I had to reduce the time horizon and work with a smaller set of available financial ratios. While this constrains the depth of the analysis, it ensures that the dataset remains reliable and usable.

Finally, I also encountered issues in collecting news and sentiment data. At the moment, this component is not fully integrated into the project. However, incorporating news-based features remains an important objective, and I plan to address these data access challenges in the later stages of the project.

Overall, these limitations have influenced the current scope of the analysis, but they also provide clear direction for the next phase: focusing on multi-factor modeling, improved feature engineering, and more robust data integration.


Use of AI Tools

AI tools (specifically large language models such as ChatGPT and Claude) were used in a limited and supportive capacity during this project. Their role was primarily focused on:

Clarifying statistical concepts,
Suggesting alternative approaches (especially in getting financial data and hypothesis testing),
Assisting with code structuring and debugging in certain parts of the EDA and hypothesis testing stages.

Use of AI Tools part will be updated and used prompts will be added after ML stage




## Notes on the Machine Learning Part

The ML component of this project follows a structured, step-by-step pipeline designed to evaluate the incremental value of different information sources in predicting stock return direction.

The modelling process is built around three progressive stages:

- **Base model:** Uses only price-based momentum and volatility features  
- **Stage 1:** Adds macroeconomic variables (VIX, interest rates)  
- **Stage 2:** Further incorporates fundamental and interaction features  

Each stage is evaluated using an **expanding window time-series validation framework**, ensuring that all predictions are strictly forward-looking and free from data leakage.

In addition to classification accuracy, model performance is assessed using financially meaningful metrics such as:
- average return when long  
- cumulative strategy return  
- comparison against a buy-and-hold benchmark  

---

## Hyperparameter Tuning

As a final step, hyperparameter tuning was applied using `GridSearchCV` combined with `TimeSeriesSplit` to ensure time-consistent validation.

The goal of tuning was not only to improve predictive performance, but also to test whether model configuration (rather than data or feature design) was limiting results.

To maintain transparency and reproducibility, two separate versions of the ML workflow are provided:

- **Baseline model (no tuning):** reflects raw model behaviour using default parameters  
- **Tuned model:** incorporates optimized hyperparameters  

This separation allows for a clear comparison of model behaviour before and after optimization.

---

## Notes and Final Adjustments

Additional refinements will be completed in the final stage of the project, including:

- adding detailed inline code comments  
- documenting AI-assisted prompts used during development  
- minor structural and readability improvements  

These updates are intentionally deferred to preserve clarity during the modelling and evaluation phase.
