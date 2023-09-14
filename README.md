import java.util.Scanner;

public class EvenOddArray {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get the size of the original array from the user
        System.out.print("Enter the size of the array: ");
        int size = scanner.nextInt();

        // Create the original array
        int[] originalArray = new int[size];

        // Input values into the original array
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            System.out.print("Enter element at index " + i + ": ");
            originalArray[i] = scanner.nextInt();
        }

        // Create separate arrays for even and odd numbers
        int[] evenArray = new int[size];
        int[] oddArray = new int[size];

        int evenCount = 0; // Number of even elements
        int oddCount = 0;  // Number of odd elements

        // Separate even and odd numbers into separate arrays
        for (int i = 0; i < size; i++) {
            if (originalArray[i] % 2 == 0) {
                evenArray[evenCount] = originalArray[i];
                evenCount++;
            } else {
                oddArray[oddCount] = originalArray[i];
                oddCount++;
            }
        }

        // Display the separate arrays for even and odd numbers
        System.out.println("\nEven numbers:");
        for (int i = 0; i < evenCount; i++) {
            System.out.print(evenArray[i] + " ");
        }

        System.out.println("\nOdd numbers:");
        for (int i = 0; i < oddCount; i++) {
            System.out.print(oddArray[i] + " ");
        }
    }
}
