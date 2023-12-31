# assignmentss
public class ErrorHandlingExample {

    public static void main(String[] args) {
        try {
            int result = divide(10, 0);
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) 
            {
            System.err.println("Error: Division by zero is not allowed.");
        } catch (Exception e) 
        {
           System.err.println("An unexpected error occurred: " + e.getMessage());
        } finally {
            System.out.println("This block always executes.");
        }

       System.out.println("Program continues...");
    }
    private static int divide(int numerator, int denominator) {
        return numerator / denominator;
    }
}
