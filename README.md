# 🎮 Networked Tic-Tac-Toe Game (Python + Sockets + Pygame)

This is a simple multiplayer **Tic-Tac-Toe** game built in **Python** using `socket` programming for real-time two-player communication and **Pygame** for the graphical interface.

Two players can play the game on separate machines connected over the same network by running the `server.py` (host) and `player.py` (client) files.

---

## ✨ Features

- Two-player mode over a local network (TCP/IP)
- Real-time multiplayer with server-client architecture
- Intuitive UI with **Pygame**
- Turn-based input with move validation
- Win/draw detection and result display
- Game matrix updates in real-time

---

## 🧰 Technologies Used

- Python 3
- `socket` — for server-client communication
- `threading` — to handle real-time gameplay
- `pygame` — for the UI and game board
- `pickle` (in server) — optional for object serialization (currently unused)

---
2. Start the Server
Run this on the host machine:

bash
Copy
Edit
python server.py
The server waits for two players to connect.

3. Start the Players
On two different terminals/machines (connected to the same network):

bash
Copy
Edit
python player.py
You'll be prompted to enter the host IP address. Use the host machine's IP address (e.g. 192.168.1.10).

Each client will be assigned as Player 1 (X) or Player 2 (O).

🖼️ Game UI
Game board: 3x3 grid

X for Player 1 (Red), O for Player 2 (Blue)

Live display of current turn and game status

Displays game result (Win/Draw) at the bottom

🔄 Turn-Based Logic
Server controls the game state and matrix

Each player clicks to send move coordinates

Invalid inputs are handled with basic validation

📌 Notes
Make sure to include tictactoe.png in the same directory as player.py for the icon to load correctly.

This game works best on local networks. For online play, you'd need to expose ports via port forwarding or use a VPN.

