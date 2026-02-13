# Experiment 4a)
## title:4a)To implement single inheritance
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String insuranceNumber;

    Employee(String name, int age, double annualSalary, int yearOfJoining, String insuranceNumber) {
        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.insuranceNumber = insuranceNumber;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("Insurance Number: " + insuranceNumber);
    }
}

public class TestEmployee {
    public static void main(String[] args) {
        Employee emp = new Employee("Saniya", 20, 450000, 2024, "INS12345");
        emp.displayEmployeeDetails();
    }
}
```
# output
![4a output](https://github.com/user-attachments/assets/089f49fd-fc70-4fc6-b7cd-9808f0d9572c)







# Experiment 4b)
## title to implement multi-value inheritance
```
class Bicycle {
    String pedalType;

    Bicycle(String pedalType) {
        this.pedalType = pedalType;
    }

    void displayBicycle() {
        System.out.println("Pedal Type: " + pedalType);
    }
}

class MotorBike extends Bicycle {
    String engineType;

    MotorBike(String pedalType, String engineType) {
        super(pedalType);
        this.engineType = engineType;
    }

    void displayMotorBike() {
        displayBicycle();
        System.out.println("Engine Type: " + engineType);
    }
}

class ElectricBike extends MotorBike {
    String motorType;
    int batteryCapacity;

    ElectricBike(String pedalType, String engineType, String motorType, int batteryCapacity) {
        super(pedalType, engineType);
        this.motorType = motorType;
        this.batteryCapacity = batteryCapacity;
    }

    void displayElectricBike() {
        displayMotorBike();
        System.out.println("Motor Type: " + motorType);
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}

public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eb = new ElectricBike(
                "Standard Pedals",
                "Petrol Engine",
                "Electric Motor",
                500
        );

        eb.displayElectricBike();class Bicycle {
    String pedalType;

    Bicycle(String pedalType) {
        this.pedalType = pedalType;
    }

    void displayBicycle() {
        System.out.println("Pedal Type: " + pedalType);
    }
}

class MotorBike extends Bicycle {
    String engineType;

    MotorBike(String pedalType, String engineType) {
        super(pedalType);
        this.engineType = engineType;
    }

    void displayMotorBike() {
        displayBicycle();
        System.out.println("Engine Type: " + engineType);
    }
}

class ElectricBike extends MotorBike {
    String motorType;
    int batteryCapacity;

    ElectricBike(String pedalType, String engineType, String motorType, int batteryCapacity) {
        super(pedalType, engineType);
        this.motorType = motorType;
        this.batteryCapacity = batteryCapacity;
    }

    void displayElectricBike() {
        displayMotorBike();
        System.out.println("Motor Type: " + motorType);
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}

public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eb = new ElectricBike(
                "Standard Pedals",
                "Petrol Engine",
                "Electric Motor",
                500
        );

        eb.displayElectricBike();
    }
}
    }
}
```
# output
![4b output](https://github.com/user-attachments/assets/554e5334-a0ab-4ed6-812d-dff93d1296e2)













# Experiment 4c)
## Title 4c)Construct abstract class in java to find areas of different shapes
```
abstract class Figure {
    double dim1;
    double dim2;

    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }

    abstract double area();
}

// Rectangle class
class Rectangle extends Figure {

    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    // Override area method
    double area() {
        return dim1 * dim2;
    }
}

// Triangle class
class Triangle extends Figure {

    Triangle(double base, double height) {
        super(base, height);
    }

    // Override area method
    double area() {
        return 0.5 * dim1 * dim2;
    }
}

// Main class
public class TestFigure {
    public static void main(String[] args) {

        Figure rect = new Rectangle(10, 5);
        Figure tri = new Triangle(8, 6);

        System.out.println("Area of Rectangle: " + rect.area());
        System.out.println("Area of Triangle: " + tri.area());
    }
}
```
# output
![WhatsApp Image 2026-02-13 at 11 23 11 AM](https://github.com/user-attachments/assets/6f8ac7c2-12ae-47ce-aec9-d01cfa8db8fb)
