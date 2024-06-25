- 👋 Hi, I’m @8Sandeep8
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
8Sandeep8/8Sandeep8 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<h1>Amma</h1>
import os

# Function to display the menu
def display_menu():
    print("Simple To-Do List")
    print("1. View To-Do List")
    print("2. Add Item to To-Do List")
    print("3. Mark Item as Done")
    print("4. Clear To-Do List")
    print("5. Exit")

# Function to view the to-do list
def view_list():
    if os.path.exists("todo.txt"):
        with open("todo.txt", "r") as f:
            lines = f.readlines()
            if lines:
                for i, line in enumerate(lines):
                    print(f"{i+1}. {line.strip()}")
            else:
                print("To-Do List is empty.")
    else:
        print("To-Do List is empty.")

# Function to add item to the to-do list
def add_item():
    item = input("Enter new item: ")
    with open("todo.txt", "a") as f:
        f.write(item + "\n")
    print("Item added to To-Do List.")

# Function to mark item as done
def mark_done():
    view_list()
    try:
        item_number = int(input("Enter item number to mark as done (0 to cancel): "))
        if item_number != 0:
            with open("todo.txt", "r") as f:
                lines = f.readlines()
            with open("todo.txt", "w") as f:
                for i, line in enumerate(lines):
                    if i != item_number - 1:
                        f.write(line)
            print("Item marked as done.")
    except ValueError:
        print("Invalid input. Please enter a number.")

# Function to clear the to-do list
def clear_list():
    confirm = input("Are you sure you want to clear the To-Do List? (yes/no): ")
    if confirm.lower() == "yes":
        open("todo.txt", "w").close()
        print("To-Do List cleared.")
    else:
        print("Clear operation cancelled.")

# Main function to run the program
def main():
    while True:
        display_menu()
        choice = input("Enter your choice: ")
        
        if choice == "1":
            view_list()
        elif choice == "2":
            add_item()
        elif choice == "3":
            mark_done()
        elif choice == "4":
            clear_list()
        elif choice == "5":
            print("Exiting program. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number from 1 to 5.")

if __name__ == "__main__":
    main()
    import os

# Function to display the menu
def display_menu():
    print("Simple To-Do List")
    print("1. View To-Do List")
    print("2. Add Item to To-Do List")
    print("3. Mark Item as Done")
    print("4. Clear To-Do List")
    print("5. Exit")

# Function to view the to-do list
def view_list():
    if os.path.exists("todo.txt"):
        with open("todo.txt", "r") as f:
            lines = f.readlines()
            if lines:
                for i, line in enumerate(lines):
                    print(f"{i+1}. {line.strip()}")
            else:
                print("To-Do List is empty.")
    else:
        print("To-Do List is empty.")

# Function to add item to the to-do list
def add_item():
    item = input("Enter new item: ")
    with open("todo.txt", "a") as f:
        f.write(item + "\n")
    print("Item added to To-Do List.")

# Function to mark item as done
def mark_done():
    view_list()
    try:
        item_number = int(input("Enter item number to mark as done (0 to cancel): "))
        if item_number != 0:
            with open("todo.txt", "r") as f:
                lines = f.readlines()
            with open("todo.txt", "w") as f:
                for i, line in enumerate(lines):
                    if i != item_number - 1:
                        f.write(line)
            print("Item marked as done.")
    except ValueError:
        print("Invalid input. Please enter a number.")

# Function to clear the to-do list
def clear_list():
    confirm = input("Are you sure you want to clear the To-Do List? (yes/no): ")
    if confirm.lower() == "yes":
        open("todo.txt", "w").close()
        print("To-Do List cleared.")
    else:
        print("Clear operation cancelled.")

# Main function to run the program
def main():
    while True:
        display_menu()
        choice = input("Enter your choice: ")
        
        if choice == "1":
            view_list()
        elif choice == "2":
            add_item()
        elif choice == "3":
            mark_done()
        elif choice == "4":
            clear_list()
        elif choice == "5":
            print("Exiting program. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number from 1 to 5.")

if __name__ == "__main__":
    main()
    
