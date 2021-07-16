
```java
class A
{
    public A()
    {
        System.out.println("Class A Constructor");
    }
}
class B extends A
{
    public B()
    {
        System.out.println("Class B Constructor");
    }
}
class C extends B
{
    public C()
    {
        System.out.println("Class C Constructor");
    }
}
public class MainClass
{
    public static void main(String[] args)
    {
        C c = new C();
    }
}
```
# Answer
```
Class A Constructor
Class B Constructor
Class C Constructor
```
# b)
```java
class A
{
    String s = "Class A";
}
class B extends A
{

    String s = "Class B";
    {
        System.out.println(super.s);
    }
}
class C extends B
{
    String s = "Class C";
    {
        System.out.println(super.s);
    }
}
public class MainClass
{
    public static void main(String[] args)
    {
        C c = new C();
        System.out.println(c.s);
    }
}
```
# Answer
```
Class A
Class B
Class C
```
# c)
```java
public class classCommLine {
    public static void main(String args[]) {
        for(int i=0; i<args.length; i++)
            System.out.println("args[" + i + "]: " + args[i]);
    }
}
```
# Answer
# Command line Commands and output:
```
 45 65 75 85 33 44
args[0]: 45
args[1]: 65
args[2]: 75
args[3]: 85
args[4]: 33
args[5]: 44
```
# Q2. Can abstract class have constructors in Java?
# Answer:
```
Yes abstract class can have contructors and you can call 
these constructors by using super keyword in derived class .
```
# Q3. Create an abstract class 'Parent' with a method 'message'. It has two subclasses each having a method with the same name 'message' that prints "This is first subclass" and "This is second subclass" respectively. Call the methods 'message' by creating an object for each subclass.
# Answer:
```java
abstract class Parent
{
    abstract void message();
}

class firstSubClass extends Parent
{
    public void message()
    {
        System.out.println("This is first subclass");
    }
}
class secondSubClass extends Parent
{
    public void message()
    {
        System.out.println("This is second subclass");
    }
}
public class program {
    public static void main(String[] args) {
        firstSubClass message1 = new firstSubClass();
        message1.message();
        secondSubClass message2 = new secondSubClass();
        message2.message();
    }
}
```
# Output: 
```
This is first subclass
This is second subclass
```
# Q4. An abstract class has a construtor which prints "This is constructor of abstract class", an abstract method named 'a_method' and a non-abstract method which prints "This is a normal method of abstract class". A class 'SubClass' inherits the abstract class and has a method named 'a_method' which prints "This is abstract method". Now create an object of 'SubClass' and call the abstract method and the non-abstract method. (Analyse the result)
# Answer: 
```java
abstract class abstractClass
{
    public abstractClass() {
        System.out.println("This is constructor of abstract class");
    }
    abstract void a_method();
    public void nonAbstractMethod()
    {
        System.out.println("This is a normal method of abstract class");
    }
}
class Subclass extends abstractClass
{
    @Override
    void a_method() {
        System.out.println("This is abstract method");
    }
}
public class program2 {
    public static void main(String[] args) {
        Subclass sc = new Subclass();
        sc.a_method();
        sc.nonAbstractMethod();
    }
}
```
# Output:
```
This is constructor of abstract class
This is abstract method
This is a normal method of abstract class
```
# Q5. Write a java code to find whether a number is prime or not where number is accepted from command line.
# Answer: 
```java
public class prime {
    public static void main(String[] args) {
        int count = 0;
        int n=Integer.parseInt(args[0]);
        for(int i = 2;i<n;i++) {
            if (n % i == 0) {
                count = 1;
            }
        }
        if(count==0)
        {
            System.out.println(n+" is prime.");
        }
        else
        {
            System.out.println(n+" is not prime.");
        }
    }
}
```
# Output: 
```
 7
7 is prime.
 8 
8 is not prime.
```
