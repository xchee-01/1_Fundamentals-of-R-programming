## Basic questions 

#### 1. Create a simple patient record list containing an ID ("P123"), age (45), and a single medication ("Metformin"). Print the list and access each element using different methods ($, [[]], [).

  <details>
  <summary>Click to view answer</summary>

  ```
  patient <- list(
    id = "P123",
    age = 45,
    medication = "Metformin"
  )
  ```

  and you can access the list by either one of these methods:

  ```
  print(patient$id)       
  print(patient[["age"]]) 
  print(patient["medication"])  
  ```

  </details>

#### 2. Given the following patient list, add a new blood_type element with value "B+" and print the updated list.

  <details>
  <summary>Click to view answer</summary>

  ```
  patient$blood_type <- "B+"
  print(patient)
  ```

  </details>

#### 3. Create a list of vital signs containing systolic (120), diastolic (80), and temperature (37.2). Calculate the mean of these values using unlist().

  <details>
  <summary>Click to view answer</summary>

  ```
  vitals <- list(
    systolic = 120,
    diastolic = 80,
    temperature = 37.2
  )

  mean_vitals <- mean(unlist(vitals))
  print(mean_vitals)
  ```

  </details>

#### 4. Given a patient medications list, add two new medications, Aspirin and Insulin, and print the updated list.

```
meds <- list(current = c("Metformin"))
```

  <details>
  <summary>Click to view answer</summary>

  ```
  meds$current <- c(meds$current, "Aspirin", "Insulin")
  print(meds)
  ```

  </details>

#### 5. Remove the age element from the following patient record and print the remaining elements:

```
patient <- list(
  id = "P001",
  age = 42,
  name = "John"
)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  patient$age <- NULL
  print(patient)
  ```

  </details>

#### 6. Given a list of vital signs, extract only the temperature value using different access methods:

```
vitals <- list(
  systolic = 120,
  diastolic = 80,
  temperature = 37.2
)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  temp1 <- vitals$temperature
  temp2 <- vitals[["temperature"]]
  ```

  </details>

#### 7. Create a list containing a patient's ID and a vector of the three blood pressure readings. Find the length of the entire list and the length of the blood pressure vector.

**The patient has the following details:**
**(a) ID: P001**
**(b) Blood pressure readings: 120, 122 and 118**

  <details>
  <summary>Click to view answer</summary>

  ```
  patient <- list(
    id = "P001",
    bp_readings = c(120, 122, 118)
  )
  list_length <- length(patient)  # 2
  bp_length <- length(patient$bp_readings)  # 3

  print(list_length)
  print(bp_length)
  ```

  </details>
