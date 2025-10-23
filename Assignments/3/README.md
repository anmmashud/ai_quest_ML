
## 🧩 Step 1 — Load Dataset

Before analysis, we start by importing the dataset into a **Pandas DataFrame**.

```python
import pandas as pd

# Load dataset
df = pd.read_csv("Dhaka_Rent.csv", header=0, sep=";")

# Display first few rows
df.head()
```

---

### ⚙️ Function: `pd.read_csv()`

> The `read_csv()` function reads data from a CSV (Comma-Separated Values) file and converts it into a Pandas DataFrame for further analysis and manipulation.

---

### 🧠 Parameters Overview

| 🏷️ **Parameter**    | 💬 **Explanation**                          | 🧮 **Example**                | 🖥️ **Output (Description)**            |
| -------------------- | ------------------------------------------- | ----------------------------- | --------------------------------------- |
| `filepath_or_buffer` | Path or URL of the CSV file to load         | `"Dhaka_Rent.csv"`            | Loads data from the file into memory    |
| `sep`                | Defines column separator character          | `sep=";"`                     | Columns are split by `;` instead of `,` |
| `header`             | Row number containing column names          | `header=0`                    | First row treated as column names       |
| `index_col`          | Set a specific column as DataFrame index    | `index_col=0`                 | The first column becomes index          |
| `usecols`            | Read only selected columns                  | `usecols=['Rent', 'Area']`    | Loads only specified columns            |
| `na_values`          | Specify additional missing value indicators | `na_values=['?', 'NA', '--']` | Marks these as `NaN`                    |
| `dtype`              | Define data type for columns                | `dtype={'Rent': float}`       | Ensures consistent types                |
| `encoding`           | Handle different file encodings             | `encoding='utf-8'`            | Prevents UnicodeDecodeError             |
| `parse_dates`        | Convert date columns to datetime            | `parse_dates=['Date']`        | Enables time-based operations           |
| `nrows`              | Read limited rows from file                 | `nrows=100`                   | Loads only first 100 rows               |

> 💡 **Tip:** You can combine multiple parameters to customize how data is read.
> Example:
>
> ```python
> df = pd.read_csv(
>     "Dhaka_Rent.csv",
>     sep=";",
>     na_values=['?'],
>     dtype={'Rent': float},
>     encoding='utf-8'
> )
> ```

---

### ✅ Expected Output

After executing the above code, you’ll see the first few rows of your dataset:

```plaintext
     Area   Rent   Location
0   Gulshan  55000  Dhaka
1   Banani   48000  Dhaka
2   Dhanmondi  42000  Dhaka
...
```

---

### 🗒️ Notes

* Always verify that the **separator** (`sep`) matches your file’s format.
* If your dataset contains missing values or incorrect encodings, set `na_values` and `encoding` properly.
* Using parameters like `dtype` and `parse_dates` early ensures cleaner data for EDA and model training.

---

### 📘 References

* [Pandas `read_csv()` Documentation](https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html)
* [Data Cleaning with Pandas Guide](https://pandas.pydata.org/docs/user_guide/io.html)

---

```

---

Would you like me to add **collapsible sections** (expandable tables using `<details>` tags) so that your README looks more interactive and compact on GitHub?
```























