Dicemain

public class Dice {
int low, high;
public Dice (int x , int y){
  low = x;
	high = y;
}
public int computerNumber (){
	int computer;
	computer = low +(int)(Math.random() * high);
	return computer;
	
}
}
import java.util.Scanner;
public class Dicemain{ 
public static void main (String args [])
{
  Scanner input = new Scanner ( System.in);
	Dice Number1 = new Dice(1,6);
	System.out.println( Number1.computerNumber());
	int computerMove;
	
	computerMove = (Number1.computerNumber());
	
	int valueTotal;
	valueTotal = computerMove;
	int computerNumber;
	if (valueTotal <= 3)
	{
		computerNumber = 0;
	}
	else if (valueTotal >= 4)
	{
		computerNumber = 1;
		
		System.out.println( "Select a number between 1 and 6");
		int userMove;
		userMove = input.nextInt();
		if ( userMove == computerNumber)
		{
			System.out.println ("You Win\n" + "dices rolled"+ valueTotal);
			
		}
		else if (userMove != computerNumber && computerNumber == 0)
		{
			System.out.println ("You Lose\n number was low\n" + "dices rolled"+ valueTotal);
		}
		else if (userMove != computerNumber && computerNumber == 1)
		{
			System.out.println ("You Lose\n number was high\n" + "dices rolled"+ valueTotal);
	}
		
	
}
}}

========
