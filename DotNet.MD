### Dotnet Notes

- It can be used to create DesktopApps, WebApps, MobileApps
- it has more than 30 languages implemented for development(any developer can work in dotnet environment)
- .NET Core is ObjectOriented, platform independent, language independent
- C# is most developed and powerful language among all available for development

*namespace* is logical container for the classes
*classes are logically collected in namespaces no need to create folder for the physical seperation*
 -objects with main methods will be the entry points
 -One solution will have one entry point
 -In c# method names start with Capital and follows camelCasing
 
 **CONSTRUCTORS**
 constructors in C# are mainly:
a. responsible for initializing the variables in the class
b. name of these constructor method is same as class without any return type
c. classes will have default public parameterless constructors and others (if required) need to be declared explicitly
d. every instance creation will give call to the constructor.
  Default scope of classed in C# is private...
 *Types of constructors: Default, parameterized, copy constructor(class instance is parameter), static constructor(similar to static initializer block)*
 
   **Variables, instance and reference of a class**
   - members can have access modifiers like : private (only accessible inside the class), public(accessible everywhere), internal(this is accessible inside the project) , protected( can be accessed inside the chiled classes), protcted internal(inside the prohject as well as in child classes)
   - *Variables can be declared as* : const, static, non-static, readOnly
   - for non-static variables memory is allocated after the instance is created and hence the constructor is required. It can be initialized *n* times with every *n* instance creations.
   -static variables and const variables declared at the time of class loading. static variable value can be changed but const is initialized only once throughout execution and must be initialized at the time of declaration only.
   - readonly cannot be modified once initialized
   
   
   **INHERITANCE**
   
   -Consuming of members of one class into another class. Private members cannot be accessed.
   - `class A{} class B:A{}1 syntax
   - parent, super, base || child, sub, derived
   - *imp points*
   1. parent class constructor must be accessible to child class if it is parameterized parameters are to be passed using `base` keyword (it implicitly calls default constructor at the time of every instance creationn). 
   2. parent cannot access any member of child class
   3. Every class in C# is inheriting Object class which is also known as Universal base/super class of all classes
   4. only overridden methods of child class will be accessed if child instance is copied into parent reference. i.e. Parent p=new Child();
but if the accessed method is not overridden in child class then the parent class's method will be called
  5. object class methods : GetType(), GetHashCode(), Equals(), ToString()
  
    *Types of Inheritance*
    a. Multilevel
    b. Single
    c. Hierarchical
    d. Multiple
    e. Hybrid (c+d)
    
    Here in C# multiple inheretance is not supported (we use Interfaces)
    
   -Application Creation process Explained:
I. identify all the entities
II. List out all the attributes for each of the entity and identify common attributes
III. Declare general classes with those attributes and common methods in general class
IV. Inherit and reuse to avoid the redundency

**Method OverLoading, OverRiding, Hiding, Operator overLoading**
- *Method Overloading* is declaring with the same name and return type but, different signatures
- *Method Overriding* works in between classes i.e. inheritance. It requires parent class permission to override method in child class. The `virtual` keyword in parent class allows overriding of the methods (same parameters, return type and name)
- *Method Hiding* of methods just uses `new` keyword to suppress warning (even if we do not use it i acceptable) and use the same method name as in base class which is not having declared `virtual`.
  
  base and this keywords are important...
  calling parent constructor from child class :- public Child() : this(a,b){} ----> here a and b are required parameters in parent class
 - *OperatorOverLoading* helps in changing the predefined functionality of operator based on type of operands.
    e.g. int a,b;
a+b is addition
 e.g. string a,b;
a+b is concatenation

declaration: 
`public static return_type_Operand operator 
+(Operand a, Operand b){//required logic}`

 **Abstract methods and Classes**
- The methods without any execution logic are declared as abstract methods
- If a class has any one of the method abstract the class must be declared abstract
- abstract classes can have both abstract and non abstract methods
- if a class inherits any abstract class it is **MUST** to override all the abstract methods in it even if it does not use them all
- Abstract class instance cannot be created only reference can be created because, this may be countering the part of inaccessibility of methods in class and developer may access unimplemented methods using instance.
    
