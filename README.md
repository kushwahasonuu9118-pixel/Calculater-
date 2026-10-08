import java.util.Scanner;

public class Calculator {

   
    static int add(int a, int b) {
        return a + b;
    }

  
    static int subtract(int a, int b) {
        return a - b;
    }

   
    static int multiply(int a, int b) {
        return a * b;
    }

   
    static int divide(int a, int b) {
        return a / b;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        switch (op) {

            case '+':
                System.out.println("Result = " + add(a, b));
                break;

            case '-':
                System.out.println("Result = " + subtract(a, b));
                break;

            case '*':
                System.out.println("Result = " + multiply(a, b));
                break;

            case '/':
                if (b != 0)
                    System.out.println("Result = " + divide(a, b));
                else
                    System.out.println("Cannot divide by zero!");
                break;

            default:
                System.out.println("Invalid operator!");
        }

        sc.close();
    }
}