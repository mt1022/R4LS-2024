## Exercises for "Introduction to R"

### Data Vector Creation and Manipulation

- Create a numeric vector `fav_numbers` with elements 3.14, 1.61, 2.71, and 4.15.
- Perform vector arithmetic to create a new vector `doubled` which is each element of `fav_numbers` multiplied by 2.

### Generating Sequences

- Use the `seq()` function to generate a sequence of integers from 1 to 100 with a step of 5, and store it in `seq_five`.
- Create a descending sequence from 100 to 1 using the colon operator and store it in `desc_seq`.


### Logical Vectors and Conditions

- Create a numeric vector temps with elements 22, 19, 24, 18, 21, and use logical vectors to filter out temperatures above 20 degrees, storing the result in `hot_days`.
- Use logical operators to create a vector `moderate_temps` that includes only temperatures between 18 and 22 degrees.

### Handling Missing Values

```r
x <- c(1, 2, NA, 4, 5)
```

Replace missing values in `x` with the mean of the non-missing values using `is.na()` and `mean()`.

### Character Vector Operations

- Construct a character vector `fruits` containing "Apple", "Banana", "Cherry", and "Date".
- Use `paste()` to create a sentence for each fruit, such as "I like to eat Apple", and store in `fruit_sentences`.

### Indexing and Subsetting Data

- Create a data frame `df_airports` with the following details for airports:
    - Name: "Heathrow", "Charles de Gaulle", "JFK International"
    - City: "London", "Paris", "New York"
    - Country: "United Kingdom", "France", "USA"
- Extract the row for Paris using indexing and store it in `paris_airport`.


### Matrix and Array Operations

- Create a matrix `mat_grades` with random scores for 4 students in 3 subjects.
- Perform matrix multiplication with a vector of subject weights `c(0.4, 0.3, 0.3)` and store the result in `weighted_scores`.

### Factor Analysis
```r
blood_types <- c("A", "B", "AB", "O", "A", "O", "B", "AB", "A", "B")
ages <- c(30, 25, 35, 40, 22, 45, 32, 28, 31, 37, 29)
```

Calculate the mean age for each blood type from a vector ages associated with each type.

### List and Data Frame Manipulation
```r
my_list <- list(
  Name = "John Doe",
  Age = 30,
  Scores = c(88, 92, 79, 65),
  Contact = list(Email = "john.doe@example.com", Phone = "123-456-7890")
)
```
Extract the phone number of John Doe from the list `my_list` and store it in `phone_number`.

### Writing Custom Functions
Create a function `simple_lm` that fits a linear model to provided data in vectors x and y and returns the summary statistics of the model.

Example usage:
```r
set.seed(2024)
x <- 1:10
y <- x * 2 + rnorm(10) # y is approximately 2 times x with some noise
model_summary <- simple_lm(x, y)

print(model_summary)
```

expected output:
```
Call:
lm(formula = y ~ x)

Residuals:
    Min      1Q  Median      3Q     Max 
-0.7844 -0.6042 -0.1298  0.5074  1.2146 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept)  1.11428    0.51691   2.156   0.0632 .  
x            1.82725    0.08331  21.934 1.97e-08 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.7567 on 8 degrees of freedom
Multiple R-squared:  0.9836,	Adjusted R-squared:  0.9816 
F-statistic: 481.1 on 1 and 8 DF,  p-value: 1.97e-08
```
