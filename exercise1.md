---
layout: default
title: JASP Practice Statistics
category : relationship testing
subcategory: correlation Example 1
---
### [<BACK](/index.md)
# Practice Exercises in Jasp and Python

JASP Practice Statistics : https://jasp-stats.org

    1.	RELATIONSHIP TESTING
    
a)	Correlation Example 1

Do heavier athletes have larger maximums in the bench press?

|     Athlete:     |    A   |    B   |   C   |    D   |    E   |    F   |    G   |
|:----------------:|:------:|:------:|:-----:|:------:|:------:|:------:|:------:|
| Bench press (kg) | 127.52 | 169.62 | 226.2 | 143.91 | 169.73 | 177.36 | 183.51 |
|    Weight (kg)   |  64.36 |  69.58 |  70.1 |  71.48 |  76.53 |  70.98 |  72.47 |


NULL Hypothesis, H0:

EXPERIMENTAL Hypothesis, H1:

---
First thing to do before to work on JASP is to create a .CSV file.  

*NB: The table needs to be arraged different. However, the function in excel (Paste Special) 'Transpose' helps.

---


```Python
import pandas as pd

tabla_df = pd.read_csv('jasp_practice_1.csv', index_col=0)

tabla_df

```

---


| Athlete: | Bench press (kg) | Weight (kg) |
|:--------:|:----------------:|:-----------:|
|     A    |      127.52      |    64.36    |
|     B    |      169.62      |    69.58    |
|     C    |      226.20      |    70.10    |
|     D    |      143.91      |    71.48    |
|     E    |      169.73      |    76.53    |
|     F    |      177.36      |    70.98    |
|     G    |      183.51      |    72.47    |


>

#### JASP Descriptive Results:


<img src="./images/Jaspdescriptive1.png" alt="drawing" width="350"/>
