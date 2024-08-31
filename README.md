# Experiment-9
### AIM
To effectively use pointers in C++ for accessing array elements and finding the addresses of different data types, focus on mastering pointer operations.

### Software Used
VS code

### Problem Statement
1.) Write a c++ program to initialize pointers of different data types and print the required values.

2.) Write a c++ program to access elements of array using pointer.

3.) Write a c++ program to access elements of array without using pointer variable.

4.) Write a c++ program to swap the numbers using call by value.

5.) Write a c++ program to swap the numbers using call by reference.

# Theory
Pointers in C++ are used to work with addresses directly, allowing programs to handle memory more flexibly. They are crucial for tasks such as simulating call-by-reference and managing dynamic data structures. Here's a breakdown of key concepts:

Call by Value:- <br>
When a function is called using call-by-value, a copy of the function's arguments is made and stored in the stack memory. This means any changes to the parameters inside the function do not affect the original arguments outside the function. Each function gets its own separate copy of the data, which helps prevent unintended modifications.

Call by Reference:- <br>
Call-by-reference, on the other hand, involves passing the actual reference (or address) of the argument to the function. Instead of working with a copy of the argument, the function operates directly on the original data. This means that any changes made to the parameter within the function will affect the original argument outside the function. This method is efficient for modifying data and can be used to simulate pass-by-reference.

### Program Codes:- 
1)Pointer Array
~~~ javascript
 //Mohit Singh Rawat
 //23070123086
#include<iostream>
using namespace std;
int main()
{
    int *ptr;
    int a[5] = { 1,3,5,9,11};
    ptr = &a[0];
    int i;
    for(i=0 ; i<5 ; i++)
    {
        cout << "Element "<< i+1 <<" "<<"="<<" "<<*ptr << endl;
        ptr ++;

    }
}
~~~
2)Pointer Character
~~~ javascript
 //Mohit Singh Rawat
 //23070123086
#include<iostream>
using namespace std;
int main()
{
    char a = 'c'; 
    

    char *ptr;

    ptr = &a;

    cout<< "The value pointed by *ptr is"<<*ptr << endl;
    cout << "The value in b is" <<a << endl;
    cout << "The value in pointer variable ptr is"<<(void*)ptr << endl;

    cout << "the address of variable b is "<<&a << endl;
    ptr ++;
    cout<< "After increment the value in pointer variable ptr is: " << (void*)ptr << endl;

    
}
~~~
3)Pointer Float
~~~ javascript
 //Mohit Singh Rawat
 //23070123086
 #include <iostream>
using namespace std;
int main()
{
    float a = 'A';
    float *ptr;
    ptr=&a;
     cout<< "The value pointed by *ptr is: "<<*ptr << endl;
    cout << "The value in b is: " <<a << endl;
    cout << "The value in pointer variable ptr is: "<<(void*)ptr << endl;

    cout << "the address of variable b is: "<<&a << endl;
    ptr ++;
    cout<< "After increment the value in pointer variable ptr is: " << (void*)ptr << endl;
}
~~~
4)Pointer Integer
~~~ javascript
 //Mohit Singh Rawat
 //23070123086
 #include <iostream>
using namespace std;
int main()
{
    int a = 10;
    int *ptr;
    ptr=&a;
   cout<< "The value pointed by *ptr is: "<<*ptr << endl;
    cout << "The value in b is: " <<a << endl;
    cout << "The value in pointer variable ptr is: "<<(void*)ptr << endl;

    cout << "the address of variable b is: "<<&a << endl;
    ptr ++;
    cout<< "After increment the value in pointer variable ptr is: " << (void*)ptr << endl;
}
~~~
5)Without Pointer
~~~ javascript
//Mohit Singh Rawat
//23070123086
#include<iostream>
using namespace std;
int main()
{
    int *ptr;
    int a[5] = { 1,2,4,8,9};
    ptr = &a[0];
    int i;
    for(i=0 ; i<5 ; i++)
    {
        cout << "Element "<< i+1 <<" "<<"="<<" "<<*(a+i) << endl;
        ptr ++;

    }
}
~~~
6)Pointer Call By Reference
~~~ javascript
//Mohit Singh Rawat
//23070123086
#include <iostream>
using namespace std;
void swap (int a,int b)
{
    int temp;
    temp=a;
    a=b;
    b=temp;
    cout<<"Inside swap a: "<<a<<" b: "<<b<<endl;
}

int main()
{
   int a=11,b=22;
   cout<<"Before swap a: "<<a<<" b: "<<b<<endl;
   swap(a,b);
   cout<<"After swap a:"<<a<<" b:"<<b<<endl;
    return 0;
}
~~~
7)Pointer Call By Value
~~~ javascript
#include <iostream>
using namespace std;
void swap (int a,int b)
{
    int temp;
    temp=a;
    a=b;
    b=temp;
    cout<<"Inside swap a: "<<a<<" b: "<<b<<endl;
}

int main()
{
   int a=11,b=22;
   cout<<"Before swap a: "<<a<<" b: "<<b<<endl;
   swap(a,b);
   cout<<"After swap a:"<<a<<" b:"<<b<<endl;
    return 0;
}
~~~

### Program Outputs
1) <img width="316" alt="Screenshot 2024-08-31 at 3 42 18 PM" src="https://github.com/user-attachments/assets/5a2fe881-94f0-43d5-8e15-b013bd3322af">
2) <img width="586" alt="Screenshot 2024-08-31 at 3 45 04 PM" src="https://github.com/user-attachments/assets/96a4c2d0-8b0c-4533-9a67-93be5a963c0a">
3) <img width="597" alt="Screenshot 2024-08-31 at 3 46 08 PM" src="https://github.com/user-attachments/assets/d49e2c23-3044-4b2b-85ea-3feaf9c35530">
4) <img width="592" alt="Screenshot 2024-08-31 at 3 47 33 PM" src="https://github.com/user-attachments/assets/115c2582-cc6b-4540-8dfa-9bd07a4bb66d">
5) <img width="295" alt="Screenshot 2024-08-31 at 3 48 38 PM" src="https://github.com/user-attachments/assets/5ae9b82e-d4ed-4fc3-9098-5aa1acd057f7">
6) <img width="294" alt="Screenshot 2024-08-31 at 3 49 22 PM" src="https://github.com/user-attachments/assets/b412289b-b317-46d1-a393-63054e2082cb">
7) <img width="300" alt="Screenshot 2024-08-31 at 3 50 17 PM" src="https://github.com/user-attachments/assets/667c7007-34a6-4981-9b9b-23062e4a533c">

### Conclusion <br>
In simple terms, pointers in C++ let you work directly with memory addresses, making it easier to manage data and memory. They are especially useful for functions that need to change the original data or work with large amounts of data efficiently. Using pointers, you can modify data directly and handle dynamic memory more effectively.
