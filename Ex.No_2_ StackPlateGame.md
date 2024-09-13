# Ex.No: 2 Implementation of Stack Plate game using Queue 
#### DATE : 23.08.2024      
#### NAME : Vishwaraja R
#### REGISTER NUMBER : 212221220060

### AIM: 
To write a python program to simulate the process of stacking plates.
### Algorithm:
1. Initialize the Stack
2. Create an empty list to represent the stack.
3. Push the plate on top of stack
4. Pop the plate from top.
5. Display the plate details.
6. Create an interactive menu and display it.
### Program:
```
class PlateStack:
    def __init__(self):
        self.stack = []

    def is_empty(self):
        return len(self.stack) == 0

    def push(self, plate):
        self.stack.append(plate)
        print(f"Plate '{plate}' added to the stack.")

    def pop(self):
        if self.is_empty():
            print("The stack is empty. No plates to remove.")
        else:
            removed_plate = self.stack.pop()
            print(f"Plate '{removed_plate}' removed from the stack.")

    def view_stack(self):
        if self.is_empty():
            print("The stack is empty.")
        else:
            print("Current stack of plates:")
            for plate in reversed(self.stack):
                print(plate)
```
```
def plate_stack_game():
    plate_stack = PlateStack()
    print("Welcome to the Plate Stack Game!")

    while True:
        print("\nChoose an option:")
        print("1. Add a plate")
        print("2. Remove a plate")
        print("3. View stack")
        print("4. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            plate = input("Enter the name of the plate to add: ")
            plate_stack.push(plate)
        elif choice == '2':
            plate_stack.pop()
        elif choice == '3':
            plate_stack.view_stack()
        elif choice == '4':
            print("Exiting the game. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")
```
```
if __name__ == "__main__":
    plate_stack_game()
```

### Output:
![Screenshot 2024-08-16 111330](https://github.com/user-attachments/assets/8c26cec6-bbeb-453c-8b72-421279f4040c)

![Screenshot 2024-08-16 111351](https://github.com/user-attachments/assets/8152422c-e165-4eef-bf53-8f3fd135f2fa)

![Screenshot 2024-08-16 111342](https://github.com/user-attachments/assets/9c7687e6-e559-4484-8d5b-e2bb756a6a79)

![Screenshot 2024-08-16 111658](https://github.com/user-attachments/assets/a20bfc05-f2e1-4142-ada5-80f9821dc5f4)

### Result:
Thus the simple Stack plate game was implemented using data structure Stack.
