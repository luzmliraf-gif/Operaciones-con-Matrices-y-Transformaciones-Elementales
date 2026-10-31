package algebralineal;

import java.util.Scanner;

public class operacionesconmatrices {

    static Scanner entrada = new Scanner(System.in);

    // Mostrar matriz con formato ordenado
    public static void mostrarMatriz(double[][] matriz) {
        for (double[] fila : matriz) {
            for (double valor : fila) {
                System.out.printf("%10.2f", valor);
            }
            System.out.println();
        }
    }

    // Leer matriz desde la consola
    public static double[][] leerMatriz(String nombre) {
        System.out.print("Filas de la matriz " + nombre + ": ");
        int filas = entrada.nextInt();
        System.out.print("Columnas de la matriz " + nombre + ": ");
        int columnas = entrada.nextInt();

        double[][] matriz = new double[filas][columnas];
        System.out.println("Ingrese los valores de la matriz " + nombre + ":");
        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < columnas; j++) {
                System.out.print(nombre + "[" + (i + 1) + "][" + (j + 1) + "]: ");
                matriz[i][j] = entrada.nextDouble();
            }
        }
        return matriz;
    }

    // 1. Suma de matrices
    public static void sumarMatrices() {
        System.out.println("\n--- SUMA DE MATRICES ---");
        double[][] A = leerMatriz("A");
        double[][] B = leerMatriz("B");

        if (A.length != B.length || A[0].length != B[0].length) {
            System.out.println("Error: Las dimensiones de ambas matrices deben ser iguales.");
            return;
        }

        double[][] resultado = new double[A.length][A[0].length];
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                resultado[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("\nResultado de la Suma (A + B):");
        mostrarMatriz(resultado);
    }

    // 2. Resta de matrices
    public static void restarMatrices() {
        System.out.println("\n--- RESTA DE MATRICES ---");
        double[][] A = leerMatriz("A");
        double[][] B = leerMatriz("B");

        if (A.length != B.length || A[0].length != B[0].length) {
            System.out.println("Error: Las dimensiones de ambas matrices deben ser iguales.");
            return;
        }

        double[][] resultado = new double[A.length][A[0].length];
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                resultado[i][j] = A[i][j] - B[i][j];
            }
        }

        System.out.println("\nResultado de la Resta (A - B):");
        mostrarMatriz(resultado);
    }

    // 3. Producto de una matriz por un escalar
    public static void multiplicarEscalar() {
        System.out.println("\n--- PRODUCTO DE UNA MATRIZ POR UN ESCALAR ---");
        double[][] A = leerMatriz("A");
        System.out.print("Introduce el valor del escalar (k): ");
        double k = entrada.nextDouble();

        double[][] resultado = new double[A.length][A[0].length];
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                resultado[i][j] = k * A[i][j];
            }
        }

        System.out.println("\nResultado del Producto (k * A):");
        mostrarMatriz(resultado);
    }

    // 4. Matriz traspuesta
    public static void matrizTraspuesta() {
        System.out.println("\n--- MATRIZ TRASPUESTA ---");
        double[][] A = leerMatriz("A");

        int filas = A.length;
        int columnas = A[0].length;
        double[][] resultado = new double[columnas][filas];

        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < columnas; j++) {
                resultado[j][i] = A[i][j];
            }
        }

        System.out.println("\nMatriz Traspuesta (A^T):");
        mostrarMatriz(resultado);
    }

    // 5. Multiplicación de matrices
    public static void multiplicarMatrices() {
        System.out.println("\n--- MULTIPLICACIÓN DE MATRICES ---");
        double[][] A = leerMatriz("A");
        double[][] B = leerMatriz("B");

        if (A[0].length != B.length) {
            System.out.println("Error: Las columnas de A deben coincidir con las filas de B.");
            return;
        }

        int filasA = A.length;
        int columnasB = B[0].length;
        int comun = B.length;

        double[][] resultado = new double[filasA][columnasB];

        for (int i = 0; i < filasA; i++) {
            for (int j = 0; j < columnasB; j++) {
                for (int k = 0; k < comun; k++) {
                    resultado[i][j] += A[i][k] * B[k][j];
                }
            }
        }

        System.out.println("\nResultado de la Multiplicación (A * B):");
        mostrarMatriz(resultado);
    }

    // Menú principal
    public static void main(String[] args) {
        int opcion;

        do {
            System.out.println("\n===== OPERACIONES CON MATRICES =====");
            System.out.println("1. Suma de matrices");
            System.out.println("2. Resta de matrices");
            System.out.println("3. Producto de una matriz por un escalar");
            System.out.println("4. Matriz traspuesta");
            System.out.println("5. Multiplicacion de matrices");
            System.out.println("6. Salir");

            System.out.print("\nSelecciona una opcion: ");
            opcion = entrada.nextInt();

            switch (opcion) {
                case 1:
                    sumarMatrices();
                    break;
                case 2:
                    restarMatrices();
                    break;
                case 3:
                    multiplicarEscalar();
                    break;
                case 4:
                    matrizTraspuesta();
                    break;
                case 5:
                    multiplicarMatrices();
                    break;
                case 6:
                    System.out.println("Programa finalizado.");
                    break;
                default:
                    System.out.println("Opción no válida.");
            }

        } while (opcion != 6);
    }
}
