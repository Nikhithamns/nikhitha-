/*a Java program to evaluate real roots of quadratic equation ax2 + b x + c = 0 using quadratic formula 
x = ( -b +/- sqrt(b*b – 4*a*c) ) / (2*a) . Program should print "complex Number" where roots are complex
i.e., when b*b – 4*a*c is negative or when a = 0 otherwise print results. */
import java.util.Scanner;

 class p6 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter the coefficients of the quadratic equation:");
        System.out.print("a = ");
        double a = input.nextDouble();

        System.out.print("b = ");
        double b = input.nextDouble();

        System.out.print("c = ");
        double c = input.nextDouble();

        double discriminant = b * b - 4 * a * c;

        if (a == 0 || discriminant < 0) {
            System.out.println("Complex Number");
        } else {
            double x1 = (-b + Math.sqrt(discriminant)) / (2 * a);
            double x2 = (-b - Math.sqrt(discriminant)) / (2 * a);

            System.out.printf("x1 = %.6f\n", x1);
            System.out.printf("x2 = %.6f\n", x2);
        }

        input.close();
    }
}



 
