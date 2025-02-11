# 11. Custom functions

Functions allow us to package code into reusable blocks, making our programs more organized and maintainable. They are essential for creating reproducible analysis pipelines.

Here is the basic syntax 

```
function_name <- function(argument1, argument2) {
    # Function body
    result <- # some computation
    return(result)
}
```

Here is an example:

```
# Custom function
calculate_drug_dose <- function(weight, age) {
    if (age < 18) {
        base_dose <- weight * 0.1
    } else {
        base_dose <- weight * 0.15
    }
    return(round(base_dose, 1))
}

# Usage
patient_dose <- calculate_drug_dose(weight = 70, age = 25)
```
