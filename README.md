# Two-Pen Crossword

A collaborative crossword for two (or a few) players: one shared board, live cursors and a chat panel.
Everything is in `index.html`. Players connect browser to browser with [PeerJS](https://peerjs.com/).

## Play

Open the page, pick a name and ink colour, then send the invite link in the header to the other player.
The room code is the part after `#` in the address.

## Notes

- Signalling uses the free public PeerJS server. To use your own PeerServer, add `?server=https://your-host/` before the `#`.
- The board and chat are saved in each player's browser and re-sync on reconnect.
- Puzzles: three built in, `.puz` / `.ipuz` import, or build one from your own list of words and clues.
