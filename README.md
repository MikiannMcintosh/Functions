# Functions
//Intro
#include <iostream>
#include <cstdlib>
using namespace std;

// Ask for User Guess Function
int askForGuess() {
    int choice;
    cout << "Please enter a guess: " << endl;
    cin >> choice;
    return choice;
}

// Comparison Function
void comparison(int passedChoice, int passedNumber) {
    if (passedChoice < passedNumber) {
        cout << "Tow Low, Try Again!" << endl;
    } else if (passedChoice > passedNumber) {
        cout << "Too High, Try Again!" << endl;
    }
}

// Main Function
int main() {
    // Random Number Variable
    int number;
    // User Guess Variable
    int choice;

    // 1. Generate The Random Number
    number = rand();
    cout << "Note: The random number is " << number << endl;

    // 3. Compare User Entry to Random Number & Display Necessary Output
    do {
        choice = askForGuess(); // Call askForGuess Function

        // Compare Guess to Random Number (Call Comparison Function)
        comparison(choice, number);

    } while (choice != number);

    cout << "That's correct";
    return 0;
}
