# Tic Tac Toe API

This is a WebSocket-based API for a multiplayer Tic Tac Toe game built using [Ktor](https://ktor.io/) in Kotlin. The API allows two players to connect and play the game in real-time. It keeps track of the game state, player turns, and broadcasts the game progress to both players.

## Features

- Real-time multiplayer Tic Tac Toe using WebSockets.
- Players are automatically assigned 'X' or 'O' when they connect.
- The game checks for win conditions after each turn.
- Supports restarting a new round after a game finishes.
- Uses Ktor's WebSocket feature for communication.
- Serialized game state using Kotlinx Serialization.

## Project Structure

- **TicTacToeGame**: Handles the game logic, including tracking the game state and player turns.
- **MakeTurn**: Represents a player's move (x, y coordinates).
- **GameState**: Represents the current state of the game board.
- **socket**: Defines the WebSocket route to manage player connections and gameplay.
- **configureSockets**: Configures the WebSocket server with settings like ping period and timeout.

## Technologies Used

- **Ktor**: For building the server.
- **Kotlinx Serialization**: For JSON serialization.
- **WebSockets**: For real-time communication between players.

## Game Rules

- Two players ('X' and 'O') can connect and take turns making moves.
- The first player to align three of their symbols (horizontally, vertically, or diagonally) wins the game.
- If the board is full and no player has won, the game is considered a draw.
- The game will automatically restart after a brief delay.

## API Endpoints

### `/play`
- **Type:** WebSocket
- **Description:** This endpoint allows players to connect to the game. Once two players have joined, they can start playing by sending their moves.
- **Response:** 
  - The game state is broadcasted to both players after each move.

## How to Play

1. Run the server locally or deploy it to a cloud platform.
2. Connect to the WebSocket `/play` endpoint using a WebSocket client or frontend.
3. Players will automatically be assigned as 'X' or 'O' and can start playing.

## Kotlin Tic-Tac-Toe App

In addition to this API, I have developed a Kotlin-based Tic-Tac-Toe app that uses this WebSocket API for real-time gameplay. You can check out the app repository by [clicking here](https://github.com/tariqjamel/Ktor-TicTacToe-Game).

## Contributing

Contributions are welcome! If you have any suggestions, bug fixes, or feature implementations, please submit a pull request.

