# 5 Data structures in R

Data structures are fundamental building blocks in R that help us organize and manage different types of data efficiently. In this lecture, we'll explore the various data structures available in R, understanding their unique characteristics and practical applications in medical research.

## 5.1. Vectors

Vectors are the simplest and most fundamental data structure in R, serving as one-dimensional arrays that can hold elements of the same type.

**(a) Numeric vectors**

```
# Basic medical example
patient_temperatures <- c(37.2, 38.1, 36.9, 37.5)
mean(patient_temperatures)  # Calculate average temperature

# Precision medicine example
gene_expression_levels <- c(0.45, 1.23, 0.78, 2.01)
names(gene_expression_levels) <- c("BRCA1", "TP53", "EGFR", "HER2")
```

> [!NOTE]
> You can easily create vectors like this
>
> ```
> numbers <- c(1:10)
> print(numbers)
> ```

**(b) Character vectors**

```
# Basic medical example
patient_conditions <- c("Hypertension", "Diabetes", "Asthma")

# Precision medicine example
mutation_types <- c("Missense", "Frameshift", "Silent", "Nonsense")
```

In R, `c()` is a function used to combine values into a vector (a one-dimensional array). 

The 'c' stands for 'combine' or 'concatenate' 

You can try the following:

```
# This won't work - will cause an error
patient_temperatures = 37.2, 38.1, 36.9, 37.5

# This works - creates a vector
patient_temperatures <- c(37.2, 38.1, 36.9, 37.5)
```

## 5.1.1. Vector functions

If given a vector:

```
numbers <- c(10, 20, 30, 40, 50)
```

Here are some of the vector functions:

```
length(numbers)  # Number of elements
sum(numbers)     # Sum of all elements
mean(numbers)    # Average
max(numbers)     # Maximum value
min(numbers)     # Minimum value
```

## 5.1.2. Adding to vectors 

You can add more items to vectors 

```
numbers <- c(1, 2, 3, 4, 5)
more_number <- c(numbers, 6, 7, 8)
more_number
```

or you can also combine two vectors together

```
vector1 <- c(1, 2, 3)
vector2 <- c(4, 5, 6)
combined <- c(vector1, vector2)
combined
```

You can also combine different vectors with different data types:

```
mixed <- c(1, "hello", TRUE)
```

> [!NOTE]
> However, in a vector with different data types, the vector would become a 'character' type.
>
> ```
> # Numeric vector
> num <- c(1, 2, 3)
> class(num)
>
> # Character vector
> char <- c('a', 'b', 'c')
> class(char)
> 
> # Concatenate vector
> mixed <- c(num, char)
> print(mixed)
> class(mixed)
> ```

## 5.1.3. Operations with vectors

Let's imagine we have two vectors as below:

```
v1 <- c(2, 4, 6, 8)
v2 <- c(1, 2, 3, 4)
```

**(a) Addition and Subtraction**

You can add/subtract to each element

```
v1 + 1
```

or if you want to add the elements in the vector together

```
v1 + v2
```

**(b) Division**

```
division <- v1 / v2
```

**(c) Multiplication using dot product**

```
product <- v1 * v2
```

**(d) Multiplication using element-by-element operations with a single number**

```
double <- v1 * 2
```

## 5.1.4. Accessing vector elements

Let's imagine you have a vector like this 

```
scores <- c(85, 92, 78, 95, 88)
```

You can access the first element like this

```
scores[1]
```

> [!CAUTION]
> Unlike Python, R indexing starts at 1, not 0.

You can also access multiple elements like this 

```
scores[c(1, 3, 5)]  # Gets first, third, and fifth elements
```

And you can also get elements using conditionals

```
scores[scores > 90]  # Gets all scores above 90
```

