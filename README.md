import java.util.Scanner;

public class Main {
    
    public static String Concatenation(String str1, String str2, String str3, String str4) {
        int len1 = str1.length();
        int len2 = str2.length();
        int len3 = str3.length();
        int len4 = str4.length();
        
        char[] strResult = new char[len1 + len2 + len3 + len4 + 3];

        int i = 0;
        
        while (i < len1) {
            strResult[i] = str1.charAt(i);
            i++;
        }
       
        strResult[i] = ' ';
        i++;
        
        int j = 0;
        while (i < len1 + len2 + 1) {
            strResult[i] = str2.charAt(j);
            i++;
            j++;
        }
        
        strResult[i] = ' ';
        i++;
        
        int x = 0;
        while (i < len1 + len2 + len3 + 2) {
            strResult[i] = str3.charAt(x);
            i++;
            x++;
        }
        
        strResult[i] = ' ';
        i++;
        
        int y = 0;
        while (i < len1 + len2 + len3 + len4 + 3) {
            strResult[i] = str4.charAt(y);
            i++;
            y++;
        }

        return new String(strResult);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your first name  : ");
        String str1 = scanner.nextLine();
        
        System.out.print("Enter your second name : ");
        String str2 = scanner.nextLine();
        
        System.out.print("Enter your middle name : ");
        String str3 = scanner.nextLine();
        
        System.out.print("Enter your last name   : ");
        String str4 = scanner.nextLine();
        
        String concatenatedName = Concatenation(str1, str2, str3, str4);
        System.out.println("Full Name: " + concatenatedName);
    }
}
