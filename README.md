# 🧹 Medical Appointments Data Cleaning Script

This repository contains a Python script to clean and preprocess the **"Medical Appointment No Shows"** dataset from Kaggle. The dataset includes information about patients and whether they showed up for their scheduled medical appointments.

---

## 📊 Dataset Source

- 📁 Original File: `KaggleV2-May-2016.csv`  
- 🔗 Source: [Kaggle - No Show Appointments](https://www.kaggle.com/datasets/joniarroba/noshowappointments)

---

## ✨ Features

### 1. Loading the Dataset
- Uses `pandas` to read the CSV file.
- Displays the initial shape and preview of the dataset.

### 2. Missing Values
- Checks for and reports any missing values.

### 3. Duplicate Handling
- Detects and removes duplicate rows.

### 4. Column Name Standardization
- Converts all column names to lowercase.
- Replaces spaces with underscores.
- Strips leading/trailing spaces.

### 5. Datetime Conversion
- Converts `ScheduledDay` and `AppointmentDay` columns to datetime format.

### 6. Age Filtering
- Filters out records with age < 0 or age > 120.

### 7. Gender Cleanup
- Standardizes values in the `Gender` column (uppercase and trimmed).

### 8. Target Column Cleaning
- Renames `No-show` to `no_show`.
- Maps:
  - `"No"` → `0` (Patient showed up)
  - `"Yes"` → `1` (Patient did not show up)

### 9. Export Cleaned Data
- Saves the cleaned dataset to `Cleaned_medical_appointments.csv`.

---

## 📁 Input & Output

| File Name                          | Description                                |
|-----------------------------------|--------------------------------------------|
| `KaggleV2-May-2016.csv`           | Raw dataset from Kaggle                    |
| `Cleaned_medical_appointments.csv`| Cleaned and preprocessed dataset           |

---

## 🛠️ Requirements, How to Run, and Output Screenshots

Make sure Python 3 and the required library are installed:

```bash
pip install pandas
```

To run the script:
python medical_cleaning.py
