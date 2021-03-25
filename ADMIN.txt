import java.util.ArrayList;
import java.util.LinkedHashMap;
import java.util.List;
import java.util.Map;
import java.util.Scanner;

public class Admin {
	public static void main(String[] args) {
	  Scanner s = new Scanner(System.in);
      System.out.println("WELCOME TO THE LIBRARY MANAGEMENT SYSTEM");
      System.out.println("SELECT THE LOGIN");
	  List<String> list = new ArrayList<String>();
	  list.add("ADMIN LOGIN");
	  list.add("LIBRARIAN LOGIN");
	  System.out.println(list);
	  
	  String login1 = s.nextLine();
	  if(login1.equals("ADMIN LOGIN")) {
		  
		  String username,password;
		  System.out.println("ENTER USERNAME");
		  username = s.nextLine();

		  System.out.println("ENTER PASSWORD");
		  password = s.nextLine();

		  if(username.equals("Muraai") && password.equals("MURAAI")) {
			  
			  System.out.println("LOGIN SUCCESSFULLY");
			  System.out.println("LIST THE ADMINSTRATOR FUNCTIONALITY");
			  
			  List<String> list1 = new ArrayList<String>();
              list1.add("CREATE LIBRARIANS");
              list1.add("READ LIBRARIANS");
              list1.add("UPDATE LIBRARIANS");
              list1.add("DELETE LIBRARIANS");
              System.out.println(list1);
              
              System.out.println("ENTER THE CATAGORY NAME OF THE LIBRARIANS");
              String librarian = s.nextLine();
			  List<String>list2 = new ArrayList<String>();
              if(librarian.equals("CREATE LIBRARIANS")) {
            	  System.out.println("ENTER THE NUMBER OF THE LIBRARIANS TO CREATE");
            	  int n ,i;
           	  n = s.nextInt();
           	  System.out.println("ENTER THE NAME OF THE LIBRARIANS");
           	  for(i=1; i<=n ; i++) 
           	  {
           		  list2.add(s.next());
           	  }
           	  System.out.println("VIEW LIBRARIANS");
         	  System.out.println(list2);
                   
              System.out.println("UPDATE LIBRARIANS");
              System.out.println("ENTER THE ARRAY POSITION TO UPDATE THE LIBRARIAN");
         	  int d = s.nextInt();
         	  System.out.println("ENTER THE LIBRARIAN NAME TO UPDATE");
         	  String t =  s.next();
         	  list2.set(d,t);
         	  
              System.out.println(list2);
               
              System.out.println("ENTER THE ARRAY POSITION OF THE LIBRARIAN WANT TO DELETE");
              
               int r = s.nextInt();
               list2.remove(r);
               
              System.out.println(list2);
              
              System.out.println("IF YOU WANT LOGOUT");
              String logout = s.next();
              if(logout.equals(logout)) {
            	  System.out.println("LOGOUT SUCCESSFULLY");
              }
              else {
            	  System.out.println("LOGIN FAILED");
              }
              }	 
		  }
	  }
	        
	}
}

