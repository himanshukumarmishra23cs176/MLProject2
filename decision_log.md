Missing values were handled through strategic imputation: Age with median (robust to outliers), Embarked with mode (categorical appropriateness), and Fare with median. Cabin (77% missing) was transformed into a binary HasCabin feature before dropping the original column, preserving information about cabin availability while eliminating the high-missingness variable.

Outliers in Fare were addressed through log transformation after detecting them via both IQR and Z-score methods. This approach reduced skewness while maintaining the relative ordering of values, preventing extreme values from disproportionately influencing the model.

Categorical variables (Sex, Embarked, Title) were one-hot encoded to convert them into machine-readable format while avoiding ordinal assumptions. Feature engineering created meaningful family structure indicators (FamilySize, IsAlone, HasSiblings, etc.) that capture potentially predictive relationships.

All transformations were applied consistently to both training and test sets to ensure data integrity and prevent leakage. Numerical features received both MinMax and Z-score normalization to provide modeling flexibility. The feature selection process employed multiple methods (correlation, tree-based importance, statistical testing) to identify the most predictive features while reducing dimensionality.
