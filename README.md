# Cars Machine Learning Project

## Mandatory Assignment 1

**For your Mandatory Assignment 1 you must do the following**:

- obtain the cars.csv file from the course materials folder in the course materials repository
- using the dataset found in the file, complete the tasks below:
  - formulate a regression problem
  - formulate a logistic regression problem
  - design and train a model for each of the regression and logistic regression problems
  - fine tune your models
  - answer your problem formulations
  - write a max two page research article (in [Latex](https://gitlab.com/keaorg/kea-aai-latex-demo)) with relevant visuals

**Submit the following to the [code share repository](https://gitlab.com/keaorg/kea-aai-codeshare-2025-2)**:
- article in PDF
- all project files, including notebooks, .tex file, etc.

Follow the directions for submission in the assignments repository README.md file.

Your submission should not include large datasets, but clearly document how to obtain such files if necessary.

**Part 1**: project as listed above, due **October 24, 08:00 morning**.

**Part 2**: peer review of two other groups, due **October 31, 08:00 morning**.

## Column descriptions in Car dataset

| Column Name     | What It Means                                                                 |
|-----------------|--------------------------------------------------------------------------------|
| **mpg**         | *Miles per gallon* — a measure of fuel efficiency. Higher values = better fuel economy. |
| **cylinders**   | Number of cylinders in the engine. More cylinders often mean more power, but lower fuel efficiency. |
| **displacement**| Engine size in cubic inches. Larger displacement usually means a more powerful engine. |
| **horsepower**  | The engine’s power output. Higher horsepower = faster acceleration and higher speed potential. |
| **weight**      | Vehicle weight in pounds. Heavier cars may be less fuel-efficient and slower to accelerate. |
| **acceleration**| Time (in seconds) to go from 0 to 60 mph. Lower values = quicker acceleration. |
| **model year**  | The year the car model was released. In your data, it's coded as two digits (e.g., 70 = 1970). |
| **origin**      | Country of origin: `1` = USA, `2` = Europe, `3` = Japan |
| **car name**    | The full name of the car, including brand and model. Useful for identification or grouping. |

## Problem formulations

### Regression Problem Example

**Goal**: Predict a car’s fuel efficiency (`mpg`) based on its physical and performance characteristics.

**Problem Statement**:  
> *Given features like `cylinders`, `displacement`, `horsepower`, `weight`, and `acceleration`, predict the car's `mpg` (miles per gallon).*

**Why it works**:  
- `mpg` is a continuous numeric value.
- You're modeling how engine size, power, and weight influence fuel efficiency.
- This is a classic linear regression setup, and you could explore regularization (Ridge/Lasso) or tree-based models if needed.

**Example input row**:
```csv
8,455,225,4425,10
```
**Predicted output**:
```csv
14.2 mpg
```

### Logistic Regression Problem Example

**Goal**: Classify whether a car is **American-made** or **foreign-made**.

**Problem Statement**:  
> *Using features like `cylinders`, `displacement`, `horsepower`, `weight`, and `acceleration`, predict whether the car's `origin` is 1 (USA) or not (foreign).*

**Why it works**:  
- You convert `origin` into a binary label:  
  - `1` → American  
  - `0` → Foreign (i.e., origin = 2 or 3)
- Logistic regression is ideal for binary classification.
- You can analyze which features most influence whether a car is American-made.

**Example input row**:
```csv
4,113,95,2372,15
```
**Predicted output**:
```csv
0 → Foreign-made
```

## TODO and homework

> For Friday the 17th of October, at least the basic design of the model should be finished.

**Nathasja**
- formulate a regression problem
  - write the problem (like above)
  - Make a hypothesis
  - Make a null hypothesis
- design and train a model for the regression problem
- fine tune your model
- answer your problem formulation

**Ane**
- formulate a logistic regression problem
  - write the problem (like above)
  - Make a hypothesis
  - Make a null hypothesis
- design and train a model for the logistic regression problem
- fine tune your model
- answer your problem formulation

