# Auto
JAVA* Place details of a vehicle into a single dimension array; Add to, delete, modify and view the information stored.
package automobileProject;


//Importing the Scanner class to allow for user input/Importing the ArrayList class to use an array


import java.util.Scanner;
import java.util.Arrays;

public class Automobile {
	
	//Defining the private variables
	private String make;
	private String model;
	private String color;
	private int year;
	private int mileage;
	
	public static void menu() {
			// Creating the menu
			System.out.print("----------------------------------------\n");
			System.out.print("* Choose your selection                *\n");
			System.out.print("*--------------------------------------*\n");
			System.out.print("* 1) Add vehicle information           *\n");
			System.out.print("* 2) Remove vehicle information        *\n");
			System.out.print("* 3) Modify vehicle information        *\n");
			System.out.print("* 4) Display vehicle information       *\n");
			System.out.print("* 5) Exit                              *\n");
			System.out.print("----------------------------------------\n");
				
			// Scanner utility named 'scan' to get user input
			Scanner scan = new Scanner(System.in);
				
			System.out.print("Enter your selection: ");
			System.out.print("\n");
			int userSelection = scan.nextInt();
				
			// Creating the if-else statements to identify the user selection
			if (userSelection == 1) {
					
				System.out.print("Transferring....");
				System.out.print("\n");
				addVehicle();
				
			}
			
			if (userSelection == 2) {
				
				System.out.print("Transferring....");
				System.out.print("\n");
				removeVehicle();
				
			}
			
			if (userSelection == 3) {
				
				System.out.print("Transferring....");
				System.out.print("\n");
				modifyVehicle();
				
			}
			
			if (userSelection == 4) {
				
				System.out.print("Transferring....");
				System.out.print("\n");
				informationVehicle();
				
			}
			
			if (userSelection == 5) {
				
				System.out.print("Goodbye");
				System.out.print("\n");
				System.out.print("...");
				System.exit(0);
				
			}
			
			System.out.print(userSelection);
			System.out.print("\n");
				
		
	}
	
	public static void addVehicle() {
		
		Scanner scan = new Scanner(System.in);
		// Initilizing the Array
		String[] autoList = new String[4];
		
		try {
			
			//Getting the user input and store them within the variables
			System.out.println("Enter the vehicle make: ");
			String make = scan.nextLine();
			System.out.print("\n");
			System.out.print("The vehicle make is: " + make);
			System.out.print("\n");
			autoList[0] = make;
				
			System.out.println("Enter the vehicle model: ");
			String model = scan.nextLine();
			System.out.print("\n");
			System.out.print("The vehicle model is: " + model);
			System.out.print("\n");
			autoList[0] = model;
				
			System.out.println("Enter the vehicle color: ");
			String color = scan.nextLine();
			System.out.print("\n");
			System.out.print("The vehicle color is: " + color);
			System.out.print("\n");
			autoList[0] = color;
				
			System.out.println("Enter the vehicle year: ");
			String year = scan.nextLine();
			System.out.print("\n");
			System.out.print("The vehicle year is: " + year);
			System.out.print("\n");
			autoList[0] = year;
				
			System.out.println("Enter the vehicle mileage: ");
			String mileage = scan.nextLine();
			System.out.print("\n");
			System.out.print("The vehicle mileage is: " + mileage);
			System.out.print("\n");
			autoList[0] = mileage;
			
			System.out.print("Returning to Main Menu");
			System.out.print("\n");
			menu();
			
		}
		
		catch (Exception e) {
			System.out.print("Something went wrong when attempting to add a Vehicle. ");
		}
	
	}
	
	static void removeVehicle() {
			
		Scanner scan = new Scanner(System.in);
		
		try {
			System.out.print("Would you like to remove the vehicle from the array? ");
			System.out.print("\n");
			System.out.print("Enter 'y' for yes, anything else for no: ");
			String removal = scan.nextLine();
			
			if (removal == "y") {
				
				ArrayUtils.remove(autoList, 0);
				ArrayUtils.remove(autoList, 1);
				ArrayUtils.remove(autoList, 2);
				ArrayUtils.remove(autoList, 3);
				ArrayUtils.remove(autoList, 4);
			}
		}
		
		catch (Exception e) {
			System.out.print("Something went wrong when attempting to delete a Vehicle. ");
		}
	
	}
	
	static void modifyVehicle() {
		
		try {
			
			System.out.print("Cannot get it to work, sorry");
			System.out.print("\n");
			menu();
			
		}
		
		catch (Exception e) {
			System.out.print("Something went wrong when attempting to modify a vehicle. ");
		}
	
	}
	
	static void informationVehicle() {
		
		try {
			
			// Attempting to display the current array that holds the stored values
			System.out.print("Here is the current Array: ");
			System.out.print("\n");
			System.out.print(autoList[0] + " " + autoList[1] + " " + autoList[2] + " " + autoList[3] + " " + autoList[4]);
			System.out.print("\n");
			System.out.print("Returning to main menu.....");
			
			menu();
		}
		
		catch (Exception e) {
			System.out.print("Something went wrong trying to display the information. ");
		}
	
	}
	
	public static void main(String[] args) {
		
		menu();

	}

}
