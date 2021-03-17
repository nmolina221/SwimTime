# SwimTime
# Calculates the amount of time it will take to swim an inputted yardage with an inputted 100-yard-swim-time.

import java.util.Scanner;
public class findTime {

	public static void main(String[] args) {
		Scanner scnr = new Scanner(System.in);
		
		int yardage;
		int pace;
		double yardsDiv100;
		double timeInSeconds;
		double time;
		int minute;
		double seconds;
		
		System.out.println("Enter swim pace (in seconds per 100 yards): ");
		pace = scnr.nextInt();
		
		System.out.println("Enter yardage you wish to swim: ");
		yardage = scnr.nextInt();
		
		yardsDiv100 = yardage / 100; // converts yardage to number of 100 yard laps
		timeInSeconds = pace * yardsDiv100; // equals total time in seconds
		
		minute = (int) (timeInSeconds / 60); //extracts minutes of total time
		seconds = ((timeInSeconds / 60) - minute) * 60; //extracts seconds of total time
		
		System.out.printf("The time it would take for you to swim " + yardage + " yards is " + minute + " minute(s) and %.1f seconds.\n", seconds);
		

	}

}
