# pruebagitimport java.util.Scanner;

public class Calculadora {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double num1, num2;
        char operator;

        System.out.println("Calculadora Simple");
        System.out.print("Ingresa el primer número: ");
        num1 = scanner.nextDouble();

        System.out.print("Ingresa el operador (+, -, *, /): ");
        operator = scanner.next().charAt(0);

        System.out.print("Ingresa el segundo número: ");
        num2 = scanner.nextDouble();

        double resultado = 0;

        switch (operator) {
            case '+':
                resultado = num1 + num2;
                break;
            case '-':
                resultado = num1 - num2;
                break;
            case '*':
                resultado = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    resultado = num1 / num2;
                } else {
                    System.out.println("Error: No se puede dividir por cero.");
                    return;
                }
                break;
            default:
                System.out.println("Operador inválido.");
                return;
        }
        ###modificacion

        System.out.println("El resultado es: " + resultado);
    }
}
