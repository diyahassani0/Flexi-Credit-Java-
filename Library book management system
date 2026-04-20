import java.util.*;

class Book {
    String title;
    String author;

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    void display() {
        System.out.println("Title: " + title + ", Author: " + author);
    }
}

public class LibraryManagement {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Book> library = new ArrayList<>();

        int choice;

        do {
            System.out.println("\n--- Library Menu ---");
            System.out.println("1. Add Book");
            System.out.println("2. Remove Book");
            System.out.println("3. Search Book");
            System.out.println("4. Display Books");
            System.out.println("5. Exit");
            System.out.print("Enter choice: ");
            choice = sc.nextInt();
            sc.nextLine(); // consume newline

            switch (choice) {
                case 1:
                    System.out.print("Enter title: ");
                    String title = sc.nextLine();
                    System.out.print("Enter author: ");
                    String author = sc.nextLine();

                    library.add(new Book(title, author));
                    System.out.println("Book added successfully!");
                    break;

                case 2:
                    System.out.print("Enter title to remove: ");
                    String removeTitle = sc.nextLine();
                    boolean removed = false;

                    Iterator<Book> it = library.iterator();
                    while (it.hasNext()) {
                        Book b = it.next();
                        if (b.title.equalsIgnoreCase(removeTitle)) {
                            it.remove();
                            removed = true;
                            System.out.println("Book removed!");
                            break;
                        }
                    }

                    if (!removed)
                        System.out.println("Book not found!");
                    break;

                case 3:
                    System.out.print("Enter title to search: ");
                    String searchTitle = sc.nextLine();
                    boolean found = false;

                    for (Book b : library) {
                        if (b.title.equalsIgnoreCase(searchTitle)) {
                            b.display();
                            found = true;
                        }
                    }

                    if (!found)
                        System.out.println("Book not found!");
                    break;

                case 4:
                    if (library.isEmpty()) {
                        System.out.println("Library is empty!");
                    } else {
                        System.out.println("\nAvailable Books:");
                        for (Book b : library) {
                            b.display();
                        }
                    }
                    break;

                case 5:
                    System.out.println("Exiting...");
                    break;

                default:
                    System.out.println("Invalid choice!");
            }

        } while (choice != 5);

        sc.close();
    }
}
