# experiment2
## TITLE: 2a.) Implement class mechanism in java 
```
class myclass {
void displaymessage() {
System.out.println("welcome to java");
}
int add (int a, int b) {
return a+b;
}
public static void main(String[] args) {
myclass obj = new myclass();
obj.displaymessage();
int result = obj.add(10, 20);
System.out.println("sum: " + result);
}
}
```
# output
<img width="1161" height="479" alt="2a output" src="https://github.com/user-attachments/assets/df63321c-5937-48b4-b93e-ffea2f4ed21a" />



# experiment2b
## TITLE: 2b.) java program implement method overloading
```
class OverloadExample {
int add(int a, int b) {
return (a + b);
}
double add(double a, double b) {
return a + b;
}
int add(int a, int b, int c) {
return a + b + c;
}
public static void main(String[] args) {
OverloadExample obj = new OverloadExample();
int sum1 = obj.add(10, 20);
double sum2 = obj.add(5.5, 6.5);
int sum3 = obj.add(10, 20, 30);
System.out.println("Result of adding two integers: " + sum1);
System.out.println("Result of adding two double values: " + sum2);
System.out.println("Result of adding three integers: " + sum3);
}
}
 ```
<img width="1438" height="403" alt="2b  output" src="https://github.com/user-attachments/assets/d733f312-e55e-4ed4-a25b-8bc988b02ee5" />


# experiment2c
## TITLE:2C.) java program implement constructor
```
class Student {
String name;
int age;
int marks;
Student (String n, int a, int m) {
name = n;
age = a;
marks = m;
}
void display ( ) {
System.out.println ("Name: " + name);
System.out.println ("Age: " + age);
System.out.println ("Marks: " + marks);
}
public static void main(String[] args) {
Student S1 = new Student ("Alice", 20, 85);
S1.display ( );
}
}
```
# output

<img width="390" height="159" alt="2c output" src="https://github.com/user-attachments/assets/a43ab9d9-5487-4915-bee9-7489d2e83fdf" />

