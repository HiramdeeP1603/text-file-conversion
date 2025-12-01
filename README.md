# 📊 Performance Comparison of Programming Languages Based on File Size

![Language](https://img.shields.io/badge/Language-Python-blue?style=for-the-badge&logo=python)
![Visualization](https://img.shields.io/badge/Data%20Visualization-Matplotlib-yellow?style=for-the-badge&logo=plotly)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen?style=for-the-badge)
[![LinkedIn](https://img.shields.io/badge/HiramDeep%20Kaur-LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/hiram-deep-227916337/)

---

## 📌 Project Overview

This project visualizes the performance of five popular programming languages—**C, C++, Java, R, and Python**—based on the **time taken to process files of increasing sizes**. Using **Pandas** for data handling and **Matplotlib** for graph plotting, we compare how each language performs as file sizes grow from **200MB to 1000MB**.

---

## 🧾 Data Used

The dataset represents the **time taken (in seconds)** by different programming languages to process files of various sizes.

| File Size | C  | C++ | Java | R  | Python |
|----------|----|-----|------|----|--------|
| 200MB    | 12 | 15  | 18   | 20 | 25     |
| 400MB    | 20 | 25  | 30   | 35 | 40     |
| 600MB    | 34 | 36  | 40   | 45 | 53     |
| 800MB    | 45 | 50  | 55   | 60 | 75     |
| 1000MB   | 55 | 60  | 70   | 80 | 100    |

---

## 🎯 What You Will Learn

✔ How to store performance data using **Pandas**  
✔ How to convert formatted size values (e.g., `"200MB"`) into integers  
✔ How to plot multi-line performance graphs using **Matplotlib**  
✔ Understanding how execution time scales across different languages  

---

## 📈 Output Graph

The line graph clearly illustrates:

📌 **C** is the fastest language for all file sizes  
📌 **Python** takes the most time as file size increases  
📌 Performance gap widens as file sizes grow, showcasing scalability differences  

---

## 🧠 Complete Python Code

```python
import pandas as pd
import matplotlib.pyplot as plt

# Define the data
data = {
    'File Size': ['200MB', '400MB', '600MB', '800MB', '1000MB'],
    'C': [12, 20, 34, 45, 55],
    'C++': [15, 25, 36, 50, 60],
    'Java': [18, 30, 40, 55, 70],
    'R': [20, 35, 45, 60, 80],
    'Python': [25, 40, 53, 75, 100]
}

# Convert the data to a DataFrame
df = pd.DataFrame(data)

# Convert 'File Size' to numerical values for plotting
df['File Size (MB)'] = df['File Size'].str.replace('MB', '').astype(int)

# Set the 'File Size (MB)' column as the index
df.set_index('File Size (MB)', inplace=True)

# Plot the data
plt.figure(figsize=(10, 6))
plt.plot(df.index, df['C'], label='C', marker='o')
plt.plot(df.index, df['C++'], label='C++', marker='o')
plt.plot(df.index, df['Java'], label='Java', marker='o')
plt.plot(df.index, df['R'], label='R', marker='o')
plt.plot(df.index, df['Python'], label='Python', marker='o')

# Add labels and title
plt.xlabel('File Size (MB)')
plt.ylabel('Time Taken (seconds)')
plt.title('Performance Comparison of Programming Languages')
plt.legend()
plt.grid(True)
plt.show()
```

---

## ▶️ How to Run

```bash
Open Visualization.ipynb in Google Colab
```

---

## 🚀 Key Takeaways

| Language | Performance Summary |
|---------|---------------------|
| C       | Fastest across all file sizes |
| C++     | Slightly slower than C |
| Java    | Moderate performance |
| R       | Slower, intended for statistical tasks |
| Python  | Easiest to use but slowest in execution |

---

## 👤 Author

**HiramDeep Kaur**  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/hiram-deep-227916337/)

---

⭐ If this helped you, **Star** the repository and share it with others!

