# EXNO:2 ANALYSIS USING PYTHON
# REGISTRATION NO: 212224040052
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

# CODING AND OUTPUT:
```
    <<INCLUDE YOUR CODING AND OUTPUT SCREENSHOTS>>
```
```
import pandas as pd
df=pd.read_csv("C:\\Users\\admin\\Downloads\\titanic_dataset.csv")
df
```
<img width="1430" height="623" alt="484407426-06444c09-796e-4ec5-b92b-9c73afee9213" src="https://github.com/user-attachments/assets/dc68e97a-5cec-4fe9-a5d0-83bf64630242" />

```
df.shape

```
<img width="1327" height="84" alt="484408294-0e871600-8d45-4e61-9985-a6e843ab1614" src="https://github.com/user-attachments/assets/b6bd1146-c33a-401e-be66-7389dc344d50" />

```
df.set_index("PassengerId",inplace=True)
df
```

<img width="1323" height="587" alt="484408383-c19a2eeb-aa3e-4299-bf02-3e0735b0fc9e" src="https://github.com/user-attachments/assets/2271e08d-cac4-4c41-9512-108f2d1089e7" />

```
df.unique()
```
<img width="1147" height="314" alt="484408679-445a6e49-6bc7-4cd4-9976-713c42de4a0c" src="https://github.com/user-attachments/assets/d0345889-bc91-4861-812e-b9c8f2006d86" />

```
df['Survived'].value_counts()
```
<img width="1191" height="134" alt="484408954-bd2f722a-a0aa-4b7c-b6bc-16d92b1203b0" src="https://github.com/user-attachments/assets/5a34b759-d11d-4e2f-8945-00775b891e1e" />

```
df.Pclass.unique()
```

<img width="1216" height="81" alt="484409228-8190e488-5948-43a8-9fba-3b8f61472551" src="https://github.com/user-attachments/assets/e66166ad-2387-4326-b4fb-5b153fbb556b" />

```
df.rename(columns={"Sex":"Gender"},inplace=True)
df
```
<img width="1333" height="587" alt="484409440-dbbb406f-9014-4e94-a306-71ffb74002b9" src="https://github.com/user-attachments/assets/494f144c-b8e6-439d-bcba-b21b1e87b5b8" />

```
import seaborn as sns
sns.countplot(data=df)
```
<img width="1376" height="674" alt="484410239-2a3112c5-b324-42db-a190-22dbafeaa89f" src="https://github.com/user-attachments/assets/66e61f22-30e8-4205-885e-a4ec38031fda" />

```
sns.countplot(x="Survived",hue="Gender",data=df)
```

<img width="1167" height="637" alt="484410821-3a8c0849-4f4f-49ff-bd5a-40232f61d324" src="https://github.com/user-attachments/assets/fa069c25-0853-447b-84f8-403f8aef95ff" />

```
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
```

<img width="1290" height="704" alt="484411466-db37945c-9e88-42c9-ac6f-5968b1cf248f" src="https://github.com/user-attachments/assets/a0a4051d-49b1-4e8c-ae68-dcd2b656f11f" />

```
sns.boxplot(data=df)
```

<img width="1045" height="621" alt="484411820-19fdcdd8-b61b-47da-bb10-a365af595b3f" src="https://github.com/user-attachments/assets/4f1e8c5d-c5b7-4079-be84-d9b351ef1075" />

```
df.boxplot(column="Survived",by="Gender")
```

<img width="1148" height="658" alt="484413224-c4cf9a1a-0bd4-4f8c-9034-f8cc4c2ff617" src="https://github.com/user-attachments/assets/f5a15efe-84ea-4568-86e9-d5ef2ae65bba" />

```
sns.scatterplot(data=df)
```

<img width="1393" height="646" alt="484413393-de0b9e6c-654e-402f-9c4a-082d0d33cded" src="https://github.com/user-attachments/assets/13d155f1-fbe6-4d1b-9264-78b4e8c0a050" />

```
sns.scatterplot(x=df['Age'],y=df['Fare'])
```

<img width="1389" height="645" alt="484413501-4be635da-cc2d-468d-9cbf-b935206a5054" src="https://github.com/user-attachments/assets/a0035952-8ca4-41fa-b06c-dbde42eafe21" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
```

<img width="1315" height="822" alt="484413731-36fd07b8-a701-453e-b0e3-0c426e0f69c8" src="https://github.com/user-attachments/assets/65821b24-e0aa-4bce-8057-910f4f16439f" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
```

<img width="1387" height="839" alt="484413876-541f46c2-15e6-4924-8f95-179109cf7eaf" src="https://github.com/user-attachments/assets/0f4232f2-a4b5-4896-8552-f2fba2da9582" />
```

# RESULT:
        <<INCLUDE YOUR RESULT HERE>>







