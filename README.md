# AccountBalance

import java.util.Scanner;

public class P49_AccountBalance {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int numPayment = Integer.parseInt(scanner.nextLine());
        double balance = 0;

        while (numPayment > 0) {
            double payment = Double.parseDouble(scanner.nextLine());
            if (payment < 0) {
                System.out.println("Invalid operation!");
                System.out.printf("Total: %.2f", balance);
                return;
            }
            System.out.printf("Increase: %.2f%n", payment);
            balance += payment;
            numPayment--;
        }
        System.out.printf("Total: %.2f%n", balance);
    }
}
