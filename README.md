# Guessing-Game
My fisrt version! updates to come and feel free to leave comments and suggestions! Idea for new features as well!

Computer picks a random number between 1 and 50. Your job to guess the chosen number. The computer will respond by stating if the guess is too high or too low or if they have guessed correctly. The program must will track how many guesses the user has taken to guess the correct answer.

@author Valentino Muiruri
  
import java.util.*;
import java.io.*;
public class CollectionOfGames {
public static void main(String[] args)
  {
    int num = 1;
    int count=0;
    
    Scanner myScan = new Scanner(System.in);
    String find;
    String answers;
    while(true)
    {
      int rand = (int)(Math.random()*50+1);
      for (int c = 0; num != rand; c++)
      {
        count++;
        System.out.println("Please enter a number between 1 and 50");
        num = myScan.nextInt();
        if (num >= 51)
        {
          System.out.println ("This number is over the limit. Try again.");
          count=0;
        }
        if (num < rand && num >0)
        {
          System.out.println("the guess is  too low"); 
        }
        else if (num > rand && num < 51)
        {
          System.out.println("the guess is  too high"); 
        }
        if (num == rand)
        {
        } 
        if (num <= 0)
        {
          break;
        } 
      }
      if (num <= 0)
      {
        myScan.nextLine();
        System.out.println ("Invalid option. Do you want to try again? (Y/N) ");
        count=0;
        if (true)
        {
          find= myScan.nextLine();
          if (find.equals ("Y")||find.equals ("y"));
          {
            num=0;
            rand = (int)(Math.random()*50+1);
          }
          if (find.equals ("N")||find.equals ("n"))
          {
            break;
          }
        }
      }
      num= 120;
       if ((count > 6) && (num== 120) )
      {
        myScan.nextLine();
       System.out.println ("You are right!!! But that took "+count+" guesses. Do you want to play again? (Y/N)");
        count=0;
        if (true)
        {
          find= myScan.nextLine();
          if (find.equals ("Y")||find.equals ("y"));
          {
            num=0;
            rand = (int)(Math.random()*50+1);
          }
          if (find.equals ("N")||find.equals ("n"))
          {
            break;
          }
        }
      }

      if (count < 6&& num== 120)
      {
        myScan.nextLine();
        System.out.println("Congratulations! You got that in "+count+" guesses. Do you want to play again? (Y/N)");
        count=0;
        if (true)
        {
          find= myScan.nextLine();
          if (find.equals ("Y")||find.equals ("y"));
          {
            num=0;
            rand = (int)(Math.random()*50+1);
          }
          if (find.equals ("N")||find.equals ("n"))
          {
            break;
          }
        }
      }
    }
  }

}
