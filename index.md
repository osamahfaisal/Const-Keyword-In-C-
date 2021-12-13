#   using of keyword const and & operation in c++ 
## using of keyword const 

![image](https://user-images.githubusercontent.com/93501065/145822193-8e0bfa13-7cda-4af3-9e19-9934daa7dee1.png)
 

- <font size = "5">The const keyword allows you to specify whether or not a variable is modifiable. In C language and C++ we use the keyword const to make program elements constant. 
const keyword can be used in many contexts in a C++ program , as the following :</font>



 <font size ="5">**1. constant variable** </font>
   - If you make any variable as constant ,you can't change its value .Also,the constant variables must be initialized while they are declared
   - example : 
```
const int i = 10 ; 
i ++ ;  // this leads to Compile time error 
```


![image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Constants-in-C.png)



2.  <font size ="5">**pointer with const keyword** </font>
- we can do it in two ways.

a. **Pointer to a const variable:** This means that the pointer is pointing to a const variable as :
```
const int* u;  // in this case the pointer point to a const variable 
```
b. **const pointer :** we can't change the pointer, which means it will always point to the variable  but can change the value that it points to, by changing the value of variable as :
```
int x = 1 ;
int *const y =&x ;
```

- this image illustrate constant pointer and Pointer to a const variable


![image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/PointersWithConstants-1024x535.png)



3. <font size ="5">**const Function argument and return type**</font>:We can make the return type or arguments of a function as const. Then we cannot change any of them as :

```
void function1(const int x ){  // void function with const argument
x=25 //  this leads to Compile time error becouse x is const argument 
}
```

```
const int function(){
return 2 ;  // if we try put variable instead it will give us error
}
```

4.<font size="4">**Defining Class Data members as const :** </font>They are not initialized during declaration Their initialization by constructor when create object as :
```
class C
{
    const int j;
    public:
    C (int x):j(x)  // initialzed when create a new object 
    };
int main()
{
    Test t(10);
    Test s(20);
}
```

5. <font size = "5" >**Defining Class Object as const**</font>: When an object is declared or created using the const keyword, its data members can never be changed, during the object's lifetime 
   - For example, if in the class C defined above, we want to define a constant object, we can do it like:
```
const C r(30);

```
6. <font size ="5">**Defining Class's Member function as const :**</font> A const member functions never modifies data members in an object.
   - its syntax is 
```
return_type function_name() const;
```
 
 - Also shown in the following class is a const constructor in the creat object and a const method : 

````
class Something
{
public:
    int m_value {};

    Something(): m_value{0} { }

    void setValue(int value) { m_value = value; }
    int getValue() const  { return m_value ; }  // const method 
};

int main()
{
    const Something something{}; // calls default constructor

    something.m_value = 5; // compiler error: violates const
    something.setValue(5); // compiler error: violates const

    return 0;
}
````



## & operation in c++


1. <font size ="5">**&& Logical AND.**</font>  True only if all the operands are true

````
if(x<y && z==g) 
 cout<< "True"<<endl // if the two parts are true the out put are true 
else 
cout<<"False "<<  // if any or both part ar false 

````

2. <font size ="5">**& represent memory address  :**</font>
````
int x =15 ; 
int *y =&x ; 
cout<< y <<endl // this will be display the refrance of x 

````
3. <font size ="5" >  & bitwise AND in C or C++ takes two numbers as operands and does AND on every bit of two numbers. The result of AND is 1 only if both bits are 1</font>

