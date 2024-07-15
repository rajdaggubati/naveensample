import java.util.Scanner;

public class PrimeNumber {

    // Method to check if a number is prime
    static boolean isPrime(int num) {
        // Corner case: Handle numbers less than 2
        if (num <= 1) {
            return false;
        }

        // Check from 2 to sqrt(num) for factors
        for (int i = 2; i * i <= num; i++) {
            if (num % i == 0) {
                return false; // Found a factor, hence not prime
            }
        }
        return true; // If no factors found, then it is prime
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = scanner.nextInt();

        if (isPrime(num)) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }

        scanner.close();
    }
}
