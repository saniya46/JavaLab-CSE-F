# experiment 6a
## title 6a)Describe exception handling mechanism
```
import java.util.Scanner;
import java.util.InputMismatchException;

public class MultipleCatchExample {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Creating an integer array
        int arr[] = {10, 20, 30, 40, 50};

        try {
            // Taking two numbers from user
            System.out.print("Enter first number: ");
            int a = sc.nextInt();

            System.out.print("Enter second number: ");
            int b = sc.nextInt();

            // Division operation
            int result = a / b;
            System.out.println("Result of division: " + result);

            // Accessing array element
            System.out.print("Enter index to access array element: ");
            int index = sc.nextInt();

            System.out.println("Element at index " + index + " = " + arr[index]);
        }

        catch (ArithmeticException e) {
            System.out.println("Error: Division by zero is not allowed.");
        }

        catch (InputMismatchException e) {
            System.out.println("Error: Please enter numeric values only.");
        }

        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Invalid array index.");
        }

        catch (Exception e) {
            System.out.println("Some other error occurred.");
        }

        finally {
            System.out.println("Program continues...");
            sc.close();
        }
    }
}
```
# output:
![6a](https://github.com/user-attachments/assets/424773c9-952c-469b-bc57-e2e89a0a163c)
