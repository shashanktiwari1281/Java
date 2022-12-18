import java.util.Objects;
import java.util.Scanner;

public class MyLibrary {
    static String[] availableBooks={"Geeta","Ramayana","Gitanjali","Constition","Godan","Madhusala","Nirmala","Rashmirathi","Pinjar","Tamas"};
    static String[] issuedBooks=new String[availableBooks.length];
    public static void main(String[] args) {
        for(;;) {
            int choice = userInput();
            if(choice==0) {

            } else if (choice>4||choice<0) {

            }
            switch (choice) {
                case 0->{System.out.println("Library Closed!");System.exit(0);}
                case 1-> printAvailableBook();
                case 2-> issueBook();
                case 3-> returnBook();
                case 4-> printIssuedBook();
                default -> System.out.println("Invalid Input!");
            }
        }
    }
    static int userInput(){
        Scanner scan=new Scanner(System.in);
        System.out.println("\n1.To See Available books\n2.To Issue a book\n3.To Submit a book");
        System.out.print("4.To See Issued books\n0. to Close Library\nEnter your choice ");
        return scan.nextInt();
    }
    static void printAvailableBook(){
        int j=1;
        for (String availableBook : availableBooks) {
            if (availableBook != null)
                System.out.println((j++) + ". " + availableBook);
        }
    }
    static void issueBook(){
        Scanner scan=new Scanner(System.in);
        System.out.print("Enter the book name which to be issue ");
        String bookName=scan.next();
        int i=0;
        while (!Objects.equals(bookName, availableBooks[i])){
            i++;
            if(i==availableBooks.length){
                System.out.println("\n"+bookName+" is not available in the library");
                return;
            }
        }
        System.out.println("Book Issued");
        int j=0;
        while (!Objects.equals(null, issuedBooks[j])){
            j++;
        }
        issuedBooks[j]=availableBooks[i];
        availableBooks[i]=null;
    }
    static void returnBook(){
        Scanner scan=new Scanner(System.in);
        System.out.print("Enter the book name which to be submit ");
        String bookName=scan.next();
        for(int j=0;j<issuedBooks.length;j++) {
            if(Objects.equals(issuedBooks[j], bookName)){
                int i = 0;
                while (availableBooks[i] != null) {
                    i++;
                }
                availableBooks[i] = bookName;
                issuedBooks[j]=null;
                System.out.println("\nBook Submited.");
                return;
            }
        }
        System.out.println("\nThis book has not issued from this library.");
    }
    static void printIssuedBook(){
        int n=1;
        for (String issuedBook : issuedBooks) {
            if (issuedBook != null) {
                System.out.println((n++)+"."+ issuedBook);
            }
        }
        if(n==1)
            System.out.println("No any book issued yet!");
    }
}
