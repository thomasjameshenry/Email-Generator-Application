package EmailApplication;

import java.util.*;

public class EmailApplication {

	public static void main(String args[]) {
		EmailAccount obj = new EmailAccount();
		obj.showMenu();
		
	}
}
class EmailAccount{
	String fname;
	String lname;
	String department;
	String company;
	String emailAddress;
	String password;
	int mailboxCapacity = 100;
	
	EmailAccount(){
		fname = "";
		lname = "";
		department = "";
		company = "";
	}
	
	EmailAccount(String firstname, String lastname, String dep, String comp){
		fname = firstname;
		lname = lastname;
		department = dep;
		company = comp;
	}
	
	void setFname(String firstname) {
		fname = firstname;
	}
	void setLname(String lastname) {
		lname = lastname;
	}
	void setDepartment(String dep) {
		department = dep;
	}
	void setCompany(String comp) {
		company = comp;
	}
	String getName() {
		return fname + " " + lname;
	}
	
	boolean knownUser(){
		if(fname.length()<=0 || lname.length()<=0 || department.length()<=0 || company.length()<=0) {
			return false;
		}
		return true;
	}
	
	String getEmail() {
		emailAddress = fname + "." + lname + "@" + department + "." + company + ".com";
		return emailAddress;
	}
	
	int getMailboxCapacity() {
		return mailboxCapacity;
	}
	
	String generatePassword() {
		Random rand = new Random();
		String alpha = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz123456789";
		String password = "";
		int n = rand.nextInt(20);
		n += 5;
		
		for(int i =0; i<n; i++) {
			password += alpha.charAt(rand.nextInt(alpha.length()));
		}
		
		return password; 
	}
	
	void setPassword(String value) {
		password = value;
	}
	
	void setMailboxCapacity(int value) {
		mailboxCapacity = value;
	}
	
	void setEmail(String value) {
		emailAddress = value;
	}
	void buffer() {
		System.out.println("*");
		System.out.println("*");
		System.out.println("*");
	}
	
	void showMenu() {
		Scanner scan = new Scanner(System.in);
		System.out.println("Welcome");
		if(!knownUser()) {
			System.out.println("Please Enter First Name");
			setFname(scan.nextLine());
			System.out.println("Please Enter Last Name");
			setLname(scan.nextLine());
			System.out.println("Please Enter Department");
			setDepartment(scan.nextLine());
			System.out.println("Please Enter Company");
			setCompany(scan.nextLine());
		}
		System.out.println("==================================================");
		System.out.println("Welcome " + getName());
		System.out.println("\n");
		
		char options = '\0';
		
		System.out.println("A. Generate Email Address");
		System.out.println("B. Generate Password");
		System.out.println("C. Change Email Address");
		System.out.println("D. Change Password");
		System.out.println("E. Set Mailbox Capacity");
		System.out.println("F. Show Details");
		System.out.println("G. Exit");
		
		do
		{
			System.out.println("==================================================");
			System.out.println("Please Enter Option");
			options = scan.next().charAt(0);
			System.out.println("\n");
			
			switch(options)
			{
			case 'A':
				System.out.println("==================================================");
				System.out.println("Generating Email Address");
				System.out.println("==================================================");
				buffer();
				System.out.println("New Email Address: " + getEmail());
				System.out.println("\n");
				break;
				
			case 'B':
				System.out.println("==================================================");
				System.out.println("Generating Password");
				System.out.println("==================================================");
				buffer();
				System.out.println("New Password: " + generatePassword());
				System.out.println("\n");
				break;
				
			case 'C':
				System.out.println("==================================================");
				System.out.println("Change Email Address");
				System.out.println("==================================================");
				setEmail(scan.next());
				buffer();
				System.out.println("New Email Address: " + getEmail());
				System.out.println("\n");
				break;
				
			case 'D':
				System.out.println("==================================================");
				System.out.println("Change Password");
				System.out.println("==================================================");
				setPassword(scan.next());
				buffer();
				System.out.println("New Password Set");
				System.out.println("\n");
				break;
				
			case 'E':
				System.out.println("==================================================");
				System.out.println("Set Mailbox Capacity");
				System.out.println("==================================================");
				setMailboxCapacity(scan.nextInt());
				buffer();
				System.out.println("New Mailbox Capacity: " + getMailboxCapacity());
				System.out.println("\n");
				break;
				
			case 'F':
				System.out.println("==================================================");
				System.out.println("Show Details");
				System.out.println("==================================================");
				buffer();
				System.out.println("Name: " + getName() + "\nEmail Address: " + getEmail() + "\nMailbox Capacity: " + getMailboxCapacity());
				System.out.println("\n");
				break;
				
			case 'G':
				System.out.println("*************************************************");
				break;
				
			default:
				System.out.println("Incorrect Operation. Please Try Again!!!!");
			}
		} while(options != 'G');
		System.out.println("Thank you for using this email service!!!");
	}
}
