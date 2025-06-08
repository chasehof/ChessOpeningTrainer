# ♟️ Chess Opening Trainer (C++ CLI App)

## 🔧 What It Does
A command-line app to help you browse and study chess openings from a small database.

- **Select your color** (White/Black) and follow a line (e.g., `1.e4 e5 2.Nf3 Nc6 3.Bb5`)
- **Shows if you made the right move** or not (like flashcards)
- **Tracks your progress** (accuracy, success rate per opening)

---

## ✨ Features (Start Simple → Grow)

| Feature            | Description                                                      |
|--------------------|------------------------------------------------------------------|
| Opening database   | Store ECO codes, names, and move lines in a file (JSON or CSV)   |
| Study mode         | Pick an opening, and go through the expected moves               |
| Input parser       | You type moves (e.g., `e4`, `Nf3`) and it checks correctness     |
| Statistics         | Track how well you're doing per opening (save to file)           |
| Flashcard mode     | Randomly present positions to test you                           |
| Future: PGN parser | Allow importing real games to compare openings used              |

---

## 🧱 Basic Architecture

```
/chess-trainer
├── src/
│   ├── main.cpp
│   ├── Opening.cpp / .h
│   ├── OpeningTrainer.cpp / .h
│   └── StatsManager.cpp / .h
├── data/
│   └── openings.json
├── include/
│   └── all headers
├── CMakeLists.txt
└── README.md
```

---

## 📝 Sample Opening JSON

```json
[
  {
    "eco": "C60",
    "name": "Ruy Lopez",
    "moves": ["e4", "e5", "Nf3", "Nc6", "Bb5"]
  },
  {
    "eco": "B01",
    "name": "Scandinavian Defense",
    "moves": ["e4", "d5"]
  }
]
```

---

## ✅ Goals

CLI app that:

- Loads opening lines from a JSON file
- Asks user to play through the moves
- Checks input against correct move
- Reports result
- (Optional for later) Saves progress to file
