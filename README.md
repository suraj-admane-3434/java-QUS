# java-QUS
//######################################QUS 1#############################################
public class DataTypesDemo {
    public static void main(String[] args) {
        // 1. Variable declarations
        int intNum = 25;
        double doubleNum = 5.5;
        char letter = 'A';
        boolean isJavaFun = true;
        String message = "Hello, ";

        // 2. Basic arithmetic operations
        int sum = intNum + 10;
        int difference = intNum - 5;
        double product = doubleNum * 2.0;
        double quotient = doubleNum / 2.0;

        // 3. String concatenation
        String fullMessage = message + "Java World!";

        // 4. Display the results
        System.out.println("Integer value: " + intNum);
        System.out.println("Double value: " + doubleNum);
        System.out.println("Character value: " + letter);
        System.out.println("Boolean value: " + isJavaFun);
        System.out.println("Sum (intNum + 10): " + sum);
        System.out.println("Difference (intNum - 5): " + difference);
        System.out.println("Product (doubleNum * 2.0): " + product);
        System.out.println("Quotient (doubleNum / 2.0): " + quotient);
        System.out.println("Concatenated message: " + fullMessage);
    }
}

//######################################QUS 2##########################################################

public class ArrayOperations {
    public static void main(String[] args) {
        // 1. Create and initialize the array
        int[] numbers = {10, 20, 30, 40, 50};

        // Variables for sum, largest, and smallest
        int sum = 0;
        int largest = numbers[0];
        int smallest = numbers[0];

        // 2. Loop through the array to calculate sum, find largest and smallest
        for (int num : numbers) {
            sum += num;
            if (num > largest) {
                largest = num;
            }
            if (num < smallest) {
                smallest = num;
            }
        }

        // 3. Calculate average
        double average = (double) sum / numbers.length;

        // 4. Display the results
        System.out.print("Array elements: ");
        for (int num : numbers) {
            System.out.print(num + " ");
        }
        System.out.println();  // New line after array output

        System.out.println("Sum of array elements: " + sum);
        System.out.println("Average of array elements: " + average);
        System.out.println("Largest element: " + largest);
        System.out.println("Smallest element: " + smallest);
    }
}

//#######################################QUS 3#################################################

import java.util.Scanner;

public class VotingEligibility {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // 1. Get user input for age
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        scanner.nextLine(); // Consume newline

        // 2. Check age using if-else
        if (age >= 18) {
            // 3. Nested if-else for valid ID
            System.out.print("Do you have a valid ID? (yes/no): ");
            String hasID = scanner.nextLine();

            if (hasID.equalsIgnoreCase("yes")) {
                System.out.println("You are eligible to vote.");
            } else {
                System.out.println("You need a valid ID to vote.");
            }
        } else {
            System.out.println("You are not eligible to vote.");
        }

        scanner.close();
    }
}
