# daily-coding-log
class Solution {
    public boolean isPalindrome(int x) {
        if(x<0){
            return false;
        }
        int rev=0;
        int num=x;

        while(num!=0){
            rev=rev*10 + num%10;
            num=num/10;
        }

        return (rev==x);
        
    }
}


class Solution {
    public void reverseString(char[] s) {
        int l=0;
        int r=s.length-1;
        while(l<r){
            char temp=s[l];
            s[l]=s[r];
            s[r]=temp;

            l++;
            r--;
        }
        
    }
}



print('hello world')


int a
if (a%2==0):
print('even')
else: 
print ('false')

a = 5
b = 3
sum = a + b
print("Sum:", sum)


arithmetic operator in python hacker rank :-
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    
    print(a+b)
    print(a-b)
    print(a*b)


print ("hello world")
print ("hello world")


a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("1.Add 2.Subtract 3.Multiply 4.Divide")
choice = int(input("Enter choice: "))

if choice == 1:
    print("Result:", a + b)
elif choice == 2:
    print("Result:", a - b)
elif choice == 3:
    print("Result:", a * b)
elif choice == 4:
    print("Result:", a / b)
else:
    print("Invalid choice")



import pandas as pd

employees=pd.DataFrame({
    'employees_id':[501,502,503,504],
    'name':['A','B','C','D'],
    'department_id':[1,2,3,4]
    })

employees.to_excel('employees.xlsx', index=False)




salaries=pd.DataFrame({
    'employees_id':[501,502,503,504],
    'salaries':[5000,6000,7000,8000]
})

salaries.to_csv('salaries.csv',index=False)



employees.shape

employees.columns

employees.isnull().sum()

salaries.columns

employees.tail()

employees.info()

salaries.describe()

import pandas as pd
import json

departments = [
    {"department_id": 1, "department_name": "HR"},
    {"department_id": 2, "department_name": "Finance"},
    {"department_id": 3, "department_name": "IT"}
]

with open('departments.json', 'w') as f:
    json.dump(departments, f)

print("department.json created successfully.")


dept_df=pd.read_json('departments.json')

print(dept_df)

print(set(employees['employees_id']).intersection(set(salaries['employees_id'])))
print("common employe ID's  bw employees & salaries")

merged_df=pd.merge(employees,salaries,on='employees_id', how='inner')
print("after  merging employees & salaries")
print(merged_df)

final_df=pd.merge(merged_df,dept_df,on='department_id',how='inner')

print('final merged dataframe')
print(final_df)

final_df.to_csv('final_df.csv',index=False)

print('final_df.csv created successfully')


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris

#need to load datasets

iris = load_iris()
df= pd.DataFrame(iris.data, columns=iris.feature_names)

df.shape

df['species']=iris.target

Index(['sepal length (cm)', 'sepal width (cm)', 'petal length (cm)',
       'petal width (cm)', 'species'],
      dtype='object')


# descriptive statistics we r going to do here

print("mean :",df.mean(numeric_only=True))



print("median :" , df.median(numeric_only=True))

print("dt_deviation :", df.std(numeric_only=True))

print("kurtosis :" , df.kurtosis(numeric_only=True))

print("skewness :", df.skew(numeric_only=True))

# boxplot :

plt.figure(figsize=(8,5))
df.drop('species', axis =1).boxplot()
plt.title("boxplot of iris features")
plt.show()

#histogram for saple length

plt.figure(figsize=(6,4))
plt.hist(df['sepal length (cm)'], bins=10)
plt.title("histogram of sepal length")
plt.xlabel("sepal length")
plt.ylabel("frequency")
plt.show()

plt.figure(figsize=(6,4))
plt.hist(df['petal width (cm)'], bins=10)
plt.title("histogram of petal width")
plt.xlabel("petal width")
plt.ylabel("frequency")
plt.show()



#Import required libraries
#SEMMA - Sample/Access, Explore, Modify, Model, Assessment
#Data management libraries (Sample, Modify)
import pandas as pd
import numpy as np
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.model_selection import train_test_split



#Visualization
import seaborn as sns
import matplotlib.pyplot as plt

#Modeling
from sklearn.naive_bayes import MultinomialNB
from sklearn.svm import LinearSVC

#Assessment/Evaluation
from sklearn.metrics import classification_report, confusion_matrix

#Accessing/sampling the data
# Replace 'spam_dataset.csv' with the path to your actual file
file_path = 'C:/Users/hansi/Downloads/4th sem minor project/spam.csv'

# Read the CSV file
df = pd.read_csv(file_path, encoding='latin-1')


#Explore
df.sample(10)

#Modify the data
df.columns

df = df[['Label', 'tmessage']]


df1.sample()

# Tokenize using lambda function (splitting by whitespace)
df['Tokens'] = df['Message'].apply(lambda x: x.split())

# Target variable
y = df['Label']

# Initialize CountVectorizer
vectorizer = CountVectorizer()

# Feature matrix from 'Message' column
X = vectorizer.fit_transform(df['Message'])

# Show shape of feature matrix
print(f"Feature matrix shape: {X.shape}")
print(f"Target variable shape: {y.shape}")


print("hello world")

print ("hello world")

import seaborn as sns
import matplotlib.pyplot as plt

# scatter plot
plt.figure(figsize=(6,4))
plt.scatter(df['sepal width (cm)'], df['petal width (cm)'])
plt.xlabel("sepal width (cm)")
plt.ylabel('petal width (cm)')
plt.title('scatter plot : sepal width vs petal width')
plt.show()


#heatmap for correlation : it means correlation of feature
plt.figure(figsize=(7,5))
correlation = df.drop('species', axis =1).corr()
sns.heatmap(correlation, annot=True, cmap='coolwarm')
plt.title('heatmap of feature correlation')
plt.show()
