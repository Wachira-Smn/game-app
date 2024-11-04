# g[09:35, 24/10/2024] +254 700 627730: 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snake Game</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #282c34;
            color: white;
            font-family: 'Arial', sans-serif;
        }

        h1 {
            margin-bottom: 10px;
        }

        canvas {
            background-color: #000;
            border: 1px solid #fff;
        }

        .sco…
[10:05, 24/10/2024] +254 711 693373: #include<iostream>
using namespace std;

void printRow(int leadingSpaces, int stars) {
    // Print leading spaces
    for (int i = 0; i < leadingSpaces; ++i) {
        cout << "  ";
    }
    // Print stars
    for (int i = 0; i < stars; ++i) {
        cout << "* ";
    }
    cout << endl;
}

void printPattern(int row) {
    // Base case to stop recursion
    if (row == 8) {
        return;
    }

    // Define the number of stars and leading spaces for each row
    if (row == 0 || row == 7) {
        printRow(0, 8); // First and last row (8 stars)
    } else if (row == 1 || row == 6) {
        printRow(1, 6); // Second and seventh row (6 stars with 1 leading space)
    } else if (row == 2 || row == 5) {
        printRow(2, 4); // Third and sixth row (4 stars with 2 leading spaces)
    } else if (row == 3 || row == 4) {
        printRow(3, 2); // Fourth and fifth row (2 stars with 3 leading spaces)
    }

    // Recursive call for the next row
    printPattern(row + 1);
}

int main() {
    printPattern(0); // Start the pattern from row 0
    return 0;
}ame-app
