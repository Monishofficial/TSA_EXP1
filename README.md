# Ex.No: 01 A PLOT A TIME SERIES DATA
###  Date: 26-08-2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

### NAME: MONISH N
### REG NO: 212223240097
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt


df = pd.read_csv('BMW_Car_Sales_Classification.csv')
sns.set(style="whitegrid")
plt.rcParams["figure.figsize"] = (10, 6)
target = 'Sales_Classification'

plt.figure()
sns.countplot(x=target, data=df, palette='pastel')
plt.title('Target Class Distribution')
plt.xlabel(target)
plt.ylabel('Count')
plt.show()

num_cols = df.select_dtypes(include=['int64', 'float64']).columns
for col in num_cols:
    plt.figure()
    sns.histplot(df[col].dropna(), kde=True, bins=30, color='skyblue')
    plt.title(f'Distribution of {col}')
    plt.xlabel(col)
    plt.ylabel('Frequency')
    plt.show()

cat_cols = df.select_dtypes(include='object').columns.drop(target, errors='ignore')
```
# OUTPUT:
<img width="921" height="522" alt="image" src="https://github.com/user-attachments/assets/a1314bf5-5137-4ac7-aeff-e6329569ae9a" />
<img width="795" height="525" alt="image" src="https://github.com/user-attachments/assets/2ca35e6d-1516-492f-96ff-83f54c8b1ec3" />
<img width="873" height="519" alt="image" src="https://github.com/user-attachments/assets/bc8bcd30-2f4e-41a5-b671-ec6fe6cf2595" />
<img width="848" height="538" alt="image" src="https://github.com/user-attachments/assets/e9d5c776-2b18-4e3d-82b1-d20029b64686" />
<img width="887" height="526" alt="image" src="https://github.com/user-attachments/assets/357874c7-7b42-424b-9def-bf148dac2b0c" />












# RESULT:
Thus we have created the python code for plotting the time series of given data.
