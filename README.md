# java-codes
import java.util.Scanner;

public class Hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int original = n;
        int sum = 0;
        int count = 0;
        while (n > 0) {
            count++;
            n = n / 10;
        }
        n = original;
        while (n > 0) {
            int digit = n % 10;

            sum = sum + (int) Math.pow(digit, count);

            n = n / 10;
        }

        if (sum == original) {
            System.out.println("Armstrong number.");
        } else {
            System.out.println("not Armstrong number.");
        }

    }
}
