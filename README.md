# EDA1-ASSIGNMENT
Codes for EDA1 
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt 
import seaborn as sns
data=pd.read_csv(r"C:\Users\haree\OneDrive\Desktop\Cardiotocographic.csv")
data
data.info()
data.dtypes
data.isnull()
plt.hist(data)
plt.show()
plt.boxplot(data)
plt.show()
data.describe()
correlation=data.corr(numeric_only=True)
correlation
sns.heatmap(correlation,annot=True)
import seaborn as sns
sns.pairplot(data)
import seaborn as sns
import matplotlib.pyplot as plt
cols = data.columns
colours = ['blue', 'yellow'] # specify the colours - yellow is missing. blue is not missing.
sns.heatmap(data[cols].isnull(),cmap=sns.color_palette(colours))
