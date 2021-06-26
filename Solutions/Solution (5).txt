#include <iostream>

using namespace std;
int greatestCommonDivisor(int num1, int num2);

void main()
{
    cout<<"<===========Welcome to Beginner's Examples============>\n";
    cout<<"1.Number's Triangle.\n";
    cout<<"2.Greatest of 3 numbers.\n";
    cout<<"3.Given Number is Palindrome or not.\n";
    cout<<"4.GCD of 2 numbers.\n";
    cout<<"Please provide input to see illustration\n";
    
    int inputNumber;
    cin>>inputNumber;
    switch (inputNumber)
    {
        case 1:
            drawTriangle();
            break;
        case 2:
            displayMaxNumber();
            break;
        case 3:
            checkForPalindrome();
            break;
        case 4:
            calculateGreatestCommonDivisor();
            break;
        default:
            cout<<"Please provide valid Input"<<endl;
    }
}

void drawTriangle()
{
    cout<<"Enter height for triangle ";
    int height;
    cin>>height;
    for(int i=0; i<height; i++)
    {
        for(int j=0; j<=i; j++)
        {
            cout<<j;
        }
        cout<<"\n";
    }
}

void displayMaxNumber()
{
    cout<<"Enter any 3 numbers ";
    int num1,num2,num3,max;
    cin>>num1;
    cin>>num2;
    cin>>num3;
    max = num1>num2?num1>num3?num1:num3:num2>num3?num2:num3;
    cout<<"Maximum of 3 numbers is "<<max<<endl;
}

void checkForPalindrome()
{
    cout<<"Enter any number ";
    int num1,num2=0,temp;
    cin>>num1;
    temp = num1;
    while(temp!=0)
    {
        num2 *= 10;
        num2 += temp%10;
        temp = temp/10;
    }
    if(num1==num2)
    {
        cout<<num1<<" is a palindrome"<<endl;
    }
}

void calculateGreatestCommonDivisor()
{
    cout<<"Enter any 2 numbers ";
    int num1,num2,gcd;
    cin>>num1;
    cin>>num2;
    gcd = greatestCommonDivisor(a,b);
    cout<<"GCD of "<<num1<<" and "<<num2<<" is "<<gcd<<endl;
}

int greatestCommonDivisor(int num1, int num2)
{
    if(num2!=0)
    {
        return greatestCommonDivisor(num2,num1%num2); //Recursion
    }
    else
    {
        return num1;
    }
}
