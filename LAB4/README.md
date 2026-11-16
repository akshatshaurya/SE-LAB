# Lab 4 – Reaction Time Tester

**Author:** Akshat Shaurya  
**SRN:** PES2UG24CS047  

## Overview
This lab is about building and improving a Reaction Time Tester game in Python (Pygame), with the help of ChatGPT. The player waits for a signal and reacts as fast as possible. The game records each round's reaction time in milliseconds, then shows the average and the number of false starts.
Before and after videos provided in Teams.
## Contents

| File | Description |
| :--- | :--- |
| [PES2UG24CS047_Lab4.pdf](PES2UG24CS047_Lab4.pdf) | Lab 4 submission document |
| [game1.mp4](game1.mp4) | Gameplay recording: original version |
| [improved1.mp4](improved1.mp4) | Gameplay recording: improved version |

## Links
- **Project repository:** [akshatshaurya/43_reaction-time-tester](https://github.com/akshatshaurya/43_reaction-time-tester)
- **ChatGPT conversation:** [Shared chat](https://chatgpt.com/share/6ad26515-fb38-83ee-b7ef-1dd37ad67d09)

## Improved Version Features
- **Difficulty selection:** Easy (3 rounds), Medium (5 rounds), Hard (7 rounds)
- **Per-round results:** reaction time for every round, in milliseconds
- **Session summary:** average reaction time and false-start count
- **Replay and quit:** R / Enter returns to the menu, Q quits, Esc exits from the menu

## Running the Game
```bash
git clone https://github.com/akshatshaurya/43_reaction-time-tester.git
cd 43_reaction-time-tester
pip install -r requirements.txt
python main.py
```
