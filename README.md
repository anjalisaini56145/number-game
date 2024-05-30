# number-game
import java.util.*;
import java.util.random.*;
public class num_game {
    public static void main(String[] args) {
		// GENRATING RANDOM NUMBER 
        Random r1 = new Random();
        int r1_int1 = r1.nextInt(100); 
        Scanner sc = new Scanner(System.in);
        System.out.println(" the number of passes are 5");
		// K IS THE NO. OF PASSES 
        int k = 5;
        int i;
        for(i=0;i<k;i++){
            System.out.println(
				"Guess the number:");

			// Take input for guessing
			 int num = sc.nextInt();

			// If the number is guessed
			if (r1_int1 == num) {
				System.out.println(
					"Congratulations!"
					+ " You guessed the number.");
				break;
			}
			else if (r1_int1 > num
					&& i != k - 1) {
				System.out.println(
					"The number is "
					+ "greater than " + num);
			}
			else if (r1_int1 < num
			&& i != k - 1) {
				System.out.println(
					"The number is"
					+ " less than " + num);
			}
		}

		if (i == k) {
			System.out.println(
				"You have exhausted the numner of passes ");

			System.out.println( "The random genrated number was " + r1_int1);
		}
	
    
    }}

