# 4. Data types in R

Understanding data types in R is fundamental for handling medical and molecular data effectively. R provides various data types that help us organize and manipulate different kinds of information, from patient records to genomic data.

## 4.1. Numeric data types 

**(a) Double (numeric)**
The default numeric type in R, used for decimal numbers and precise measurements.

```
patient_temperature <- 37.5  # Body temperature in Celsius
```

> [!NOTE]
> You can use `class` to find out the data type.
> For example, using the example above,
>
> ```
> patient_temperature <- 37.5
> class(patient_temperature)
> ``` 

**(b) Integer**
Whole numbers **without** decimal points, useful for counting discrete occurrences.

```
heart_rate <- 72L
```

## 4.2. Character (string) data

Character data types store text information, crucial for maintaining patient information and molecular annotations.

```
patient_name <- "John Doe"
blood_type <- "A+"
```

## 4.3. Boolean data 

Logical values represent true/false conditions, useful for filtering and conditional operations.

```
is_diabetic <- TRUE
has_hypertension <- FALSE
```

## 4.4. Factor data 

Factors represent categorical data with predefined levels, commonly used in clinical classifications and molecular annotations. It is a very unique data type in R. 

For example:

```
disease_stage <- factor(c("Stage I", "Stage II", "Stage III", "Stage IV"))
```

or 

```
variant_impact <- factor(
  c("High", "Moderate", "Low"),
  levels = c("Low", "Moderate", "High"),
  ordered = TRUE
)
```

Factors are super useful when you want to:

- Organize categorical data (like blood types: A, B, AB, O)
- Ensure categories stay in a specific order (like size: Small, Medium, Large)
- Analyze data by groups (like comparing test scores between different grade levels)

The cool thing about factors is that R will automatically handle them appropriately in statistical analyses and plots, making your data analysis much smoother.

For example 

```
# Create a vector of gene expression levels
gene_expression <- c("High", "Medium", "Low", "High", "High", "Medium", 
                    "Low", "High", "Medium", "High", "Low", "Medium")

# Convert to ordered factor (Low < Medium < High)
expression_factor <- factor(gene_expression, 
                          levels = c("Low", "Medium", "High"), 
                          ordered = TRUE)

# Count frequency of each expression level
table(expression_factor)
```

> [!NOTE]
> Refering back to the examples above,
> `levels = c("Low", "Medium", "High")` tells R these are the only **valid categories** allowed and the **exact specific order** we want them in
> `ordered = True` tells R that these levels have a meaningful order (Low < Medium < High)

## 4.5. Data and time data 

Temporal data types are crucial for tracking patient histories and experimental timelines.

```
admission_date <- as.Date("2024-02-06")
```

or 

```
sequencing_date <- as.Date("2024-02-06")
```
