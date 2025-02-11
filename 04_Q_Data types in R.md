## Basic questions

#### 1. What will be the output of the following code? Before trying it out on R, can you predict what would the output be?

```
blood_pressure <- 120.5
class(blood_pressure)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  `numeric`
  ```
  
  </details>

#### 2. Create a vector of patient IDs (P001, P002, P003) and determine its class. Before trying it out on R, can you predict what would the output be?

```
patient_ids <- c("P001", "P002", "P003")
class(patient_ids)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  `character`
  ```
  
  </details>

#### 3. Create a logical vector indicating whether patients have diabetes. Before trying it out on R, can you predict what would the output be?

```
diabetes_status <- c(TRUE, FALSE, TRUE, FALSE)
length(diabetes_status)
class(diabetes_status)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  [1] 4
  [1] "logical"
  ```
  
  </details>

> [!TIP]
> In R, when you see [1] at the beginning of output lines, it's simply indicating the index position of the first element shown in that line of output. It's a way to help you keep track of element positions in vectors or other data structures, especially when the output spans multiple lines.
>
> For example:
>
> ```
> [1]  1  2  3  4  5  6  7  8  9 10
> [11] 11 12 13 14 15 16 17 18 19 20
> ```
>
> Here, `[1]` means the line starts with the 1st element and `[11]` means the line starts with the 1st element

#### 4. What is the output of this factor creation and its levels? Before trying it out on R, can you predict what would the output be?

```
cancer_stages <- factor(c("Stage I", "Stage II", "Stage I", "Stage III"))
levels(cancer_stages)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  [1] "Stage I"  "Stage II" "Stage III"
  ```
  
  </details>

#### 5. Convert this numeric temperature data to integer. What's the class? Before trying it out on R, can you predict what would the output be?

```
temp <- 37
class(temp)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  [1] "numeric"
  ```
  
  </details>

> [!NOTE]
> What is the difference between these two codes?
>
> ```
> temp <- 37
> class(temp)
> ```
>
> with
>
> ```
> temp <- 37L
> class(temp)
> ```
>
> You can read more [here](https://rpubs.com/STEMResearch/data-types-in-r#:~:text=There%20are%20two%20ways%20to%20declare%20a,space)) under the section of integer

> [!TIP]
> Why should i care if i am using integers or numerics? Arent they the same?
>
> Integers only store whole numbers and use half the memory of numerics, making them more memory-efficient for large datasets.
>
> Numerics (also called doubles) can store decimal values and very large or small numbers, offering more flexibility but taking up more space.
>
> Try the code below to check the storage size of integer and numeric:
> 
> ```
> x <- 1:1000000L  # integer
> y <- as.numeric(1:1000000)  # numeric
> object.size(x)  
> object.size(y)  
> ```

#### 6. What's the output of this factor table? Before trying it out on R, can you predict what would the output be?

```
mutation_impact <- factor(c("High", "Low", "Medium", "High", "Low"))
table(mutation_impact)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  High  Low Medium 
   2    2      1
  ```
  
  </details>



