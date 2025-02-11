# 8. Data structures in R - Dataframes 

A dataframe is one of R's most fundamental and powerful data structures, specifically designed to handle tabular data in a way that's intuitive for data analysis. In the context of medical research and precision medicine, dataframes are essential for managing patient data, genetic information, and clinical trial results.

## 8.1. Basic structures and creation of dataframes 

Dataframes are two-dimensional data structures that organize data into rows and columns, where each column can contain different types of data (numeric, character, logical, etc.).

```
patient_data <- data.frame(
  patient_id = c(1, 2, 3, 4),
  age = c(45, 52, 38, 61),
  blood_pressure = c(120, 135, 118, 142),
  diabetes = c(FALSE, TRUE, FALSE, TRUE)
)
```

You can view the datafaframe structure with the following codes:

```
# Basic structure inspection
str(patient_data)
head(patient_data)
```

You could also view the the descriptive statistics of the dataframe:

```
summary(patient_data)
```

## 8.2. Selecting columns

We can select the columns we want and store it as a separate variable. 

For example:

```
# Using $ notation
blood_pressure_values <- patient_data$blood_pressure

# Using square brackets
age_values <- patient_data[, "age"]
```

> [!NOTE]
> If you remember, `patient_data$blood_pressure` is used to access the values in the name `blood pressure` 

> [!NOTE]
> The square brackets [] are used to subset the data frame.
> The first part (before the comma) represents the rows to be selected. In this case, it is left blank, which means all rows will be selected.
> The second part (after the comma) represents the columns to be selected. In this case, "age" is specified as a character string, indicating that we want to select the column named "age".

We can also filter rows.

For example,

```
# Searching for patients with blood pressure > 130
high_bp_patients <- patient_data[patient_data$blood_pressure > 130, ]
```

## 8.3. Adding and modifying data 

The ability to modify dataframes by adding or updating information is essential when working with evolving medical data.

**(a) Add new columns**

For example, we may want to add a BMI column. 

```
patient_data$bmi <- c(24.5, 28.3, 22.1, 27.8)
```

**(b) Updating existing values**

```
patient_data$blood_pressure[patient_data$patient_id == 1] <- 122
```

## 8.4. Merging and combining dataframes 

In medical research, data often comes from multiple sources and needs to be combined for comprehensive analysis.

For example:

```
# Dataframe 1
patient_data <- data.frame(
  patient_id = c(1, 2, 3, 4),
  age = c(45, 52, 38, 61),
  blood_pressure = c(120, 135, 118, 142),
  diabetes = c(FALSE, TRUE, FALSE, TRUE)
)

# Dataframe 2
patient_demographics <- data.frame(
  patient_id = c(1, 2, 3, 4),
  gender = c("F", "M", "F", "M"),
  smoking_status = c("Never", "Former", "Current", "Never")
)

# Combining the two dataframes
complete_patient_data <- merge(
  patient_data, 
  patient_demographics, 
  by = "patient_id"
)
```

> [!WARNING]
> By default, when you use merge(), R performs what's called an "inner join" - it only keeps rows where the matching key (like patient_id) exists in both dataframes. This can indeed lead to data loss if you're not careful.
>
> For example,
>
> ```
> # Dataframe 1: Clinical Data
> clinical_data <- data.frame(
>   patient_id = c(1, 2, 3, 4),
>   age = c(45, 52, 38, 61),
>   blood_pressure = c(120, 135, 118, 142)
> )
> 
> # Dataframe 2: Lab Results
> lab_results <- data.frame(
>   patient_id = c(1, 2, 3, 4, 5),
>   glucose = c(90, 110, 85, 140, 95),
>   cholesterol = c(180, 200, 170, 220, 190)
> )
> 
> # Default merge (inner join)
> merged_data <- merge(clinical_data, lab_results, by = "patient_id")
> ```
>
> In this case, Patient 5 will be omitted because they only exist in the lab_results dataframe.
>
> However, you can control this behavior using the all, all.x, or all.y parameters in merge():
>
> ```
> full_merge <- merge(clinical_data, lab_results, by = "patient_id", all = TRUE)
> ```
>
> When you use these parameters, missing values will be filled with NA rather than being omitted. This is often preferable in medical research where you might want to know which data points are missing rather than automatically excluding incomplete records.
