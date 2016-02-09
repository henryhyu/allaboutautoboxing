# allaboutautoboxing
All About Autoboxing

"Autoboxing" Defined (in java)!

Autoboxing: Automatic conversion of primitive types to the object of their corresponding wrapper classes is known as autoboxing. For example – conversion of int to Integer, long to Long, double to Double etc.

Unboxing: It is just the reverse process of autoboxing. Automatically converting an object of a wrapper class to its corresponding primitive type is known as unboxing. For example – conversion of Integer to int, Long to long, Double to double etc.

Primitive type -> Wrapper class

boolean -> Boolean

byte -> Byte

char -> Character

float -> Float

int -> Integer

long -> Long

short -> Short

double -> Double

Java 1.5 introduced a special feature of auto conversion of primitive types to the corresponding Wrapper class and vice versa.

Autoboxing: Automatic conversion of primitive types to the object of their corresponding wrapper classes is known as autoboxing. For example – conversion of int to Integer, long to Long, double to Double etc.

Unboxing: It is just the reverse process of autoboxing. Automatically converting an object of a wrapper class to its corresponding primitive type is known as unboxing. For example – conversion of Integer to int, Long to long, Double to double etc.

Primitive type	Wrapper class
boolean	        Boolean
byte	        Byte
char	        Character
float	        Float
int	        Integer
long	        Long
short	        Short
double	        Double

When does the autoboxing and unboxing happens in Java?

Case 1: When a method is expecting a wrapper class object but the value that is passed as parameter is a primitive type. 

For example in the below code, the method myMethod() is expecting an object of Integer wrapper class, however we passed a primitive int type. The program ran fine as compiler does the autoboxing (conversion of int to Integer)
```
class AutoboxingExample1
{
   public static void myMethod(Integer num){
	System.out.println(num);
   }
   public static void main(String[] args) {
       /* passed int (primitive type), it would be 
        * converted to Integer object at Runtime
        */
   	myMethod(2);
   }
}
```
Case 2: When at some point of time, you are assigning a primitive type value to an object of its wrapper class. 

For example: The below statements are valid because compiler does the autoboxing at runtime.

```
Integer inum = 3; //Assigning int to Integer: Autoboxing
Long lnum = 32L; //Assigning long to Long: Autoboxing
```

Case 3: When dealing with collection framework classes:

Here ArrayList class is expecting an Integer wrapper class object but we are providing int primitive.

```
ArrayList<Integer> arrayList = new ArrayList<Integer>();
arrayList.add(11); //Autoboxing - int primitive to Integer
arrayList.add(22); //Autoboxing
```

