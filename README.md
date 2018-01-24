# Crime Forecasting in Mexico

Authors: Pedro Armengol & Faraz Ahmed

This project use data of the Mexican Ministry of Statistics (INEGI) to predict different types of crimes in Mexico. 

First, we download about 25 CSV's of INEGI containing information at State and Month-Year level in order to create our predictive features.
The INEGI data cover education, transportation, infrastructure, criminal justice records, economic outcomes and so on. In total, we collected
more that 200 features. Then, we obtained the information of 20 different crimes for the Mexico's Prosecutor Statistics Office (SESNP).
Later on, we created a database using SQL schemas. Later, we process the data in Python (Pandas) to create lags and changes (more predictors using the same data).

To predict, we built a class in Python that estimate different models for each type of crime (we predict in year and state basis). As a predictive technique, we used least absolute shrinkage and selection operator (LASSO) with different lambdas. The models were estimated using the scikit-learn package. Is necessary to say that we didn’t trained our models through cross-validation and it presents serious overfitting problems. 

Our exercise was published in a local website using Flask. The website has a data exploratory analysis (levels and correlations) as well as the predictive results.

Sources:

http://sc.inegi.org.mx/cobdem/contenido.jsp?rf=false&solicitud=

http://secretariadoejecutivo.gob.mx/incidencia-delictiva/incidencia-delictiva-fuero-comun.php
