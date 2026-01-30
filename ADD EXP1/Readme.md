# experiment add1
## TITLE:1) INSERT SUB STRING
```
import java.util.Scanner;
public class InsertSubstring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the main string: ");
        String mainString = sc.nextLine();
System.out.print("Enter the substring to insert: ");
        String subString = sc.nextLine();
System.out.print("Enter the position to insert the substring: ");
        int position = sc.nextInt();
String result = mainString.substring(0, position) 
               + subString 
               + mainString.substring(position);
System.out.println("String after insertion: " + result);
sc.close();
    }
}
```
# output
