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
## output:
![output fot constructor](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/bc8977b9b3370d1ac3e63a741596ae2288e69135/2c.output.png)
## title 3a) constructor overloading
```
class Student {
        String name;
        int age;
        double marks;
        Student() {
        }
        Student(String name,int age,double marks) {
                this.name = name;
                this.age = age;
                this.marks = marks;
                }
                void display() {
                System.out.println("name:" +name);
                System.out.println("age:" +age);
                System.out.println("marks:" +marks);
                }
             }

 class main {
     public static void main(String args[]) {
            Student std = new Student();
             std.display();
            Student std1 = new Student("yagna", 12,400);
             std1.display();
       }
      }
```
## output:
![output for constructor overloading](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/87e67743d0828851689d77910928f4b91f8105ff/3a.output.png)
## title 3b) Binarysearch
```
import java.util.Scanner;

class Binarysearch {
    int list[];
    int size;

    Binarysearch(int size) {
        this.size = size;
        list = new int[size];
    }

    void setlist() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the list items in Ascending order:");
        
        for (int i = 0; i < size; i++) {
            System.out.println("Enter value " + (i + 1) + ": ");
            list[i] = sc.nextInt();
        }
    }

    void getlist() {
        for (int i = 0; i < size; i++)
            System.out.print(list[i] + ",");
        System.out.println("\b\b.");
    }

    int Binarysearch(int key) {
        int low = 0;
        int high = list.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (list[mid] == key)
                return mid;

            else if (list[mid] < key)
                low = mid + 1;

            else
                high = mid - 1;
        }

        return -1; 
    }
}
import java.util.Scanner;

class main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        Binarysearch bs = new Binarysearch(10);

        bs.setlist();
        bs.getlist();

        System.out.println("Enter the key to search: ");
        int key = sc.nextInt();

        int index = bs.Binarysearch(key);

        if (index == -1)
            System.out.println("Key item does NOT exist.");
        else
            System.out.println("Key item exists at index: " + index);
    }
}
```
## output
![output for Binarysearch](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/0707d3510bbdd6174ae5fbc88f6e1808bb1bf3e5/vyshu3c.jpeg)
## title 3c) bubblesort
```
import java.util.Scanner;

class BubbleSort {
    void bubbleSort(int arr[]) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
import java.util.Scanner;
 class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int size = sc.nextInt();

        int arr[] = new int[size];

        for (int i = 0; i < size; i++) {
            System.out.print("Enter element " + (i + 1) + ": ");
            arr[i] = sc.nextInt();
        }

        BubbleSort bs = new BubbleSort();
        bs.bubbleSort(arr);

        System.out.print("Sorted array: ");
        for (int i = 0; i < size; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}
```
## output
[outpur for bubblesort](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/fcdf935eeece6ea3b3a8cc9a61fe7d000b22f3d7/vyshu3b.jpeg)
## title 4a) person
```
  class Person {
     String name;
     int age;

      Person(String name, int age) {
          this.name = name;
          this.age = age;
     }
     void displayPersonDetails() {
         System.out.println("Name : "+name);
         System.out.println("Age : "+age);
     }
  }
  class Employee extends Person {
     double annualSalary;
     int yearofJoining;
     String nationalInsuranceNumber;
     Employee(String name, int age, double annualSalary,int yearofJoining, String nationalInsuranceNumber) {
          super(name,age);
          this.annualSalary = annualSalary;
          this.yearofJoining = yearofJoining;
          this.nationalInsuranceNumber = nationalInsuranceNumber;
    }
    void displayEmployeeDetails() {
      displayPersonDetails();
      System.out.println("Annual Salary : " +annualSalary);
      System.out.println("Year of Joining :"+yearofJoining);
      System.out.println("nationalInsuranceNumber : "+nationalInsuranceNumber);
    }
 }
public class TestEmployee {
   public static void main(String args[]) {
       Employee emp1 = new Employee("yagna",20,1000000,2029,"NI80746828B");
       emp1.displayEmployeeDetails();
   }
}
```
## output
[output for person](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/fd948fc68e94760ea6c3e4ef19e6e6266fad631f/Screenshot%202026-01-30%20141840.png)
## title 4b) multilevel inheritance
```
  class Bicycle {
     String pedalType;
     void showBicycleInfo() {
         System.out.println("This is a bicycle with pedals:");
         System.out.println("Pedal Type :" + pedalType);
     }
}
  class ElectricBike extends Motorbike {
     int batteryCapacity;

     void showElectricBikeInfo() {
         System.out.println("This electric bike has an electric motor and battery.");
         System.out.println("Battery Capacity : " +batteryCapacity + "Wh");
     }
}
  class Motorbike extends Bicycle {
     int engineCapacity;

     void showMotorbikeInfo() {
        System.out.println("this motorbike has an engine.");
        System.out.println("Engine Capacity :" +engineCapacity + "cc");
     }
}
 public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();
        eBike.pedalType = "Standard pedals";
        eBike.engineCapacity = 255;
        eBike.batteryCapacity = 400;
        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
      }
 }
```
## output
[output for multilevel inheritance](https://github.com/kuchivyshnavi12/java-lab-cse-g/blob/ca1ec324475f34c301e9e7868fee4875ee88fb87/4b.output.png)
## 4c) dimensions in different shapes
```
  abstract class Figure {
      double dim1;
      double dim2;
      Figure(double dim1,double dim2) {
      this.dim1 = dim1;
      this.dim2 = dim2;
      }
 abstract double area();
 }
  class Rectangle extends Figure {
    Rectangle(double length,double breadth) {
             super(length,breadth);
   }
   double area() {
   double result = dim1*dim2;
   return result;
   }
}
  class Triangle extends Figure {
      Triangle(double base,double height) {
              super(base,height);
      }
     double area() {
            double result = 0.5*dim1*dim2;
            return result;
     }
}
  class TestFigure {
       public static void main(String args[]) {

       Figure f1 = new Rectangle(99.9,66.6);
       Figure f2 = new Triangle(88.8,55.5);


       System.out.println("Area of Rectangle = " +f1.area());
       System.out.println("Area of Triangle = " +f2.area());
       }
}
```
## output
[output for dimensions in different shapes]()



