# ♟️ Chess Engine

A powerful and interactive Python-based Chess Engine featuring:
- Player vs Player mode
- Player vs Computer mode
- AI-powered move generation (Random, Greedy, Minimax, Alpha-Beta Pruning)

---

## 📖 About the Game

Chess is a two-player strategy board game played on an 8×8 grid. Each player starts with 16 pieces:
- 1 King
- 1 Queen
- 2 Rooks
- 2 Knights
- 2 Bishops
- 8 Pawns

The goal: **Checkmate the opponent’s king while defending your own.**

---

## 🚀 Getting Started

### 📦 Prerequisites
- Python 3.6 or higher

### 🛠️ Installation

1. **Download** the repository as `.zip` and extract it  
2. Open terminal in the extracted folder  
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the game:
   ```bash
   python game.py
   ```

---

## 🎮 Game Modes

- 👥 **Player vs Player**: Play locally with a friend  
- 🤖 **Player vs Computer**: Choose your color and let the AI make moves

---

## 🧠 AI Move Generators

| Mode              | Description |
|-------------------|-------------|
| 🔀 **Random**      | Picks a random valid move |
| 🤑 **Greedy**      | Captures the highest-value piece (if possible) |
| 🧮 **Minimax**      | Explores future moves recursively to pick best outcome |
| ✂️ **Alpha-Beta**  | Optimized Minimax that skips unhelpful branches |

---

## ♜ Engine Mechanics

### ✅ Valid Move Generation
- Shows all possible legal moves for selected piece  
- Prevents illegal moves that leave the king in check  
- Ends the game if no legal moves remain (Checkmate or Stalemate)

### ⚠️ Check Detection
- Simulates all enemy moves  
- Checks if the king is in attack range  

---

## 🌳 Minimax & Alpha-Beta Pruning

### 🔁 Minimax Tree
- Generates all future board states up to a certain depth  
- Evaluates scores assuming both players play optimally  

### ✂️ Alpha-Beta Pruning
- Skips irrelevant branches in the tree  
- Greatly improves speed and efficiency  

#### 👇 Observed Improvements:
| Depth | Without Pruning | With Pruning |
|-------|------------------|---------------|
| 2     | ~4,000 nodes     | ~500 nodes    |
| 3     | ~25,000 nodes    | ~5,000 nodes  |

---

## 📊 Evaluation Function

Each board state is scored using:

- **Piece Values**: Pawn (1), Knight/Bishop (3), Rook (5), Queen (9)  
- **Positioning**: Bonus for strong squares (via piece-square tables)  
- **Mobility**: More available moves = higher score  
- **Synergy**: Defensive/attacking formations add strength  

You can fine-tune these values to create smarter AI.

---

## 📁 Project Structure

```
chess-engine/
├── assets/                 # Images (for README and GUI)
├── engine/                 # Core game and AI logic
├── game.py                 # Main game script
├── requirements.txt        # Python dependencies
└── README.md               # You're here!
```

---

## 🖼️ Screenshots

![{1E40F138-99F1-49CA-9947-A1E264FEA35D}](https://github.com/user-attachments/assets/e148f755-8f85-4eb4-b414-bb8cad7f4cea)


---

## 🤝 Contributions

Pull requests and improvements are welcome!  
You can help with:
- Better evaluation functions  
- UI enhancements  
- Bug fixes  

---

## 📬 Contact

Made with ❤️ by **Rajiv Yadav**  


---

## ✅ License

This project is open-source and available under the [MIT License](LICENSE).
