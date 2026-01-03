// Check draw
bool checkDraw() {
    for (int i = 0; i < 3; i++)
        for (int j = 0; j < 3; j++)
            if (board[i][j] != 'X' && board[i][j] != 'O')
                return false;
    return true;
}
int main() {
    int choice;

    cout << "=== TIC TAC TOE (X - O) ===\n";

    while (true) {
        displayBoard();
        cout << "Player " << currentPlayer << ", choose a position (1-9): ";
        cin >> choice;

        if (choice < 1 || choice > 9 || !makeMove(choice)) {
            cout << "Invalid move! Try again.\n";
            continue;
        }

        if (checkWin()) {
            displayBoard();
            cout << "Player " << currentPlayer << " wins!\n";
            break;
        }

        if (checkDraw()) {
            displayBoard();
            cout << "It's a draw!\n";
            break;
        }

        switchPlayer();
    }

    return 0;
}