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




