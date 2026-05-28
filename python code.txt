import pandas as pd


data = {
    "Name": ["Ravi", "Ravi", "Kumar", "Priya"],
    "Marks": [85, 85, None, 90]
}

df = pd.DataFrame(data)


df = df.drop_duplicates()


df["Marks"] = df["Marks"].fillna(0)


df.to_csv("cleaned_data.csv", index=False)

print("Data cleaned successfully!")
print(df)
