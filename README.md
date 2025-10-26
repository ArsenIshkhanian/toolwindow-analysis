# 🧠 Tool Window Usage Analysis

### 📊 Data Science & Statistical Analysis Project

This project analyzes **tool window usage patterns** in an IDE to explore **how long users keep tool windows open** depending on whether they were opened **manually** or **automatically**.  
The analysis reconstructs **open–close sessions**, calculates **durations**, and compares statistics between the two open types.

---

## 📂 Dataset Description

Each record in the dataset contains:

| Column       | Description                                         |
|-------------|-----------------------------------------------------|
| `user_id`    | Unique anonymized user ID                            |
| `timestamp`  | Event time (epoch milliseconds)                     |
| `event`      | `"open"` or `"close"`                               |
| `open_type`  | `"manual"`, `"auto"`, or `NULL` (for close events) |

---

## 🎯 Objectives

✅ Match **open/close pairs** to form complete sessions  
✅ Compute **duration** of each session  
✅ Compare **manual vs automatic** session lengths  
✅ Handle **orphaned events** and **missing closes**  

---

## ⚙️ Setup Instructions

### 1️⃣ Create Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

## 🧮 Analysis Summary

The notebook includes the following steps:

- 🧹 **Data Loading & Cleaning**  
  Handling missing values, orphaned events, and messy data to ensure accurate analysis.

- 🔗 **Matching Open/Close Events**  
  Pairing each open event with its corresponding close event to reconstruct full sessions.

- ⏱️ **Session Duration Calculations**  
  Computing how long each tool window stayed open for both manual and automatic opens.

- 📊 **Descriptive Statistics**  
  Summary metrics including **count**, **mean**, **median**, **standard deviation**, **min**, and **max** for session durations.

- 🖼️ **Visualizations**  
  Boxplots and histograms to compare manual vs auto open durations and visualize patterns.
