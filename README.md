#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    int secretNumber, guess;

    // Seed the random number generator
    srand(time(0));

    // Generate a random number between 1 and 100
    secretNumber = rand() % 100 + 1;

    cout << "=== Number Guessing Game ===" << endl;
    cout << "I have chosen a number between 1 and 100." << endl;
    cout << "Try to guess it!" << endl;

    do {
        cout << "Enter your guess: ";
        cin >> guess;

        if (guess > secretNumber) {
            cout << "Too High! Try again." << endl;
        } 
        else if (guess < secretNumber) {
            cout << "Too Low! Try again." << endl;
        } 
        else {
            cout << "🎉 Congratulations! You guessed the correct number." << endl;
        }

    } while (guess != secretNumber);

    return 0;
}
