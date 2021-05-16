# Object Oriented Programming
## Class
Its like a signature which consists all data methods access specifiers etc
```cpp
class Person{
    // your Code
};
```
- this is a pointer to the class itself
```cpp
class Person{
    int a=10;
public:
    Person(int a){
        cout<<a;//5
        cout<<this->a;//10
    }
};
int main(){
    Person p(5);
}
```
## Object
Instance of class is called a object
```cpp
Person P;
```
Some Other terms in class
- data : all data elementrs
- methods: all functions
- constructor: A method with name of class (no return type needed)
- Destructor: A method with name ~followed by name of class
- Constructor is called at initialization of class
- Destructor is called at end of class (when class scope ends);
 
## Static Data in Class [^1]
- Data is not created in every instance
- It is the shared data between all instances
- We can access static data by using acessSpecifier (::) 
```cpp
class Person{
    static int x;
    static printX(){
        cout<<x;
    };
}
int main(){
    Person::x=5;
    Person::printX();//5 is printed
}
```
Example2:
```cpp
class Person{
    static int x;
    static printX(){
        cout<<x;
    };
    Person(){
        x+=2;
    }
}
int main(){
    Person::x=5;
    Person::printX();//5 is printed
    Person p;
    Person::printX();//7 is printed
}
```
## Abstraction
Hiding Unnesassary data
### Acess Specifiers
-  ```public```: Allowed from anywhere
-  ```private```: Allowed only in class
-  ```protected```: Allowed in class and in inherited classes

## Encapsulation
The process of placig all methods data and related content at one place is called Encapsulation
## Inheritence
## Polimorphism
> many forms in one name
### Compile Time polimorphism
> Resolves at compile time
- functional overloading
- operator overloading
### Functional Overloading
- same name can be used multiple times.
- Which code to use will depend on set of arguments passed.
- All these types of overloading are possible.
```cpp
func();
func(int a);
func(double a);
func(int a,int b);
func(int a,double b);
```

### Operator overloading
- same as function overloading but we use operatrs here
-  No of arguments must be fixed i.e 2 for binary and 1 for unary operands
```cpp
int operator+(int a,int b){

}
```
- we can reduce one argument while using in a class and then first arg is from class
```cpp
class Person(){
    int val;
public:
    int operator+(int a){
        return this->val+a;
    }
}
```
- list of symbols which cant be overloaded
```WIP```

### Function hiding
> while using inheritence if a function of base class is rewritten in derived class then all copies of the function in base class are no longer useful and those which are in dervied class are used

Example
```cpp
class Base{
public:
    func();
    func(int,int);
    func(int);
    func(int,double);
};
class Derived:public Base{
public:
    func(int);//as this is declared all the four func methods in Base are no longer accessible  (THEY ARE HIDDEN);
};
```
(NO LONGER ACCESSIBLE FROM OUTSIDE BUT CAN BE USED INTERNALLY [^1])


[^1]: Subject to change Doubt in this part.