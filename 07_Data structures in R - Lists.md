# 7. Data structures in R - Lists

Lists are versatile containers that can hold elements of different types and lengths, making them perfect for storing heterogeneous medical data.

# 7.1. Lists 

Lists are versatile containers that can hold elements of different types and lengths, making them perfect for storing heterogeneous medical data.

```
patient_record <- list(id = "P001", vital_signs = c(120, 80, 37.2), medications = c("Aspirin", "Metformin"))
```

This can be written more clearly as:

```
patient_record <- list(
  id = "P001",
  vital_signs = c(120, 80, 37.2),
  medications = c("Aspirin", "Metformin"),
  age = 42
)
```

> [!NOTE]
> The terminologies in R are slightly different than Python.
> `patient_record` is a list
> `id` is a name or an identifier
> `P001` is the value (this is normally referred to as 'element')
> `id = "P001"` is called a name-value pair or named component or key-value pair

# 7.2. More about accessing elements in lists

Let's take an example of a simple list 

```
my_list <- list(
    numbers = c(1, 2, 3),
    letters = c("a", "b", "c"),
)
```

You can access the elements like these:

```
my_list[1]
my_list[[1]]
my_list[['numbers']]
my_list$numbers
```

> [!CAUTION]
> Do you see the difference between the output of the codes above?
>
> Let's try and find out the data type of the output.
>
> class(list_name[1])
> class(list_name[[1])
> class(list_name$numbers)

Think of it this way:

- Single bracket [1] is like opening a box and taking out a smaller box
- Double bracket [[1]] is like opening a box and taking out what's actually inside

You'd use [[]] when you want to:

- Access the actual content
- Perform operations on the element
- Pass the element to a function

You'd use [] when you want to:

- Keep the list structure
- Extract multiple elements
- Maintain the names/attributes

If you would to access the individual elements, you would have to use syntax like the following:

```
my_list[[1]][1]
```

or 

```
my_list$numbers[1]
```

or 

```
my_list[["numbers"]][1]
```

# 7.3. Lists manipulation

Lists can be modified, extended, and combined, making them powerful tools for managing evolving datasets.

Coming back to our earlier example:

```
patient_record <- list(
  id = "P001",
  vital_signs = c(120, 80, 37.2),
  medications = c("Aspirin", "Metformin"),
  age = 42
)
```

We can **extend** the list using the following:

```
patient_record$blood_type <- "A+"
patient_record$medications <- c(patient_record$medications, "insulin")

print(patient_record)
```


We can also **delete** a key-value pair in the list by:

```
patient_record$age <- NULL  # Remove age information
```

> [!NOTE]
> In R, assigning NULL to a column of a data frame effectively removes that column from the data frame.

# 7.4. List operations and functions 

R provides various functions to work with lists efficiently, enabling complex data analysis and manipulation.

Here are some of the common functions:

```
length()    # Number of elements in list
names()     # Names of list elements
unlist()    # Convert list to vector
lapply()    # Apply function to all elements
```

Applying to our example:

```
length(patient_record)
names(patient_record)
unlist(patient_record)
lapply(patient_record, length)
```

You can also update an element inside the list.

For example:

```
patient_record[['vital_signs']] <- patient_record[['vital_signs']] * 2
```

# 7.5. Nested list

Lists can contain other lists, allowing for hierarchical data organization. This is particularly useful in complex medical and genomic data structures.

This is the basic structure:

```
nested_list <- list(
    outer_element = list(
        inner_element1 = value1,
        inner_element2 = value2
    )
)
```

For example:

```
# Complex patient record
patient_complex <- list(
    demographics = list(
        id = "P001",
        age = 45,
        gender = "F"
    ),
    clinical_data = list(
        vitals = c(120, 80, 98.6),
        medications = c("aspirin", "metformin")
    )
)
```


