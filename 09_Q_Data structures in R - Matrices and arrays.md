## Basic questions 

#### 1. Create a 3x3 matrix containing patient blood pressure readings (systolic): 120, 130, 115, 125, 135, 120, 130, 125, 120. Name the rows as "patient1", "patient2", "patient3" and columns as "morning", "afternoon", "evening".

> [!NOTE]
> If you need a refresher, you may refer [here](https://www.geeksforgeeks.org/r-matrices/). 

  <details>
  <summary>Click to view answer</summary>

  ```
  bp_matrix <- matrix(c(120, 130, 115, 125, 135, 120, 130, 125, 120), nrow=3)
  rownames(bp_matrix) <- c("patient1", "patient2", "patient3")
  colnames(bp_matrix) <- c("morning", "afternoon", "evening")
  bp_matrix
  ```
  
  </details>

#### 2. Using the matrix above, how would you:

> [!NOTE]
> This is not explicitly taught in the learning materials so that you can get used to learning from documentations:
> Here are some resources that you can turn to to learn how to extract data from matrices:
> (a) [Extract Values from Matrix by Column and Row Names in R](https://www.geeksforgeeks.org/extract-values-from-matrix-by-column-and-row-names-in-r/)
> (b) [Accessing Elements in R Matrix](https://sparkbyexamples.com/r-programming/accessing-elements-in-r-matrix/0

**(a) Extract the morning reading for patient 2?**
**(b) Extract all evening readings?**

  <details>
  <summary>Click to view answer</summary>

  ```
  # a) Morning reading for patient2
  bp_matrix["patient2", "morning"]  # Returns 130

  # b) All evening readings
  bp_matrix[, "evening"]  # Returns c(120, 120, 120)
  ```
  
  </details>

#### 3. Given the following patient vitals matrix:

```
vitals_matrix <- matrix(c(
  120, 130, 125, 
  80, 85, 82,     
  95, 98, 94      
), nrow=3, byrow=TRUE)
rownames(vitals_matrix) <- c("systolic", "diastolic", "glucose")
colnames(vitals_matrix) <- c("patient1", "patient2", "patient3")
```

**How would you:**
**(a) Access the glucose level for patient 2?**
**(b) Access the systolic reading for patient 3?**
**(c) Access the diastolic reading for patient 1?**

  <details>
  <summary>Click to view answer</summary>

  ```
  # a) Glucose for patient2
  vitals_matrix["glucose", "patient2"]  

  # b) Systolic for patient3
  vitals_matrix["systolic", "patient3"]  

  # c) Diastolic for patient1
  vitals_matrix["diastolic", "patient1"]  
  ```
  
  </details>
