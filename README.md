#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed the random number generator
    srand(time(0));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    int guess;
    int attempts = 0;

    std::cout << "Welcome to the Number Guessing Game!\n";
    std::cout << "I'm thinking of a number between 1 and 100.\n";

    while (true) {
        // Get the user's guess
        std::cout << "Enter your guess: ";
        std::cin >> guess;
        attempts++;

        // Check if the guess is correct
        if (guess == secretNumber) {
            std::cout << "Congratulations! You found the number in " << attempts << " attempts.\n";
            break;
        } else if (guess < secretNumber) {
            std::cout << "Too Low! Try again.\n";
        } else {
            std::cout << "Too High! Try again.\n";
        }
    }

    return 0;
}
