# 🐍 Snake and Ladders Game (x86 Assembly)

A fully interactive **Snake and Ladders** game developed in **x86 Assembly Language** using the **Irvine32 library**, simulating a two-player CLI-based board game with classic snake and ladder mechanics.

---

## 📌 Overview

This project is a nostalgic digital version of the traditional *Snake and Ladders* game, built entirely in **Assembly (MASM syntax)**. It is designed to run on the **Windows console** using the **Irvine32** library for console I/O and random number generation.

Features include:
- Two-player turn-based gameplay
- Dynamic position tracking and updates on a 10x10 grid
- Ladder boosts and snake penalties with visual feedback
- Randomized dice rolling
- Victory condition with automatic game termination and result logging

---

## 🎮 How to Play

- **Player 1** and **Player 2** take turns rolling a virtual dice (press Enter).
- Your position is updated based on the dice roll.
- If you land on a **ladder**, you move to a higher position.
- If you land on a **snake**, you slide down to a lower position.
- First player to reach **position 100** wins.

The game visually displays the board and updates it after each move.

---

## 🧮 Board Structure

The board is represented using a 1D byte array `grid[100]`, with snake and ladder mappings hardcoded as:

### 🔼 Ladders
| From | To  |
|------|-----|
| 3    | 10  |
| 20   | 29  |
| 63   | 81  |
| 80   | 99  |

### 🔽 Snakes
| From | To  |
|------|-----|
| 40   | 22  |
| 50   | 30  |
| 98   | 77  |

---

## 🧠 Concepts Demonstrated

Console I/O with Irvine32.inc

Use of gotoxy, writestring, writechar, and randomrange

ASCII-based grid simulation

Player state tracking using memory (byte array and registers)

Game loop logic and conditional branching

Writing to external files using CreateOutputFile and WriteToFile

---

## Preview📷

|81|82|83|84|85|86|87|88|89|90|
|80|79|78|77|76|75|74|73|72|71|
|61|62|63|64|65|66|67|68|69|70|
|60|59|58|57|56|55|54|53|52|51|
|41|42|43|44|45|46|47|48|49|50|
|40|39|38|37|36|35|34|33|32|31|
|21|22|23|24|25|26|27|28|29|30|
|20|19|18|17|16|15|14|13|12|11|
|1 |2 |3 |4 |5 |6 |7 |8 |9 |10|

Player pieces are represented by ASCII characters (127 = Player 1, 224 = Player 2, 150 = shared tile)

---

📂 Output

The game logs the winner to a file:
Snakes and Ladders.txt

---

🙌 Credits
Developed by [Saad Suleman Brohi]
Assembly implementation using Irvine32 library by Kip Irvine.

