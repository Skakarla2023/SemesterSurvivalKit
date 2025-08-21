package com.skakarla.java_Programs;

import java.util.Scanner;

public class Prime_Number {
    public static void main(String[] args) {
        Scanner obj = new Scanner(System.in);
        System.out.println("Enter a number:");
        int n = obj.nextInt();

        System.out.println("Prime numbers up to " + n + " are:");
        for (int i = 2; i <= n; i++) {
            if (isPrime(i)) {
                System.out.print(i + " ");
            }
        }

        obj.close();
    }

    // Function to check if a number is prime
    private static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
}
