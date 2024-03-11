/*saif eddien wassem hussien abu mustafa
game (3)
id  20230814
date of creating 2/3/2024*/
#include <iostream>
#include <cmath>

using namespace std;

int num_coins = 100;

// Update the number of coins
void update_state(int coins_taken) {
    num_coins -= coins_taken;
}

// Checking if there is a winner
bool is_winner() {
    return num_coins <= 0;
}

int main() {
    // Displaying the game rules
    cout << "To start the game you should enter the number of coins" << endl;
    cout << "The players must take a perfect square number of coins like (1, 4, 9, ...)" << endl;
    cout << "The last player to take coins wins " << endl;
    cout << "Good luck! " << endl;

    while (true) {
        // For player 1
        int subtracted_coins1;
        cout << "Player 1, please enter the number of coins to subtract: ";
        cin >> subtracted_coins1;
        while (subtracted_coins1 != 1 && (subtracted_coins1 <= 0 || subtracted_coins1 >= num_coins || subtracted_coins1 % static_cast<int>(sqrt(subtracted_coins1)) != 0)) {
            cout << "Invalid number, please enter a perfect square number: ";
            cin >> subtracted_coins1;
        }
        update_state(subtracted_coins1);
        if (is_winner() && subtracted_coins1 == 1) {  // Checking if player 1 wins if the subtracted coin is 1
            cout << "Player 1 won!" << endl;
            break;
        } else if (is_winner()) {
            cout << "Player 2 won!" << endl;
            break;
        } else {
            cout << "The remaining coins are: " << num_coins << endl;
        }

        // For player 2
        int subtracted_coins2;
        cout << "Player 2, please enter the number of coins to subtract: ";
        cin >> subtracted_coins2;
        while (subtracted_coins2 != 1 && (subtracted_coins2 <= 0 || subtracted_coins2 >= num_coins || subtracted_coins2 % static_cast<int>(sqrt(subtracted_coins2)) != 0)) {
            cout << "Invalid number, please enter a perfect square number: ";
            cin >> subtracted_coins2;
        }
        update_state(subtracted_coins2);
        if (is_winner() && subtracted_coins2 == 1) {  // Checking if player 2 wins if the subtracted coin is 1
            cout << "Player 2 won!" << endl;
            break;
        } else if (is_winner()) {
            cout << "Player 1 won!" << endl;
            break;
        } else {
            cout << "The remaining coins are: " << num_coins << endl;
        }
    }

    return 0;
}
