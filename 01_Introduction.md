# 1. R Programming

R is a programming language and environment specifically designed for statistical computing, data analysis, and graphical visualization. R packages are collections of functions, data, and documentation that extend R's basic functionality.

Here are the key things to know about R packages:

# 1.1. Installing packages 

Installing Packages

```
install.packages("package_name")
```

For example, you can install the popular tidyverse package 

```
install.packages("tidyverse")
```

# 1.2. Loading packages 

After installing, you would need to load packages in order to use it 

```
library(package_name)
```

For example, to load the tidyverse package, you would need to:

```
library(tidyverse)
```

R comes with several **pre-installed packages** like:

stats: Statistical functions
graphics: Basic plotting functions
base: Core R functions
utils: Utility functions


There are some popular **external packages** that are commonly used as well:


tidyverse: Collection of data science packages (includes ggplot2, dplyr, tidyr)
data.table: Fast data manipulation
shiny: Web application framework
caret: Machine learning workflows

# 1.3. Package management


To view the list of installed packages, you can type 

```
installed.packages()
```

At times, you might also need to update packages. To do so, you can:

```
update.packages()
```

To remove packages, you can:

```
remove.packages("package_name")
```

There are two ways of how you can seek help:
(a) To seek help from packages, you can:

```
help(package = "package_name")
```

or 

to get help for specific function

```
help("function_name")
```
