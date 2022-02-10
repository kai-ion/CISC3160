
import java.util.*;

class Main {
    

    /**helper function to computer arr */
    static void compute(double[] arr) {

        int len = arr.length;
        
        //computer arr in reverse order

        for (int i = len - 1; i >= 0; i--) {

            double ans = Math.sqrt(Math.abs(arr[i])) + 5 * arr[i];
            if (ans > 500) {
                System.out.println("ans: " + ans + " is greater than 500");
            }  else {
                System.out.println("ans is: " + ans );
            }
        }
        
    }


    public static void main(String[] args) {

        int len = 11;

        System.out.println("Enter " + len + " numbers");

        Scanner myObj = new Scanner(System.in);  // Create a Scanner object

        double[] nums = new double[len];

        for (int i = 0; i < len; i++) {
            System.out.print("Enter num: ");
    
            double num = myObj.nextDouble();  // Read user input

            nums[i] = num;  //store input
        }
        
        System.out.println("\nNums = " + Arrays.toString(nums) + "\n");  // Output All user input

        Main.compute(nums); //helper function

        myObj.close();
    }
}
