## Basic questions

#### 1. Create a function that classifies patients as "Normal" or "Hypertensive" based on their blood pressure.

```
blood_pressures <- c(135, 142, 128, 150)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  for (bp in blood_pressures) {
      if (bp >= 140) {
          print(paste("Blood Pressure:", bp, "- Hypertensive"))
      } else {
          print(paste("Blood Pressure:", bp, "- Normal"))
      }
  }
  ```
  
  </details>

#### 2. Calculate drug dosage based on patient weight (mg/kg). The patients' weights are 65, 72, 88, 45, 91 in kgs. The rule for drug dosage is 2.5mg per kg of body weight. Write a code to print out the dosage that each patient should receive for the drug. 

```
weights <- c(65, 72, 88, 45, 91)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  for (weight in weights) {
      dosage <- weight * 2.5
      print(paste("Patient weight:", weight, "kg - Required dosage:", dosage, "mg"))
  }
  ```
  
  </details>

#### 3. Create a BMI calculator that categorizes patients. The categories are Underweight (<18.5), Normal (18.5-24.9), Overweight (25-29.9), Obese (≥30). You may use the data below.

```
heights <- c(1.75, 1.68, 1.82, 1.60)
weights <- c(68, 55, 95, 52)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  for (i in 1:length(heights)) {
      bmi <- weights[i] / (heights[i]^2)
      if (bmi < 18.5) {
          category <- "Underweight"
      } else if (bmi < 25) {
          category <- "Normal"
      } else if (bmi < 30) {
          category <- "Overweight"
      } else {
          category <- "Obese"
      }
      print(paste("Patient", i, "BMI:", round(bmi, 2), "-", category))
  }
  ```
  
  </details>

#### 4. Classify drug response based on reduction in tumor size for the different patients are. The classifications are No Response (<10%), Partial Response (10-50%), Complete Response (>50%). The reduction in tumours for the different patients are 5, 25, 60, 15, 80 in %. 

  <details>
  <summary>Click to view answer</summary>

  ```
  reductions <- c(5, 25, 60, 15, 80)
  for (reduction in reductions) {
      if (reduction < 10) {
          response <- "No Response"
      } else if (reduction <= 50) {
          response <- "Partial Response"
      } else {
          response <- "Complete Response"
      }
      print(paste("Tumor reduction:", reduction, "% -", response))
  }
  ```
  
  </details>

#### 5. Create a function that classifies patients into age groups of Pediatric (0-17), Adult (18-64), Elderly (65+). The ages of these patients are: 15, 45, 72, 8, 55, 68. Write a code to print age and corresponding group for each patient.

  <details>
  <summary>Click to view answer</summary>

  ```
  ages <- c(15, 45, 72, 8, 55, 68)
  for (age in ages) {
      if (age < 18) {
          group <- "Pediatric"
      } else if (age < 65) {
          group <- "Adult"
      } else {
        group <- "Elderly"
      }
      print(paste("Age:", age, "- Group:", group))
  }
  ```
  
  </details>
