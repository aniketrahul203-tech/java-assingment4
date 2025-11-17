📚 City Library Digital Management System
Java Programming — Assignment 4 (File Handling + Collections)
🌟 Overview

The City Library Digital Management System is a Java-based application built to digitize library operations.
It uses File Handling, Java Collections Framework, Comparable/Comparator, and I/O streams to manage:

✔ Books
✔ Members
✔ Issue/Return Transactions
✔ Persistent Storage through files

This project is developed as part of B.Tech / BCA / BSc Semester 3 — Java Programming Assignment 4.

🏆 Key Functionalities
📘 Book Management

Add new books

Store book info in books.txt

Search by title, author, category

Sort by title (Comparable)

Sort by author/category (Comparator)

👤 Member Management

Add members with unique IDs

Maintain issued book list using List<Integer>

Save member data in members.txt

🔄 Book Transactions

Issue book

Return book

Validate: Book availability, member existence

💾 File Persistence

Load data from files at startup

Save updates after each operation

Uses FileReader, FileWriter, BufferedReader, BufferedWriter

Optional: Binary file handling using FileOutputStream

🧰 Collections Used
Feature	Collection
Store books	Map<Integer, Book>
Store members	Map<Integer, Member>
Issued books list	List<Integer>
Store categories	Set<String>
Waiting list (optional)	Queue<Integer>
🧑‍💻 Tech Stack

Java 8+

Collections Framework

File Handling (Character & Byte Streams)

Comparable & Comparator

Generics

🧱 Project Structure
CityLibrarySystem/
│
├── Book.java
├── Member.java
├── LibraryManager.java
├── books.txt
└── members.txt

🏗 Class Diagram
+----------------------+        +----------------------+
|        Book          |        |       Member         |
+----------------------+        +----------------------+
| bookId: int          |        | memberId: int        |
| title: String        |        | name: String         |
| author: String       |        | email: String        |
| category: String     |        | issuedBooks: List<>  |
| isIssued: boolean    |        +----------------------+
+----------------------+        | + displayDetails()   |
| + displayDetails()   |        | + addIssuedBook()    |
| + markAsIssued()     |        | + returnIssuedBook() |
| + markAsReturned()   |        +----------------------+
+----------------------+

                 +-------------------------+
                 |     LibraryManager      |
                 +-------------------------+
                 | books: Map<Integer,Book>|
                 | members: Map<Integer,Member>|
                 +-------------------------+
                 | + addBook()             |
                 | + addMember()           |
                 | + issueBook()           |
                 | + returnBook()          |
                 | + searchBooks()         |
                 | + sortBooks()           |
                 | + loadFromFile()        |
                 | + saveToFile()          |
                 +-------------------------+

📄 Sample Interaction
Welcome to City Library Digital Management System

1. Add Book
2. Add Member
3. Issue Book
4. Return Book
5. Search Books
6. Sort Books
7. Exit

Enter your choice: 1
Enter Book Title: Java Programming Mastery
Enter Author: John Smith
Enter Category: Programming

Book added successfully with ID: 101

💾 File Handling Implementation
✔ Text-Based Storage

Files used:

books.txt
members.txt

✔ Streams Used

FileReader / FileWriter

BufferedReader / BufferedWriter

FileInputStream / FileOutputStream (Optional)

✔ Ensures

Auto creation of files

Persistent library data

Efficient read/write operations

📌 Learning Outcomes

By completing this project, you will:

✔ CO4.1: Apply Java File Handling for storing real-world data
✔ CO4.2: Use Collections Framework for dynamic data management
✔ CO4.3: Implement Comparable & Comparator for sorting
✔ CO4.4: Integrate I/O operations with collections

🚀 How to Run
1. Compile all Java files
javac *.java

2. Run the program
java LibraryManager

🛠 Future Enhancements

Add GUI using JavaFX/Swing

Add JSON/XML-based file storage

Add admin login system

Add book reservation queue

✨ Author

Rahul Kumar
Semester 3 — Java Programming
City Library Digital Management System (Assignment 4)
