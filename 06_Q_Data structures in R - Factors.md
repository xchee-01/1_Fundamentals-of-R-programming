## Basic Question 

#### 1. Given the following patient data:

```
treatment_response <- c("Positive", "Negative", "Positive", "Positive", "Negative")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  response_factor <- factor(treatment_response)
  levels(response_factor)
  ```
  
  </details>

#### 2. Given the following factors, change the levels to be more descriptive: "High" to "Strong_Response", "Medium" to "Moderate_Response", and "Low" to "Weak_Response".

```
drug_response <- factor(c("High", "High", "Low", "Medium", "Low"))
```

  <details>
  <summary>Click to view answer</summary>

  ```
  levels(drug_response) <- c("Strong_Response", "Moderate_Response", "Weak_Response")
  drug_response
  ```
  
  </details>

#### 3. Create a factor for gene expression levels ("Low", "Medium", "High") and convert it to an ordered factor.

  <details>
  <summary>Click to view answer</summary>

  ```
  expression <- factor(c("Low", "High", "Medium", "Low", "High"))
  expression_ordered <- factor(expression, 
                             levels = c("Low", "Medium", "High"),
                             ordered = TRUE)
  ```
  
  </details>

#### 4. Create a factor of treatment outcomes, then combine "Partial_Response" and "Complete_Response" into a single level called "Responders".

  <details>
  <summary>Click to view answer</summary>

  ```
  outcomes <- factor(c("No_Response", "Partial_Response", "Complete_Response", 
                    "Partial_Response", "No_Response"))
  levels(outcomes)[levels(outcomes) %in% c("Partial_Response", "Complete_Response")] <- "Responders"
  table(outcomes)
  ```
  
  </details>
