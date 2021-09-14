# Pump-It-Up-Machine-Learning-Project

## Preprocessing

### Handeling missing values in data set

1. Added 'Unknown' for Nan values

installer and funder fill Nans with 'Unknown' value

2. Fill numerical null values from mean value and max frequent values acording to context

population, latitude and longitude null values are filled with mean value
public_meeting, construction_year and permit null values are filled with most frequent value

### Encoding the Categorical Data

Use label encoding for categorical features
 
### Normalization



## Feature Engineering

### Create features

Created 3 new numerical features as recorded_year, recorded_month, recorded_date from date_recorded

### Feature selection

1. To identify the co-related features used heat map for numerical values.

2. Some object type feature are droped beacuse they have same representation of data.

Form source_type, source_class and source, source_type and source_class are dropped.
From quantity and quantity_group, dropped quantity_group
From payment and payment_type, dropped payment_type
From water_quality and quality_group, dropped quality_group
From waterpoint_type and waterpoint_type_group,dropped waterpoint_type_group
From management and management_group, dropped management_group
From extraction_type_group, extraction_type_class and extraction_type, dropped extraction_type_group and extraction_type_class
From region, subvillage and region_code, subvillage is dropped because all are represent geographycal data and subvillage has large non unique values.


4. Object type features which had considerble Nan values are dropped

scheme_management is dropped because it has 3000 Nan values
amount_tsh is dropped it has 70% of zeros

5. Droppped object type features which has large unusefull values

wpt_name is dropped, because it has more than 50% of unique values  and 
Also scheme_name and subvillage are dropped, it have large unique values
num_private is dropped, because it has 98% of zeros
Since recorded_by has only one unique value, it does not depend to output. So featue is dropped
