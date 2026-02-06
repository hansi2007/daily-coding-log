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
