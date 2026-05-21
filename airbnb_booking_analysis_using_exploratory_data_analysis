# Step 1: Importing Necessary Libraries and Loading the AirBnB Dataset
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset:
file_path = "/content/Airbnb_Open_Data.csv"
df = pd.read_csv(file_path)
print(df.head())

# Step 2: Check the Column Names in the Dataset
df.columns

# Step 4: Handle Missing Values
# Convert 'last review' to datetime and handle errors:
df['last review'] = pd.to_datetime(df['last review'], errors='coerce')
# Fill missing values:
df.fillna({'reviews per month': 0, 'last review': df['last review'].min()}, inplace=True)
# Drop records with missing 'name' or 'host name':
df.dropna(subset=['NAME', 'host name'], inplace=True)

# Step 5: Correct Data Types
# Remove $ and convert to float:
df['price'] = df['price'].replace('[\$,]', '', regex=True).astype(float)
df['service fee'] = df['service fee'].replace('[\$,]', '', regex=True).astype(float)

# Step 6: Remove Duplicates
# Step 7: Confirm Data Cleaning
df.drop_duplicates(inplace=True)
print(df.info())

# Step 8: Descriptive Statistics
print(df.describe())

# Step 9: Visualization
# Distribution of Prices
plt.figure(figsize=(10, 6))
sns.histplot(df['price'], bins=50, kde=True)
plt.title('Distribution of Listing Prices')
plt.xlabel('Price ($)')
plt.ylabel('Frequency')
plt.show()

# Room Type Analysis
plt.figure(figsize=(8, 5))
sns.countplot(x='room type', data=df, color='hotpink')
plt.title('Room Type Distribution')
plt.xlabel('Room Type')
plt.ylabel('Count')
plt.show()

# Neighborhood Analysis
plt.figure(figsize=(12, 8))
sns.countplot(y='neighbourhood group', data=df, color="lightgreen", order=df['neighbourhood group'].value_counts().index)
plt.title('Number of Listings by Neighborhood Group')
plt.xlabel('Count')
plt.ylabel('Neighborhood Group')
plt.show()

# Price vs. Room Type
plt.figure(figsize=(10, 6))
sns.boxplot(x='room type', y='price', hue='room type', data=df, palette='Set2')
plt.title('Price vs. Room Type')
plt.xlabel('Room Type')
plt.ylabel('Price ($)')
plt.legend(title='Room Type')
plt.show()

# Reviews Over Time
df['last review'] = pd.to_datetime(df['last review'])
reviews_over_time = df.groupby(df['last review'].dt.to_period('M')).size()

plt.figure(figsize=(12, 6))
reviews_over_time.plot(kind='line', color='red')
plt.title('Number of Reviews Over Time')
plt.xlabel('Date')
plt.ylabel('Number of Reviews')
plt.show()