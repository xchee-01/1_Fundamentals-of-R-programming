# 6 Data structures in R - Factors 

Previously, we have had a quick overview of factors. Let's explore this a bit more. As a reminder, factors are R's way of storing categorical variables - data that falls into distinct categories or levels. In medical research, they are essential for organizing patient characteristics, treatment groups, and genetic variants.  

# 6.1. [REMINDER] Creating factors

We can create factors like this:

```
# Basic medical example
patient_status <- factor(c("Healthy", "Sick", "Healthy", "Recovered"))

# Molecular precision medicine example
mutation_status <- factor(c("Wild_Type", "BRCA1_Mutant", "Wild_Type", "BRCA2_Mutant"))
```

We can also view the different levels of factors:

```
# Check levels of patient status
levels(patient_status)

# Check mutation status levels
levels(mutation_status)
```

> [!NOTE]
> `levels()` in R factors are like categories or unique groups in your data

# 6.2. [REMINDER] Ordered factors 

Ordered factors represent categorical data with a natural ordering, common in disease staging or drug response measurements.

```
# Basic medical example
disease_stage <- factor(c("Stage_I", "Stage_II", "Stage_III"), 
                       levels = c("Stage_I", "Stage_II", "Stage_III"),
                       ordered = TRUE)

# Molecular medicine example
drug_response <- factor(c("No_Response", "Partial_Response", "Complete_Response"),
                       levels = c("No_Response", "Partial_Response", "Complete_Response"),
                       ordered = TRUE)
```

# 6.3. Modifying factors 

We can change the factor levels. 

```
# Basic medical example
treatment_group <- factor(c("Control", "Treatment_A", "Treatment_B"))
levels(treatment_group) <- c("Placebo", "Drug_X", "Drug_Y")

# Molecular example
variant_type <- factor(c("SNP", "Deletion", "Insertion"))
levels(variant_type) <- c("Single_Nucleotide_Variant", "Deletion_Variant", "Insertion_Variant")
```

We can also combine different levels. 

For example, 

```
# Create factor with ene expression levels
expression <- factor(c("Very_High", "High", "Medium", "Low", "Very_Low", "Very_High", "Very_High", "Low", "High", "Medium", "Low", "Very_Low"))
table(expression)

# Combine "Very_High" and "High" into "High_Expression"
# And combine "Low" and "Very_Low" into "Low_Expression"
levels(expression)[levels(expression) %in% c("Very_High", "High")] <- "High_Expression"
levels(expression)[levels(expression) %in% c("Low", "Very_Low")] <- "Low_Expression"

# Check new levels
levels(expression)  
table(expression)
```

To make it ordered, we can use this code:

```
expression_ordered <- factor(expression, 
                           levels = c("Low_Expression", "Medium", "High_Expression"),
                           ordered = TRUE)
table(expression_ordered)
```
