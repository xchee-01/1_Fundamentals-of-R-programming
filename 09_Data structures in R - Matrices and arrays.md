# 9 Data structures in R - Matrices and arrays

Matrices and arrays are essential for handling multi-dimensional data, commonly used in genomics and biostatistics. A matrix is a two-dimensional data structure in R that organizes data in rows and columns, making it ideal for handling structured medical and biological data analysis.

## 9.1. Basic matrix creation

# Basic matrix creation with medical data

You can create a matrix like this:

```
manual_matrix <- matrix(c(1, 2, 3,
                          4, 5, 6,
                          7, 8, 9))

patient_data # to view the matrix
```

> [!NOTE]
> These line of codes
>
> ```
> manual_matrix <- matrix(c(1, 2, 3,
>                           4, 5, 6,
>                           7, 8, 9))
> ```
>
> and
>
> ```
> manual_matrix <- matrix(c(1, 2, 3, 4, 5, 6, 7, 8, 9))
> ```
>
> are the same. Both approaches will produce the same matrix
> R will automatically infer the dimensions of the matrix based on the length of the vector (9 elements) and create a 3x3 matrix filled by columns.
                    

You can assign names to the columns and rows of a data

```
colnames(patient_data) <- c("systolic", "diastolic", "glucose")
rownames(patient_data) <- c("patient1", "patient2", "patient3")

patient_data # to view the matrix
```

> [!NOTE]
> While matix and dataframes look similar, there is an important difference:
> -  A matrix can only contain elements of the same data type (e.g., all numeric or all character).
> -  A data frame can contain elements of different data types in each column (e.g., numeric, character, factor, etc.).

## 9.2. Basic array creation

You can create a 3D array like this:

```
patient_vitals <- array(
  data = c(
    # Baseline readings
    120, 130, 125,  # systolic
    80, 85, 82,     # diastolic
    95, 98, 94,     # glucose
    
    # Week 1 readings
    118, 128, 122,  # systolic
    79, 83, 80,     # diastolic
    94, 96, 93,     # glucose
    
    # Week 2 readings
    115, 125, 120,  # systolic
    78, 82, 79,     # diastolic
    93, 95, 92      # glucose
  ),
  dim = c(3, 3, 3)
)
```

> [!NOTE]
> In the case of a multidimensional array, you would have to specify the dimensions using `dim()` or else it will just be treated as a 1D array. 

And then assign the names of the 

```
dimnames(patient_vitals)[[1]] <- c("patient1", "patient2", "patient3")  # Rows
dimnames(patient_vitals)[[2]] <- c("systolic", "diastolic", "glucose")  # Columns
dimnames(patient_vitals)[[3]] <- c("baseline", "week1", "week2")        # Planes
```

