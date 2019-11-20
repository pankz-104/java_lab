//class account

package Balance;
import java.util.Scanner;
public class Account {
	int curBalance, amt;
	public Account() {
		curBalance = 500;
	}
	void deposit() {	
		Scanner s = new Scanner(System.in);
		System.out.println("Enter the amount :");
		amt = s.nextInt();
		curBalance += amt;
		System.out.println("Current balance is :" + curBalance);
	}
	void withdraw() {
		Scanner s = new Scanner(System.in);
		System.out.println("Enter the amount :");
		amt = s.nextInt();
		try {
			if ((curBalance - amt) < 500)
				throw new LessBalanceException(amt);
			curBalance -= amt;
			System.out.println("\nBalance left :" + curBalance);
		} catch (LessBalanceException e) {
			System.out.println(e);
		}
	}
	void display_balance() {
		System.out.println("Balance in your a/c :" + curBalance);	
	}
}


//class lessbalanceexception

class LessBalanceException extends Exception {
	int amt;	
	LessBalanceException(int x) {
		System.out.println("Balance is less :" + amt);
	}
}


//class mainaccount


package Balance;
import java.util.Scanner;
public class mainaccount {
	public static void main(String[] args) {
		int ch;
		Scanner s = new Scanner(System.in);
		Account a = new Account();
		while (true) {
			System.out.println("1:Deposit\t2:Withdraw\t3:Balance\t4:Exit\n");
			System.out.println("Enter your choice:");
			ch = s.nextInt();
			switch (ch) {
			case 1:		a.deposit();
				        break;
			case 2:   a.withdraw();
			        	break;
			case 3:  	a.display_balance();
			          break;
			case 4:   return;
			default: 	System.out.println("Invalid choice\n");
				        return;
			}
		}
	}
}
