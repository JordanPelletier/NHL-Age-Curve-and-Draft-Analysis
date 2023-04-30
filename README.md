# NHL-Age-Curve-and-Draft-Analysis
Using an xG model to improve upon the traditional RAPM (Regularized adjusted plus minus) model. Using RAPM values to analyze age curves and draft pick value in the NHL.

For full description of the project and results please read my article on the project posted at https://medium.com/@jordanpelletier1995/analyzing-age-curves-and-draft-pick-value-in-nhl-skaters-with-an-rapm-model-93504d1c9683

# Description of each notebook:

**xG model data setup:** Code to convert raw NHL play by play data into a dataset used for an expected goals model. Play by play scrapped with Harry Shomer's NHL PBP scrapper

**xG_Models:** Testing various models and producing visuals describing the returned values of the model.CV gridsearch was used to optimize models, and then had their code removed to reduce clutter.

**RAPM:** xG values are merged back onto the raw PBP. This is then used as a dataset to produce an RAPM model, where the coefficients are used as a dataset later on.

**Player_BIO_Scrape:** My scrapper for getting player info such as draft year, draft position, birthdate, handedness.

**PBP_Metric_Generation:** combining xG metrics, RAPM metrics, metrics from the raw PBP, and player BIO data using SQLlite3 python extension.

**Age_Curve_Draft_Pick:** Notebook containing final exploration of RAPM data to evaluate the effect of age on performance and the value of draft picks.
