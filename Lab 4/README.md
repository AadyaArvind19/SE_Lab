# Lab 4: Vibe Coding Assignment — Coin Collector Game

## Student Details
- **Name:** Aadya Arvind
- **SRN:** PES2UG24CS008
- **Section:** 5A CSE

## Objective
To use Vibe Coding tools and natural-language prompts to fix a bug in an existing Python game and implement the additional features specified in the assigned repository.

## Assigned Project
**Coin Collector Game**

- **Assigned starter repository:** [SETAPESU26/06_coin_collector](https://github.com/SETAPESU26/06_coin_collector)
- **Technology:** Python and Pygame

## Work Completed

### 1. Fixed the Coin-Collection Bug
- Fixed the bug that allowed the same coin to award points repeatedly while the player remained in contact with it.
- Collected coins are now removed from the active coin list, so each coin can be collected only once.

### 2. Added Multiple Coin Types
- Added **Bronze coins** worth 1 point.
- Added **Silver coins** worth 3 points.
- Added **Gold coins** worth 5 points.
- Assigned distinct colours to the three coin types so they can be visually distinguished.

### 3. Added Obstacles and Lives
- Added obstacles to the play area that the player must avoid.
- Added a starting allowance of **3 lives**.
- Obstacle contact reduces the player's lives. Remaining in contact with the same obstacle does not repeatedly deduct lives every frame; a new penalty can occur after the player leaves and makes contact again.

### 4. Added a Timed Round
- Added a **30-second countdown timer** displayed during gameplay.
- The round ends when the timer reaches zero or the player runs out of lives.
- The game-over screen displays the final score and the reason the round ended.
- Added the **R** key to restart after game over; the score, lives, timer and round state are reset.

## How to Run

Install the required dependency:

```bash
python -m pip install -r requirements.txt
```

Run the game:

```bash
python main.py
```

**Controls:**
- Arrow keys: Move the player.
- R: Restart after game over.

## Deliverables
- **Updated game source code:** `main.py`, `requirements.txt` and the `game/` folder.
- **Before and after gameplay videos:** Demonstrations recorded before and after the changes.
- **Vibe Coding interaction history:** `Lab4_Chat_History.pdf`, containing the AI interaction history.

## Video Demonstrations
- **Before Changes:** [Watch Video](https://drive.google.com/file/d/11fRGmQOSuCUxQYIL425srMps-UHhS_We/view?usp=sharing)
- **After Changes:** [Watch Video](https://drive.google.com/file/d/15i04MFkgBcUArC0mr81Ti28nYw7yr5er/view?usp=sharing)

## Files in This Folder
- `main.py`
- `requirements.txt`
- `game/__init__.py`
- `game/coin.py`
- `game/collection.py`
- `game/game_engine.py`
- `game/player.py`
- `game/renderer.py`
- `Lab4_Chat_History.pdf`
- `CoinCollector_Before_Change.mp4`
- `CoinCollector_After_Change.mp4`

All updated source files and supporting submission evidence are included in this folder.
