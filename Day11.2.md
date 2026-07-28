# Data Cleaning in Excel

## What is Data Cleaning?

**Data Cleaning** (also called **Data Cleansing**) is the process of identifying, correcting, and removing inaccurate, incomplete, duplicate, or inconsistent data from a dataset. Clean data improves the accuracy of analysis and helps in making better decisions.

---

# Steps for Data Cleaning in Excel

## 1. Remove Duplicate Records

Duplicate records can affect analysis and produce incorrect results.

### Steps:
1. Select the entire dataset.
2. Go to **Data** → **Remove Duplicates**.
3. Select the columns to check for duplicates.
4. Click **OK**.

**Purpose:** Ensures each record appears only once.

---

## 2. Handle Missing Values

Missing values can lead to inaccurate calculations.

### Steps:
- Use **Filter** to find blank cells.
- Fill missing values manually or with suitable values.
- Delete rows if the missing information is unnecessary.

**Purpose:** Completes the dataset and improves accuracy.

---

## 3. Correct Data Entry Errors

Typing mistakes create inconsistent data.

### Steps:
- Press **Ctrl + H** to open **Find and Replace**.
- Replace incorrect values with the correct ones.
- Review spelling mistakes manually if necessary.

**Purpose:** Maintains consistency in the dataset.

---

## 4. Remove Extra Spaces

Extra spaces can prevent proper matching and sorting.

### Formula:
```excel
=TRIM(A2)
```

**Purpose:** Removes unnecessary spaces before, after, and between words.

---

## 5. Standardize Text Format

Ensure all text follows the same format.

### Common Functions

Convert to Uppercase:

```excel
=UPPER(A2)
```

Convert to Lowercase:

```excel
=LOWER(A2)
```

Capitalize First Letter:

```excel
=PROPER(A2)
```

**Purpose:** Makes text data consistent.

---

## 6. Standardize Date and Number Formats

Use a consistent format for:
- Dates
- Currency
- Percentages
- Numbers

### Steps:
1. Select the cells.
2. Press **Ctrl + 1**.
3. Choose the desired format.

**Purpose:** Ensures uniform presentation of data.

---

## 7. Remove Unwanted Characters

Some imported data contains hidden or non-printable characters.

### Formula:

```excel
=CLEAN(A2)
```

You can combine it with:

```excel
=TRIM(CLEAN(A2))
```

**Purpose:** Removes unwanted hidden characters.

---

## 8. Validate Data

Restrict users from entering invalid data.

### Steps:
1. Select the cells.
2. Go to **Data** → **Data Validation**.
3. Set validation rules (number, date, list, etc.).

**Purpose:** Prevents incorrect data entry.

---

## 9. Check for Inconsistencies

Look for inconsistent values such as:

| Incorrect | Correct |
|-----------|---------|
| M | Male |
| F | Female |
| USA | United States |
| MH | Maharashtra |

### Methods:
- Sort data
- Apply filters
- Use Conditional Formatting

**Purpose:** Makes categories consistent.

---

## 10. Identify Outliers

Outliers are unusually high or low values.

### Methods:
- Sort data
- Use Conditional Formatting
- Create charts
- Compare with expected range

**Purpose:** Detects abnormal values that may affect analysis.

---

## 11. Verify Data Accuracy

Perform a final review after cleaning.

### Checklist
- No duplicate records
- No missing values
- Correct spelling
- Consistent formatting
- Valid data entries
- Proper calculations

**Purpose:** Ensures the dataset is accurate and reliable.

---

# Excel Tools Used for Data Cleaning

| Tool | Purpose |
|------|---------|
| Remove Duplicates | Deletes duplicate records |
| Sort | Organizes data |
| Filter | Displays specific records |
| Find & Replace | Corrects repeated errors |
| Text to Columns | Splits text into multiple columns |
| Flash Fill | Automatically fills patterns |
| TRIM() | Removes extra spaces |
| CLEAN() | Removes hidden characters |
| UPPER(), LOWER(), PROPER() | Standardizes text |
| Data Validation | Restricts invalid entries |
| Conditional Formatting | Highlights duplicates, blanks, and errors |

---

# Data Cleaning Workflow

```text
Raw Data
    │
    ▼
Remove Duplicates
    │
    ▼
Handle Missing Values
    │
    ▼
Correct Data Entry Errors
    │
    ▼
Trim Extra Spaces
    │
    ▼
Standardize Text
    │
    ▼
Standardize Dates & Numbers
    │
    ▼
Remove Hidden Characters
    │
    ▼
Validate Data
    │
    ▼
Check Inconsistencies
    │
    ▼
Identify Outliers
    │
    ▼
Verify Accuracy
    │
    ▼
Clean Data Ready for Analysis
```

---

# Summary

Data cleaning is an essential step before analyzing any dataset. It improves data quality by removing duplicates, correcting errors, handling missing values, standardizing formats, and validating entries. Clean data leads to more accurate reports, better visualizations, and reliable decision-making.

---