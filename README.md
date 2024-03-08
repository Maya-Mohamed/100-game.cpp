# 100-game.cpp
#include<iostraeam>
//game eeplaniation: Two players start from 0 and alternatively add a number from 1 to 10 to the sum. The player who reaches 100 wins.
int main() {

    //exeplain the game to the user
    std::cout << " game eeplaniation: Two players start from 0 and alternatively add a number from 1 to 10 to the sum The player who reaches 100 wins.";
    int n_coins = 0;
    while (n_coins < 100) {

        // Player 1's turn
        int x;
        std::cout << "Player 1: Enter a number from 1 to 10: ";
        std::cin >> x;
        if (x > 10 || x < 1) {
            std::cout << "Invalid input\n";
            break;
        }
        n_coins += x;
        std::cout << "Total coins: " << n_coins << std::endl;

        if (n_coins == 100) {
            std::cout << "Player 1 wins!\n";
            break;
        }

        // Player 2's turn
        std::cout << "Player 2: Enter a number from 1 to 10: ";
        std::cin >> x;
        if (x > 10 || x < 1) {
            std::cout << "Invalid input\n";
            break;
        }
        n_coins += x;
        std::cout << "Total coins: " << n_coins << std::endl;

        if (n_coins == 100) {
            std::cout << "Player 2 wins!\n";
            break;
        }

        if (n_coins > 100) {
            std::cout << "you lost :( number of coins can't exceed 100\n";
            break;
        }
    }

    return 0;
}
