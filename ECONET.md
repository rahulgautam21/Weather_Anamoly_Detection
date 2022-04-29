# EcoNET Dataset

This dataset consists of 23 measurements from sensors at 45 weather stations around North Carolina for the year 2021.
See [these slides](https://docs.google.com/presentation/d/1fDYvhloskC5TLCBD2MLW92Q0V8wI_2sju6KjPVZKgmk/edit#slide=id.g118a1692908_0_8) for more details.

## Features:

* Station: The station where the reading was taken.
* Ob: The date of the reading.
* value: The value of the reading.
* measure: What the reading measured.
* target: True if the reading was reviewed by a human and found to be likely erroneous, and False if reviewed by a human and found to be likely accurate.
* R/I/Z/B_flag: One of 4 automated Quality Control (QC) flags generated based on this reading. See the white paper in the "Further Reading" section for more.


## Files

* ECONET_QC_Readme.xlsx: Contains information on each of the columns, along with more information on the 4 flags provided.
* train.csv: Contains the training data, with `target` labels. Training data includes the first 3 weeks out of every 4 weeks.
* test.csv: Contains the test data, without `target` labels. Test data includes the last weeks out of every 4 weeks. This data is used to make predictions for the in-class competition (details will be posted elsewhere).
* full/*.csv: Contains the full time-series data for each weather station for the year 2021. This data in unlabeled and contains all readings, not just the ones reviewed by a human. This data may be used to extract features to help predict wither reviewed readings were accurate.

## Further Reading

* A description of the ECONet Sensors is [here](https://econet.climate.ncsu.edu/about/)
* A white paper explaining the 4 QC flags and how they're calculated is [here](https://econet.climate.ncsu.edu/wp-content/uploads/2021/05/QC-paperV4_NoLN.pdf)