# Basics of JAVA
## OOPS Concepts:
### Objects: Everything is a Object,  instance of the class
### Class:
```JAVA
//Class
class Human{
  public int age;
  public String name;

  public void introduce(){
    System.out.println("I'm"+name+"and I'm"+age+"years old");
  }
}

//Object Creation
Human amanda = new Human();    // Create amanda.
amanda.age = 6;                // Set amanda's fields.
amanda.name = "Amanda";
amanda.introduce();            // _Method_call_ has amanda introduce herself.
// Using default contructor here
// The output is:    I'm Amanda and I'm 6 years old
```
#### Constructors: Same name as the class
```JAVA
class Human {
  // Include all the stuff from the previous definitions here.

  public Human(String givenName) {
    age = 6;
    name = givenName;
  }
}

Human amanda = new Human("Amanda");
amanda.introduce();
// The output is:    I'm Amanda and I'm 6 years old
```
#### "this" Keyword: if the parameters or local variables of a method have the same name as the fields of an object, then the former have priority, and the "this" keyword is needed to refer to the object's fields.
```JAVA
public void change(int age) {
   String name = "Tom";

   this.age = age;
   this.name = name;
 }
 //Calling
amanda.change(11)
// Output: I'm Tom and I'm 11 years old
```
- You CANNOT change the value of "this"!

#### Static Keyword: Its the single variable shared by a whole class of objects; its value does not vary from object to object
- In a static method, THERE IS NO "this"!

#### Lifetimes of Variables
- A local variable (declared in a method) is gone forever as soon as the method in which it's declared finishes executing.  (If it references an object, the object might continue to exist, though.)
- An instance variable (non-static field) lasts as long as the object exists. An object lasts as long as there's a reference to it.
- A class variable (static field) lasts as long as the program runs

```JAVA
public static void main(String[] args) {
```
- The public keyword means that the method is available to the outside world
- The argument to main( ) is an array of String objects.
- The args won’t be used in this program, but the Java compiler insists that they be there because they hold the arguments from the command line.  
- Overflow after promotion
```JAVA
public class Overflow {
 public static void main(String[] args) {
   int big = Integer.MAX_VALUE;
 System.out.println("big = " + big);
 int bigger = big * 4;
 System.out.println("bigger = " + bigger);
 }
} /* Output:
big = 2147483647
bigger = -4
*///:~
```
- `for(initialization; Boolean-expression; step)`
- Foreach syntax:
```JAVA
public class ForEachString {
 public static void main(String[] args) {
 for(char c : "An African Swallow".toCharArray() )
 System.out.print(c + " ");
 }
} /* Output:
A n A f r i c a n S w a l l o w
*///:~
```

- foreach will also work with any object that is Iterable
-
