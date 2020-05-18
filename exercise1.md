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

However, there is a funtion in Python that also do this:

```Python
    import pandas as pd
    tabla_df = pd.read_csv('jasp_practice_1.csv', index_col=0) # use the path of your file
    df_transposed = tabla_df.transpose()
    df_transposed
    # if you want to write the new file use: df_transposed.to_csv('jasp_practice_2.csv')
```

---

|     Athlete:     |    A   |    B   |    C   |    D   |    E   |    F   |    G   |
|:----------------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| Bench press (kg) | 127.52 | 169.62 | 226.20 | 143.91 | 169.73 | 177.36 | 183.51 |
|    Weight (kg)   |  64.36 |  69.58 |  70.10 |  71.48 |  76.53 |  70.98 |  72.47 |

---

Now we read the file from the csv file.

```Python
    import pandas as pd
    tabla_df = pd.read_csv('jasp_practice_1.csv', index_col=0) # use the path of your file
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


---


##### Once we upload the file in JASP, we select the 'Descriptives' option and then Descriptive Statistics 


---

![image](/images/Jaspdescriptive1.png)

---

***From Pandas module we use the fucntion describe():***
- describe() Function gives the mean, std and IQR values. 
It excludes character column and calculate summary statistics only for numeric columns. 

---

```Python
    import pandas as pd
    tabla_df = pd.read_csv('jasp_practice_1.csv', index_col=0) # use the path of your file
    tabla_df.describe()
```

---

| Bench press (kg) | Weight (kg) | Weight (kg) |
|------------------|-------------|:-----------:|
| count            | 7.000000    | 7.000000    |
| mean             | 171.121429  | 70.785714   |
| std              | 31.283069   | 3.641592    |
| min              | 127.520000  | 64.360000   |
| 25%              | 156.765000  | 69.840000   |
| 50%              | 169.730000  | 70.980000   |
| 75%              | 180.435000  | 71.975000   |
| max              | 226.200000  | 76.530000   |

---
