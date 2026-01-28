# my--experiments-1
## Experiment 1a: Default Primitive Type
### java Code:
```
java
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
##output:
![output](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/e94ea853117b63b2bc630a50049b97d5a3d98d43/1a.0utput.png)

### 1b.QUADRATIC EQUQTION SOLUTION:
### java code
```
import java.util.Scanner;
class QuadraticEquationSolution {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a value of a:");
        double a = sc.nextDouble();
        System.out.println("Enter a value of b:");
        double b = sc.nextDouble();
        System.out.println("Enter a value of c:");
        double c = sc.nextDouble();
        double D = b * b - 4 * a * c;
        if (D > 0) {
            double x1 = (-b + Math.sqrt(D)) / (2 * a);
            double x2 = (-b - Math.sqrt(D)) / (2 * a);
            System.out.println("Roots are real and distinct:");
            System.out.println("x1 = " + x1);
            System.out.println("x2 = " + x2);
        } 
        else if (D == 0) {
            double y = -b / (2 * a);
            System.out.println("The roots are real and equal:");
            System.out.println("y = " + y);
        } 
        else {
            double real = -b / (2 * a);
            double img = Math.sqrt(-D) / (2 * a);
            System.out.println("Roots are complex:");
            System.out.println("x1 = " + real + " + " + img + "i");
            System.out.println("x2 = " + real + " - " + img + "i");
        }
        sc.close();
    }
}
```
##OUTPUT:
![output](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/ed71c6071b6ec94e320cc9d29dbe5e655e86c777/Screenshot%202025-12-30%20170135.png)
## title : rectangke
```
  class Rectangle {
        double length;
        double breadth;
 double area() {
        return length * breadth;
        }
 double perimeter() {
        return 2*(length + breadth);
        }
 }
  class main {
     public static void main(String args[]) {
      Rectangle rect = new Rectangle();
      rect.length = 12;
      rect.breadth = 20;
      double area = rect.area();
      double perimeter = rect.perimeter();
  System.out.println("Area of given Rectangle:"+area);
  System.out.println("perimeter of given rectangle:"+perimeter);
}
}
```
## output:
![output for rectangle](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/a49ace221df2460a2b1eba765c178510b422f85f/2a.output.png)
## title: 2b) method overloading
```
  class sum {
     int sum(int a,int b) {
     return a+b;
     }
     int sum(int a,int b,int c) {
     return a+b+c;
     }
     double sum(double a,double b) {
     return a+b;
     }
   }
  class main {
     public static void main(String args[]) {
      sum S = new sum();
 System.out.println("sum of 2 integers:"+S.sum(30,40));
 System.out.println("sum of 3 integers:"+S.sum(39,56,78));
 System.out.println("summ of real numbers:"+S.sum(20-456,22-564));
 }
}
```
## output:
![output for Methodoverloading](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/53da6b241f6f15357bd3d3e0ab87fc439b10f6ae/2b.output.png)
## title 2c) construtor
```
  class student {
     String Sname;
     int Sage;
     double Smarks;
     student(String name,int age,double marks) {
     Sname = name;
     Sage = age;
     Smarks = marks;
     }
     void display() {
     System.out.println("student name:"+Sname);
     System.out.println("student age:" +Sage);
     System.out.println("student marks:" +Smarks);
     }
}
  class main {
     public static void main(String args[]) {
      student S = new student("yagna:",19,600);
      S.display();
}
}

```
