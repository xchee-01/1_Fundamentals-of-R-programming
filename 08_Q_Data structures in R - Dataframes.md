## Basic questions

#### 1. How would you view the structure of this dataframe?

```
patient_data <- data.frame(
    patient_id = c(1, 2, 3, 4, 5),
    age = c(45, 52, 38, 61, 43),
    mutation_present = c(TRUE, FALSE, TRUE, FALSE, TRUE)
)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  str(patient_data)
  ```
  
  </details>

#### 2. Using the same dataset in question 1, how would you extract just the age values into a new variable called `patient_ages`?

  <details>
  <summary>Click to view answer</summary>

  ```
  patient_ages <- patient_data$age
  # OR
  patient_ages <- patient_data[, "age"]
  ```
  
  </details>

#### 3. Using the same dataset in question 1, how would you find all patients who are over 50 years old?

  <details>
  <summary>Click to view answer</summary>

  ```
  older_patients <- patient_data[patient_data$age > 50, ]
  ```
  
  </details>

#### 4. Using the same dataset in question 1, how would you add a new column called "treatment_status" with values c("Active", "Complete", "Active", "Complete", "Active")?

  <details>
  <summary>Click to view answer</summary>

  ```
  patient_data$treatment_status <- c("Active", "Complete", "Active", "Complete", "Active")
  ```
  
  </details>

#### 5. Using the same dataset in question 1, how would you update the age of patient_id 1 to 46?

  <details>
  <summary>Click to view answer</summary>

  ```
  patient_data$age[patient_data$patient_id == 1] <- 46
  ```
  
  </details>

#### 6. Using the same dataset in question 1, how would you get a summary of all numerical columns in the dataset?

  <details>
  <summary>Click to view answer</summary>

  ```
  summary(patient_data)
  ```
  
  </details>

#### 7. Using the same dataset in question 1, how would you determine how many patients have mutations present?

  <details>
  <summary>Click to view answer</summary>

  ```
  sum(patient_data$mutation_present == TRUE)
  # OR
  nrow(patient_data[patient_data$mutation_present == TRUE, ])
  ```
  
  </details>

## Intermediate questions

#### 8. How would you merge these datasets while keeping only patients that are common across the datasets?

```
genetic_data <- data.frame(
    patient_id = c(1, 2, 3, 4, 5),
    gene_expression = c(0.5, 1.2, 0.8, 1.5, 0.9)
)

clinical_data <- data.frame(
    patient_id = c(1, 2, 3, 4, 6),
    response = c("Positive", "Negative", "Positive", "Negative", "Positive")
)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  common_data <- merge(genetic_data, clinical_data, by = "patient_id")
  common_data
  ```
  
  </details>

#### 8. How would you merge these datasets while keeping only patients that are common across the datasets?

  <details>
  <summary>Click to view answer</summary>

  ```
  complete_data <- merge(genetic_data, clinical_data, by = "patient_id", all = TRUE)
  complete_data
  ```
  
  </details>

