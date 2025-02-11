# 3 Basics of R

## 3.1. Basic Arithmetc Operations 

> [!NOTE]
> The run the codes below, you can do Ctrl+Enter 10-

```
# Basic arithmetic
5 + 3    # Addition
10 - 4   # Subtraction
6 * 2    # Multiplication
15 / 3   # Division
2 ^ 3    # Exponents
17 %% 5  # Modulus (remainder)
```

Here is an example of how we can apply this in a medical context:

```
# Calculating BMI
weight_kg <- 70
height_m <- 1.75
bmi <- weight_kg / (height_m^2)
print(bmi)
```

> [!NOTE]
> In R, <- is the assignment operator, which is used to assign values to variables. It's equivalent to the = operator that's commonly used in many other programming languages like Python.
> Hence, `weight_kg <- 70' means the value 70 is assigned to the variable name `weight_kg`
> 
> Also note that once you have done this, the variable is reflected in the variable.

> [!TIP]
> It is also possible to use the `=` for variable assignment as well.
>
> For example, the following is the same. 
>
> ```
> patient_age <- 45
> patient_age = 4
> ```

> [!NOTE]
> **Running Code in RStudio:**
>
> **Running Single Lines:**
> 
> Place your cursor on any line and press Ctrl + Enter (Windows/Linux) or Cmd + Enter (Mac)
> RStudio will execute just that line
> The cursor automatically moves to the next line
> 
> **Running Multiple Lines:**
> 
> Highlight the lines you want to run
> Press Ctrl + Enter to execute all highlighted lines
> 
> **Running Entire Script:**
> 
> Press Ctrl + Shift + R (Windows/Linux) or Cmd + Shift + R (Mac) to run the whole script at once
> This executes all lines from top to bottom

## 3.2. Getting Help in R

R provides extensive documentation and help features that are essential for learning and troubleshooting.

**(a) You can view function documentation**

```
?mean  # Opens help for mean function
help("median")  # Alternative way (syntax) of seeking help
```

**(b) Search for help topics**

```
??correlation  # Search for topics containing "correlation"
```

**(c) Access package vignettes**

A vignette in R is a long-form documentation or tutorial that shows how to use an R package. Think of it as a detailed guide that demonstrates the functionality of a package through examples and explanations.

```
vignette()  # List all available vignettes
vignette("dplyr")  # View specific package vignette
```
