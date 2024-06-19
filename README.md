# Maneuvers-in-orbital-data
The goal is to create a method that automatically detects maneuvers in orbital data. This is achieved using machine learning (ML) approaches.

# Problem Statement
The task requires identifying potential maneuvers, like engine burns or orientation adjustments, using only the semi-major axis (SMA) variation over time and without explicit maneuver data. 
Reference graphs with known maneuvers will be provided to assess the method's accuracy. Note that this provided data is not true data used to build the model.

# Repository Includes
code includes modules for data preprocessing, feature extraction, maneuver detection, and result visualization.

# Analysis
The detected anomalies from Isolation Forest and DBSCAN align well with known maneuver dates, validating the effectiveness of these approaches. Random Forest classification improved the predictive power by leveraging ensemble learning, reducing false positives and false negatives. Additional anomalies detected by DBSCAN and Random Forest may indicate previously unidentified maneuvers or false positives, warranting further investigation.

# Assumptions
1. Data Quality : The provided SMA and DateTime data is assumed to be accurate and free from significant errors or noise.
2. Feature Relevance : Extracted features are assumed to be relevant and sufficient for detecting maneuvers.
3. Maneuver Characteristics : Maneuvers are assumed to cause significant deviations in the SMA, detectable as anomalies.
4. Static Contamination Rate : The contamination rate for Isolation Forest is set to 5%, assumed to represent the proportion of maneuvers.
5. Data Continuity : The dataset is assumed to be continuous without large gaps, ensuring detected anomalies reflect true maneuvers.
