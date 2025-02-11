## Basic Questions

#### 1. Create a numeric vector called gene_expression containing the following expression values: 1.2, 3.4, 2.1, 4.5, 1.8. Then print the vector and its class.

  <details>
  <summary>Click to view answer</summary>

  ```
  gene_expression <- c(1.2, 3.4, 2.1, 4.5, 1.8)
  print(gene_expression)
  class(gene_expression)
  ```
  
  </details>

#### 2. Create a numeric vector of mutation frequencies (0.05, 0.12, 0.08, 0.15) and assign gene names (BRCA1, TP53, KRAS, EGFR) to each value. Print the named vector.

  <details>
  <summary>Click to view answer</summary>

  ```
  mutation_freq <- c(0.05, 0.12, 0.08, 0.15)
  names(mutation_freq) <- c("BRCA1", "TP53", "KRAS", "EGFR")
  print(mutation_freq)
  ```
  
  </details>

#### 3. Given a vector of patient temperatures:

```
temps <- c(37.2, 38.5, 36.9, 37.8, 39.1)
```

**Calculate:**

**i. The mean temperature**
**ii. The max temperature**
**iii. The number of temperatures in the vector**
**iv. Put all the answers i-iii in a vector**

  <details>
  <summary>Click to view answer</summary>

  ```
  mean_temp <- mean(temps)
  max_temp <- max(temps)
  num_readings <- length(temps)
  answer_vector <- c(mean_temp, max_temp, num_readings)

  print(mean_temp)
  print(max_temp)
  print(num_readings)
  print(answer_vector)
  ```
  
  </details>

#### 4. Create the following as vectors and calculate the final expression levels by adding these two vectors. 

baseline treatment: 1.0, 2.0 and 1.5
treatment expression: 0.5, 0.7 and 0.3


  <details>
  <summary>Click to view answer</summary>

  ```
  baseline_expression <- c(1.0, 2.0, 1.5)
  treatment_effect <- c(0.5, 0.8, 0.3)
  final_expression <- baseline_expression + treatment_effect
  print(final_expression)
  ```
  
  </details>

#### 5. Given a vector of gene names as below:

```
genes <- c("BRCA1", "TP53", "KRAS", "EGFR", "HER2")
```

  <details>
  <summary>Click to view answer</summary>

  i. first_gene <- genes[1]
  ii. third_fourth <- genes[c(3,4)]
  iii. last_gene <- genes[length(genes)]
  
  </details>

#### 6. Create a vector of drug dosages and calculate double the dosage for each value. 

```
dosage <- c(2, 4, 6, 8)
```

  <details>
  <summary>Click to view answer</summary>

  doubled_dosage <- dosage * 2
  print(doubled_dosage)
    
  </details>

#### 7. Given a vector of gene expression values as below, find all values greater than 1.0.

  <details>
  <summary>Click to view answer</summary>

  expression <- c(0.5, 1.2, 2.1, 0.8, 1.7)
  high_expression <- expression[expression > 1.0]
  print(high_expression)
    
  </details>

#### 8. Combine two vectors of patient IDs into a single vector

```
group1 <- c("P01", "P02", "P03")
group2 <- c("P04", "P05")
```

  <details>
  <summary>Click to view answer</summary>

  all_patients <- c(group1, group2)
  print(all_patients)
    
  </details>
