import java.time.LocalDate;
import java.util.*;
import java.util.Map.Entry;
import java.util.Date;
import hello.Hi;
public class Librarian {
	
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
	      System.out.println("WELCOME TO THE LIBRARY MANAGEMENT SYSTEM");
	      System.out.println("LOGIN PORTALS");
		  List<String> list = new ArrayList<String>();
		  list.add("ADMIN LOGIN");
		  list.add("LIBRARIAN LOGIN");
		  list.add("STUDENT LOGIN");
		  System.out.println(list);
		  System.out.println("ENTER THE LOGIN PORTAL");
		  String log = s.nextLine();
		    if (log.equals("LIBRARIAN LOGIN")) {
			  String username, password;
			  System.out.println("Enter username :");

			  username = s.nextLine();
			  System.out.println("Enter password :");

			  password = s.nextLine();
			  if(username.equals("Muraai") && password.equals("MURAAI")) 
			  {
				  System.out.println("LOGIN SUCEESSFULLY");
				  System.out.println("LIST THE LIBRARIAN FUNCTIONALITY");
				  List<String> list1 = new ArrayList<String>();
				    list1.add("CREATE BOOKS");
				    list1.add("VEIW BOOKS");
				    list1.add("UPDATE BOOKS");
				    list1.add("DELETE BOOKS");
				    System.out.println(list1);
				    
				    String log1 = s.nextLine();
				    List<String> list2 = new ArrayList<String>();

				    if (log1.equals("CREATE BOOKS")) {
					    System.out.println("ENTER THE BOOKID , BOOKNAME , BOOKAUTHOR");
					      int n ;
			           	  System.out.println("ENTER THE NUMBER OF BOOKS TO CREATE");
			           	  n = s.nextInt();
		           		  HashMap<Integer,String> hm=new HashMap<Integer,String>();  
			           	  for(int i=1; i<=n ; i++) 
			           	  {
                              
			           		  System.out.println("ENTER THE BOOKNAME");
			           		  String Bookname = s.next();
			           		  System.out.println("ENTER THE BOOKAUTHOR");
			           		  String Bookauthor = s.next();
			           		  String s4=Bookname+"  "+Bookauthor;
			           	      hm.put(i,s4);
			           	  }
			           	     System.out.println("VEIW BOOK DETAILS");  
			           	    for(Entry<Integer, String> m : hm.entrySet()){    
			           	      System.out.println(m.getKey()+"   "+m.getValue());    
			           	   } 
			           	 System.out.println("UPDATE BOOK DETAILS");
			              System.out.println("ENTER THE BOOK ID TO UPDATE THE BOOK");
			         	  int d = s.nextInt();
			         	  System.out.println("ENTER THE BOOK NAME TO UPDATE");
			         	  String t =  s.next();
			         	  System.out.println("ENTER THE BOOK AUTHOR TO UPDATE");
			         	  String e = s.next();
			         	  
			         	  String s5 = t+"  "+e;
			         	  hm.put(d, s5);
			         	 System.out.println("UPDATED BOOK DETAILS");  
			           	    for(Entry<Integer, String> r : hm.entrySet()){    
			           	      System.out.println(r.getKey()+"   "+r.getValue());    
			           	   } 
                         System.out.println("ENTER THE BOOK ID TO DELETE THE BOOK DETAILS");
                         int h = s.nextInt();
                         hm.remove(h);
                         
                         System.out.println("DELETED BOOK DETAILS");  
			           	    for(Entry<Integer, String> r : hm.entrySet()){    
			           	      System.out.println(r.getKey()+"   "+r.getValue());    
			           	   }
			 				   System.out.println("ENTER THE LOGIN PORTAL");
                            System.out.println(list);
			           	   String login1 = s.next();
			 		        if (login1.equals("STUDENTLOGIN")) {
			 			     String user, pass;
			 			     System.out.println("Enter username :");

			 			      user = s.next();
			 			     System.out.println("Enter password :");

			 			     pass = s.next();
			 			  
			 			  if(user.equals("HAATHI") && pass.equals("hello")) 
			 			  {
			 				  System.out.println("LOGIN SUCEESSFULLY");
			 				    List<String> list4 = new ArrayList<String>();
			 				    list4.add("ISSUE BOOKS");
			 				    list4.add("VIEW ISSUED BOOKS");
			 				    list4.add("RETURN BOOKS");
			 				    System.out.println(list4);  
			 				    System.out.println("DISPLAY THE BOOKS AVAIABLE");
			 				    
			 				    for(Entry<Integer, String> m : hm.entrySet())
			 				    {    
			 		           	      System.out.println(m.getKey()+"   "+m.getValue());
			 				    }
			 				    
			 				    System.out.println("ISSUE BOOKS");
			 				    System.out.println("SELECT THE BOOK ID FROM BOOK DETAILS YOU WANT");
			 				    int p = s.nextInt();
			 				    String k1 = s5+ " "+ user;
			 				    hm.put(p, k1);
			 				   for(Entry<Integer, String> m : hm.entrySet())
			 				    {    
			 		           	      System.out.println(m.getKey()+"   "+m.getValue());
			 				    }
			 				   
			 				   System.out.println("ENTER THE LOGIN PORTAL");
			 				  System.out.println(list);
			 				  String log8 = s.next();
			 				    if (log8.equals("LIBRARIANLOGIN")) {
			 					  String username1, password1;
			 					  System.out.println("Enter username :");

			 					  username1 = s.next();
			 					  System.out.println("Enter password :");

			 					  password1 = s.next();
			 					  if(username1.equals("Muraai") && password1.equals("MURAAI")) 
			 					  {
			 						  System.out.println("LOGIN SUCEESSFULLY");

			 				   System.out.println("VEIW ISSUED BOOK DETIALS");
			 				  LocalDate date  = LocalDate.now().plusDays(15);
			 				  String k3= s5+ " "+ user+ " "+LocalDate.now()+ " "+date;
			 				 hm.put(p, k3);
			 				   for(Entry<Integer, String> m : hm.entrySet())
			 				    {    
			 		           	      System.out.println(m.getKey()+"   "+m.getValue());
			 				    }
			 				String  list7 = hm.put(p, k3);
			 				list7.lastIndexOf(4);
                            System.out.println(list7);
			 				   System.out.println("RETURN BOOK DETAILS");
                                 if(list7.equals (LocalDate.now().plusDays(15))) {
			 				    	  System.out.println("BOOK IS RETURNED");
			 				      }
			 				      else {
			 				    	  System.out.println("BOOK IS NOT RETURNED");
			 				      }
                                 System.out.println("IF YOU WANT LOGOUT");
			 				     String logout = s.next();
			 					if(logout.equals(logout)) {
			 						System.out.println(logout);
			 					}
			 				   
			 					  }
			 				    }
			  }
		 }
	
			 		        
			 		        
			 		        
			 		        
			 		        
	}
		    
	}
			  else {
            	  System.out.println("LOGIN FAILED");
              }
				   
			  }    
    }
	}
	

