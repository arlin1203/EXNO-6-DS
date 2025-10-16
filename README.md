# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
# EXNO-6-DS : Data Visualization using Seaborn Library

# Step 1: Import necessary libraries
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

# Step 2: Create sample dataset
data = {
    'Student': ['John', 'Alice', 'Bob', 'Diana', 'Eva', 'Tom', 'Lisa', 'Nick'],
    'Gender': ['Male', 'Female', 'Male', 'Female', 'Female', 'Male', 'Female', 'Male'],
    'Maths': [88, 92, 79, 93, 85, 76, 89, 90],
    'Science': [90, 85, 76, 89, 95, 80, 83, 91],
    'English': [78, 82, 74, 88, 90, 72, 85, 87]
}

# Step 3: Convert dictionary to DataFrame
df = pd.DataFrame(data)
print("Input Data:\n")
print(df)

# Step 4: Set Seaborn theme
sns.set(style="whitegrid")

# Step 5: Data Visualization using Seaborn

# 1. BAR PLOT – Compare average Maths marks by Gender
plt.figure(figsize=(7,5))
sns.barplot(x='Gender', y='Maths', data=df, palette='pastel', ci=None)
plt.title("Average Maths Marks by Gender")
plt.show()

# 2. SCATTER PLOT – Relationship between Maths and Science
plt.figure(figsize=(7,5))
sns.scatterplot(x='Maths', y='Science', hue='Gender', style='Gender', s=100, data=df, palette='husl')
plt.title("Maths vs Science Marks by Gender")
plt.show()

# 3. BOX PLOT – Distribution of English Marks by Gender
plt.figure(figsize=(7,5))
sns.boxplot(x='Gender', y='English', data=df, palette='cool')
plt.title("Distribution of English Marks by Gender")
plt.show()

# 4. HISTOGRAM – Distribution of Maths Marks
plt.figure(figsize=(7,5))
sns.histplot(df['Maths'], bins=6, kde=True, color='coral')
plt.title("Distribution of Maths Marks")
plt.xlabel("Maths Marks")
plt.ylabel("Count")
plt.show()

# 5. HEATMAP – Correlation between subjects
plt.figure(figsize=(6,5))
corr = df[['Maths', 'Science', 'English']].corr()
sns.heatmap(corr, annot=True, cmap='Blues', linewidths=0.5)
plt.title("Correlation Heatmap of Subjects")
plt.show()

# 6. PAIRPLOT – Pairwise relationships between all subjects
sns.pairplot(df[['Maths', 'Science', 'English']], kind='scatter')
plt.suptitle("Pairplot of Subject Marks", y=1.02)
plt.show()



<img width="567" height="381" alt="Screenshot 2025-10-16 110225" src="https://github.com/user-attachments/assets/e2f78b60-2a36-42a1-8f58-70dfda29084e" />

# Result:
The above code executed sucessfully
