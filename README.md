# Scoring

After looking through raw data, I've decided to take following steps;

1. Applied `identify_zero_importance_features` function to identify and then drop zero importance features in a training dataset based on the feature importances from a gradient boosting model.
2. Decided to try out [featuretools](https://github.com/FeatureLabs/featuretools) an open source python library for automated feature engineering, because of inability to come up with domain specific feature engineering.
3. Applied `reduce_mem_usage` function which resulted in decreasing memory usage by 67.8% and 74.9%.
4. Removed Collinear Variables, because these can decrease the model's availability to learn, decrease model interpretability, and decrease generalization performance on the test set.
5. Automated Hyperparameter Tuning via Bayesian Optimization and the [Hyperopt](https://github.com/hyperopt/hyperopt) library to tune the hyperparameters of a gradient boosting machine.

- "reports/submission.csv" (zbiór test_rekrutacyjny_dane_walidacyjne z obliczoną predykcją modelu)
- "notebooks/00_eda_feature_engineering_model_tuning.ipynb" (Przestawienia danych/analizy obrazującej zdolność modelu do generalizacji (inaczej pokazującej, że model nie jest przeuczony))
- "notebooks/01_light_gradient_boosting_machine.ipynb" (Przedstawienie, krótkiego opisu techniki zbudowania modelu (jaki został użyty algorytm, jakie techniki przygotowania danych) ewentualnie przesłanie skryptu analizy)
