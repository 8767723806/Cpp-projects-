# Cpp-projects-
#include <iostream>
using namespace std;

// Function to perform addition
double add(double a, double b) {
    return a + b;
}

// Function to perform subtraction
double subtract(double a, double b) {
    return a - b;
}

// Function to perform multiplication
double multiply(double a, double b) {
    return a * b;
}

// Function to perform division
double divide(double a, double b) {
    if (b == 0) {
        cout << "Error! Division by zero." << endl;
        return 0;
    }
    return a / b;
}

int main() {
    double num1, num2;
    char operation;
    int choice;

    do {
        // Display menu options
        cout << "Simple Calculator\n";
        cout << "1. Add (+)\n";
        cout << "2. Subtract (-)\n";
        cout << "3. Multiply (*)\n";
        cout << "4. Divide (/)\n";
        cout << "5. Exit\n";

        // Prompt user for the operation choice
        cout << "Enter your choice (1-5): ";
        cin >> choice;

        // If the user wants to exit, break the loop
        if (choice == 5) {
            cout << "Exiting the calculator. Goodbye!" << endl;
            break;
        }

        // Get the numbers for calculation
        cout << "Enter first number: ";
        cin >> num1;
        cout << "Enter second number: ";
        cin >> num2;

        // Perform the selected operation
        switch (choice) {
            case 1:
                cout << "Result: " << add(num1, num2) << endl;
                break;
            case 2:
                cout << "Result: " << subtract(num1, num2) << endl;
                break;
            case 3:
                cout << "Result: " << multiply(num1, num2) << endl;
                break;
            case 4:
                cout << "Result: " << divide(num1, num2) << endl;
                break;
            default:
                cout << "Invalid choice! Please try again." << endl;
        }

    } while (true);

    return 0;
}
