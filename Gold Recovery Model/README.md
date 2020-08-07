# Gold Recovery Model

## Data

The data for this project was provided by Yandex.Practicum in three files: training dataset, test dataset and source dataset. It contains a lot of measurements during the whole technological process of gold purification:
#### Technological process
- Rougher feed — raw material
- Rougher additions (or reagent additions) — flotation reagents: Xanthate, Sulphate, Depressant
- Xanthate — promoter or flotation activator;
- Sulphate — sodium sulphide for this particular process;
- Depressant — sodium silicate.
- Rougher process — flotation
- Rougher tails — product residues
- Float banks — flotation unit
- Cleaner process — purification
- Rougher Au — rougher gold concentrate
- Final Au — final gold concentrate
#### Parameters of stages
- air amount — volume of air
- fluid levels
- feed size 
- feed rate
#### Feature naming
- [stage].[parameter_type].[parameter_name]
- Example: rougher.input.feed_ag
- Possible values for [stage]:
  - rougher — flotation
  - primary_cleaner — primary purification
  - secondary_cleaner — secondary purification
  - final — final characteristics
- Possible values for [parameter_type]:
  - input — raw material parameters
  - output — product parameters
  - state — parameters characterizing the current state of the stage
  - calculation — calculation characteristics

## Task
To build a machine learning model for a gold mining company that should predict the amount of gold recovered from gold ore.<br>
Both recovery after flotation (rougher output) and after the final stage of purification needed to be predicted.<br>
To evaluate the model we should use symmetric Mean Absolute Percentage Error (sMAPE). <br>
final sMAPE = 25% * sMAPE(rougher) + 75% * sMAPE(final)

## Details
- dealing with imbalanced class 
- implemented custom cross-validation for upsample and downsample techniques

## Machine Learning Algorithmes used
*RandomForestRegressor*, *GradientBoostingRegressor*, *AdaBoostRegressor*, *MultiOutputRegressor*, *Lasso*, *Ridge*, *ElasticNet*

## Libraries used
*pandas*,
*numpy*,
*matplotlib*,
*scikit-learn*
