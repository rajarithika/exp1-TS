## LAB EXPERIMENT 1: PLOT A TIME SERIES DATA

**Name:** RAJA RITHIKA M

**Reg.no:** 2305001029

## Aim

To develop a Python program to plot and visualize time series data such as population, commodity market price, or temperature.

## Objective

Students will learn to:

1. Create time-series data.
2. Store data using Pandas.
3. Plot the data using Matplotlib.
4. Identify the trend in a time series.

## Step 1: Install Required Libraries

If using Google Colab, libraries are usually already available.

```python
!pip install pandas matplotlib
```

## Step 2: Import Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
```

### Why?

- `pandas` → stores and handles data.
- `matplotlib` → creates graphs.

## Step 3: Create Sample Population Data

We will use Year and Population.

```python
year = [2019, 2020, 2021, 2022, 2023, 2024, 2025]

population = [100, 103, 106, 110, 114, 118, 123]
```

Here, population is assumed to be in millions.

## Step 4: Create a DataFrame

```python
data = pd.DataFrame({
    "Year": year,
    "Population": population
})

print(data)
```

**Output:**

```text
   Year  Population
0  2019         100
1  2020         103
2  2021         106
3  2022         110
4  2023         114
5  2024         118
6  2025         123
```

## Step 5: Plot the Time Series

```python
plt.plot(data["Year"], data["Population"])
```

## Step 6: Add Title and Labels

```python
plt.title("Population Time Series")
plt.xlabel("Year")
plt.ylabel("Population (Millions)")
```

## Step 7: Display the Graph

```python
plt.show()
```

---

## Example 1: Annual Population (2015–2025)

```python
import pandas as pd
import matplotlib.pyplot as plt

year = [2015, 2016, 2017, 2018, 2019, 2020,
        2021, 2022, 2023, 2024, 2025]

population = [85, 88, 91, 95, 100, 103,
              106, 110, 114, 118, 123]

data = pd.DataFrame({"Year": year, "Population": population})

print(data)

plt.plot(data["Year"], data["Population"], color="red")

plt.title("Annual Population 2015-2025")
plt.xlabel("Year")
plt.ylabel("Population")
plt.grid()

plt.show()
```
## Output
**Observation:** The population shows an increasing trend from 2015 to 2025.
<img width="712" height="567" alt="image" src="https://github.com/user-attachments/assets/99608569-eb49-4384-a8c7-44972b3e2b08" />


---

## Example 2: Monthly Temperature for 12 Months

```python
import pandas as pd
import matplotlib.pyplot as plt

month = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
         "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]

temperature = [25, 27, 30, 33, 35, 34,
               32, 31, 30, 29, 27, 25]

data = pd.DataFrame({"Month": month, "Temperature": temperature})

print(data)

plt.plot(data["Month"], data["Temperature"], color="red")

plt.title("Monthly Temperature")
plt.xlabel("Month")
plt.ylabel("Temperature (°C)")
plt.grid()

plt.show()
```
## Output
**Observation:** Temperature increases until May and then decreases towards December, showing a seasonal pattern.
<img width="696" height="563" alt="image" src="https://github.com/user-attachments/assets/df6e5a0d-d1bc-4a08-8837-82ca75b873a6" />

---

## Example 3: Monthly Commodity Price for 12 Months

```python
import pandas as pd
import matplotlib.pyplot as plt

month = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
         "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]

price = [4200, 4350, 4280, 4500, 4650, 4800,
         4700, 4900, 5100, 5000, 5300, 5500]

data = pd.DataFrame({"Month": month, "Price": price})

print(data)

plt.plot(data["Month"], data["Price"], color="red")

plt.title("Monthly Commodity Price")
plt.xlabel("Month")
plt.ylabel("Price")
plt.grid()

plt.show()
```
## Output
**Observation:** The commodity price shows an overall increasing trend, with small decreases in some months.
<img width="722" height="567" alt="image" src="https://github.com/user-attachments/assets/99e2b66b-2afa-41b3-bfcd-1be63d9dbef4" />

---

## Result

Thus, a Python program to plot and visualize time series data such as annual population, monthly temperature, and monthly commodity price was implemented and executed successfully.
