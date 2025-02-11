# 10. Conditionals and loops

## 10.1. If-else statements 

In R, if-else statements allow us to execute different code blocks based on specific conditions, making our programs capable of making decisions.

The basic syntax is as follows: 

```
if (condition) {
    # code to execute if condition is TRUE
} else {
    # code to execute if condition is FALSE
}
```

For example:

```
blood_pressure <- 140

if (blood_pressure >= 140) {
    print("Patient is hypertensive")
} else {
    print("Patient has normal blood pressure")
}
```

## 10.2. Loops 

Loops allow us to repeat operations multiple times, which is essential when working with large datasets or performing iterative analyses.

### 10.2.1 For loops

For loops iterate over a sequence of elements, executing code for each item.

The basic syntax is as follows:

```
for (item in sequence) {
    # code to execute
}
```

For example:

```
# Calculate BMI for multiple patients
patient_weights <- c(70, 85, 62, 91)
patient_heights <- c(1.75, 1.82, 1.65, 1.78)

for (i in 1:length(patient_weights)) {
    bmi <- patient_weights[i] / (patient_heights[i]^2)
    print(paste("Patient", i, "BMI:", round(bmi, 2)))
}
```

> [!NOTE]
> `paste()` is a function in R that concatenates/combines strings together.
>
> For example,
>
> ```
> greeting <- "Hello"
> name <- "John"
> message <- paste(greeting, name)
> print(message)
> ```

### 10.2.3 While loops

While loops continue executing until a condition becomes false, useful for situations where we don't know the exact number of iterations needed.

The basic syntax is as follows:

```
# Basic syntax
while (condition) {
    # code to execute
}
```

For example:

```
# Patient temperature monitoring
temperature <- 39.5  # Starting temperature (fever)

while (temperature > 37.5) {
    print(paste("Current temperature:", temperature))
    temperature <- temperature - 0.5  # Simulate temperature dropping
}
print("Temperature is now normal")
```
