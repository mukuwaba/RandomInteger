import java.security.SecureRandom;//imported the secure random calls which makes random numbers

public class RandomInteger {
    public static void main(String[] args) {

        //int numberOfFaces = 1_000; //can promt the user to input number then have it equal the intNum

        SecureRandom randomNumbers = new SecureRandom();
        //creates a new object
        //shawn weed
        //mordenstates.org -- CELP

        //Loop through 20 rolls of the die
        for(int counter =1; counter <= 20; counter++){
            //20 is the number of numbers that it will output per roll
            //Get a random number between (inclusive) 1,6
            int face = 1 + randomNumbers.nextInt(6);
            //bound feature controls how many sides of the dice there are so only 1-6 is possible
            //will generate a number between one and 6 each time it loops

            //Report the number on the face
            System.out.printf("%d", face);

            //After rolling the die 5 time...
            if(counter %5 == 0){//dividing by 5 with no remainder = 5 rolls
                //each counter is a roll
                //(counter %5 == 0) is the number of times that the dice is rolls
                //The == # is details that you are looking for numbers with a remainder of 0
                System.out.println();
            }//if
        }//for
    }//main
}//RandomInteger
