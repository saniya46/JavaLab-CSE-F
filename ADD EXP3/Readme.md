# addtional experiment3
## 3)palindrome
```
import java.util.Scanner;

public class PalindromeString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String str = sc.nextLine();
        String reverse = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reverse = reverse + str.charAt(i);
        }
        if (str.equals(reverse)) {
            System.out.println("The string is a Palindrome");
        } else {
            System.out.println("The string is NOT a Palindrome");
        }
        sc.close();
    }
}
```
# output
<img width="358" height="31" alt="3A ADD OUTPUT" src="https://github.com/user-attachments/assets/dca5feb5-9901-4a2a-8073-fb9c2156b73c" />
