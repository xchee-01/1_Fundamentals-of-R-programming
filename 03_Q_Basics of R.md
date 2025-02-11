## Basic questions

#### 1. Calculate the total number of patients if there are 45 patients in Ward A and 32 patients in Ward B.

  <details>
  <summary>Click to view answer</summary>

  ```
  ward_A <- 45
  ward_B <- 32
  total_patients <- ward_A + ward_B
  print(total_patients
  ```
  
  </details>

#### 2. If a hospital starts the day with 100 test tubes and uses 37 throughout the day, how many test tubes remain?

  <details>
  <summary>Click to view answer</summary>

  ```
  initial_tubes <- 100
  used_tubes <- 37
  remaining_tubes <- initial_tubes - used_tubes
  print(remaining_tubes)
  ```
  
  </details>

#### 3. If each patient needs 3 doses of medication per day, how many total doses are needed for 25 patients?

  <details>
  <summary>Click to view answer</summary>

  ```
  doses_per_day <- 3
  number_of_patients <- 25
  total_doses <- doses_per_day * number_of_patients
  print(total_doses)
  ```
  
  </details>

#### 4. If you have 100mL of solution that needs to be divided equally among 4 test tubes, how many mL will be in each tube?

  <details>
  <summary>Click to view answer</summary>

  ```
  total_solution <- 100
  number_of_tubes <- 4
  solution_per_tube <- total_solution / number_of_tubes
  print(solution_per_tube)
  ```

  </details>

#### 5. If a bacterial culture doubles every generation, how many bacteria will there be after 4 generations if you start with 5 bacteria?

  <details>
  <summary>Click to view answer</summary>
    
  ```
  initial_bacteria <- 5
  generations <- 4
  final_bacteria <- initial_bacteria * (2 ^ generations)
  print(final_bacteria)
  ```

  </details>


#### 6. If a lab technician needs to prepare a solution that requires 2.5mL for each test, and they need to run the test in triplicate for 6 patients, how many mL of solution should they prepare? (Include 10% extra volume for pipetting errors)

  <details>
  <summary>Click to view answer</summary>

  ```
  ml_per_test <- 2.5
  tests_per_patient <- 3
  number_of_patients <- 6
  safety_factor <- 1.1

  total_volume <- ml_per_test * tests_per_patient * number_of_patients * safety_factor
  print(total_volume)
  ```

  </details>

#### 7. Calculate the final concentration if you add 5mL of a 2mg/mL _stock_ solution to 15mL of _new_ solution. Print out the answer

> [!NOTE]
> If you need to refresh your knowledge on dilution, you may refer [here](https://www.quansysbio.com/support/dilutions-explanations-and-examples/#:~:text=To%20make%20a%20fixed%20amount,Final%20volume%20of%20new%20solution)

  <details>
  <summary>Click to view answer</summary>
    
  ```
  # Given values
  initial_concentration <- 2  # mg/mL
  initial_volume <- 5        # mL
  final_volume <- 20        # mL

  # Calculate final concentration
  # Using C1V1 = C2V2
  final_concentration <- (initial_concentration * initial_volume) / final_volume

  print(paste0("Final concentration: ", final_concentration, " mg/mL"))
  ```

  </details>

> [!NOTE]
> What is the difference between `paste()` and paste0() `?
>
> Try it out:
>
> ```
> paste('df', 1:6)
> ```
>
> and
>
> ```
> paste0('df', 1:6)
> ```
>
> You can highly encouraged to read more [here](https://www.digitalocean.com/community/tutorials/paste-in-r)
