This program is a **console-based Library Management System** written in Java. It allows users to:

1. Add new books
2. Display all books
3. Borrow a book
4. Return a book
5. Exit the program

All data is stored **in memory** using an `ArrayList`.

---

## 🧱 **Structure of the Code**

### ✅ `Book` Class

```java
class Book {
    String title;
    String author;
    boolean isAvailable;
```

* **Represents a book** in the library.
* Each book has:

  * `title` – the name of the book.
  * `author` – the author's name.
  * `isAvailable` – tells whether the book is available or already borrowed.
* `toString()` is used to print a readable summary of a book.

---

### ✅ `LibraryManagementSystem` Class

This is the **main class** where the program runs.

```java
static ArrayList<Book> books = new ArrayList<>();
static Scanner scanner = new Scanner(System.in);
```

* `books`: stores all the books in a dynamic list.
* `scanner`: helps in getting user input from the keyboard.

---

## 🌀 **How the Program Works**

### 🔁 `main()` Method – Shows Menu

This is the main loop of the program:

```java
while (running) {
    // Show menu
    // Get user choice
    // Call the respective function
}
```

The user sees a menu like this:

```
1. Add Book
2. Display All Books
3. Borrow Book
4. Return Book
5. Exit
```

The program keeps running until the user selects option 5 (Exit).

---

## 🔧 **Functions Explained**

### 1️⃣ `addBook()`

* Asks user for book title and author
* Creates a new `Book` object
* Adds it to the `books` list

```java
books.add(new Book(title, author));
```

---

### 2️⃣ `displayBooks()`

* Prints all books in the list
* Shows whether each book is **Available** or **Borrowed**

Example:

```
1. Harry Potter by J.K. Rowling [Available]
2. Rich Dad Poor Dad by Robert Kiyosaki [Borrowed]
```

---

### 3️⃣ `borrowBook()`

* Shows the book list
* User selects a book number to borrow
* If available, marks the book as borrowed (`isAvailable = false`)
* Else, shows a warning

---

### 4️⃣ `returnBook()`

* Shows the book list
* User selects the book number to return
* If the book was borrowed, marks it available again (`isAvailable = true`)
* Else, shows a message

---

### 5️⃣ Exit

* Ends the program with a goodbye message.

---

## 🧠 Summary Diagram:

```
User ---> Menu ---> [Add | Display | Borrow | Return | Exit]
           |
        ArrayList<Book> (Memory)
           |
        Books (title, author, isAvailable)
'''
