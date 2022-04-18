# Reading-user-input
collecting user input of (int) and retuning the sum if input == 10

import java.util.Scanner;

public class Exercises {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sum = 0;
        int x = 0;
        int count = 0;
        while (true) {
            x = count + 1;
            System.out.println("Enter your number #" + x + ":");
            boolean hasNextInt = scanner.hasNextInt();
            if(hasNextInt){
                count++;
                int input = scanner.nextInt();
                sum+= input;
                if(count == 10){
                    break;
                }
            } else {
                System.out.println("Invalid number");
            }
            scanner.nextLine();
        }
        System.out.println("Total is: " + sum);
        scanner.close();
    }
}
