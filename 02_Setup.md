# 2 Setup

## 2.1. Installing R and R Studio as a standalone

R is a programming language specifically designed for statistical computing and data analysis, while RStudio is an integrated development environment (IDE) that makes it easier to work with R. Think of R as the engine that performs all the statistical calculations and data manipulations, while RStudio is the user-friendly interface that provides features like code editing, visualization, debugging, and project management. 

You need to have R installed to use RStudio, as RStudio simply provides a more convenient way to write, organize, and execute R code through features like syntax highlighting, code completion, variable viewing, and plot visualization all in one window.

You can install R and R studio [here](https://posit.co/download/rstudio-desktop/)

## 2.2. Installing R and R Studio in Anaconda

You can install R studio using Anaconda. 

## 2.3. Understanding the RStudio Interface 

The RStudio is divided into four main panels, each serving a different purpose. 

![RStudio Interface](https://github.com/xchee-01/1_Fundamentals-of-R-programming/blob/main/Images/Rstudios_interface.png)

**1. Script Editor:**

- Where you write and edit your R code
- Save scripts for future use
- Execute code line by line or in chunks

**2. Console:**

- Where code is executed and results are displayed
- Direct interaction with R
- Shows command history

**3. Environment/History:**

- Lists all objects (variables, functions) in memory
- Shows command history
- Displays available connections

**4. Files/Plots/Packages/Help:**

- Browse files and working directory
- View plots and visualizations
- Manage packages
- Access help documentation


## 2.4. How to keep your RStudio workspace tidy

**(a) Clearing variables**

```
# Remove a specific variable
rm(variable_name)

# Remove multiple variables
rm(var1, var2, var3)

# Remove all variables in the current environment
rm(list = ls())
```

**(b) Clear workspace**

```
rm(list = ls())
```

**(c) Clear console**

You can clear console using Ctrl + L 
