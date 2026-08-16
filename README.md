# No-show Appointments Analysis


## Overview

This project analyzes medical appointment data from Brazil to explore factors related to whether patients attend or miss their appointments.
## Research Questions

1. Is there a relationship between receiving an SMS reminder and whether patients attend their appointments?
2. Is there a relationship between patient age and appointment attendance?
3. Is there a relationship between enrollment in the scholarship program and whether patients attend their appointments?

4. ## Dataset

The dataset contains medical appointment records from Brazil. Each row represents one medical appointment and includes information about the patient, appointment dates, scholarship enrollment, SMS reminders, and appointment attendance.

The main outcome variable is `No-show`:

- `0` = Patient attended the appointment
- `1` = Patient did not attend the appointment

- ## Tools Used

- Python
- Pandas
- Matplotlib
- Jupyter Notebook

- ## Data Cleaning

The following data cleaning steps were performed:

- Removed one record with an invalid age of `-1`.
- Converted `ScheduledDay` and `AppointmentDay` to datetime format.
- Converted `Handcap` into a binary indicator.
- Changed `PatientId` from `float64` to `int64`.
- Converted `No-show` from `Yes/No` to `1/0`.
- Checked for duplicate records.

## Key Findings

### SMS Reminders

Patients who received an SMS reminder had a higher no-show rate than patients who did not receive one:

- Received SMS: **27.6%**
- Did not receive SMS: **16.7%**

### Patient Age

Patients who attended their appointments had a higher median age than patients who did not attend:

- Attended: **38 years**
- Did not attend: **33 years**

### Scholarship Program

Patients enrolled in the scholarship program had a higher no-show rate than patients who were not enrolled:

- Enrolled: **23.7%**
- Not enrolled: **19.8%**

- ## Limitation

This analysis explores relationships between selected variables and appointment attendance. It does not prove causation, and no statistical tests were performed to determine whether the observed differences are statistically significant. Other factors may also influence whether patients attend their appointments.

## Project Files

- `Investigate_a_Dataset.ipynb` — Jupyter Notebook containing the complete analysis.
- `Investigate_a_Dataset.html` — HTML version of the analysis.
- `noshowappointments-kagglev2-may-2016 (1).csv` — Dataset used in the analysis.

- ## Conclusion

The analysis found differences in appointment attendance across SMS reminder status, patient age, and scholarship enrollment. Further analysis using additional variables and statistical tests could provide a deeper understanding of the factors associated with missed appointments.
