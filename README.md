# Two-Pen Crossword

A collaborative crossword for two (or a few) players: one shared board, live cursors and a chat panel.
Everything is in `index.html`. Players connect browser to browser with [PeerJS](https://peerjs.com/), and every message also goes through a public MQTT relay
(EMQX and HiveMQ public brokers over secure WebSocket), so play still works when routers block the direct link.

## Play

Open the page, pick a name and ink colour, then send the invite link in the header to the other player.
The room code is the part after `#` in the address.

## Notes

- The status pill says "Connected" (direct) or "Connected via relay". Hover it for details.
- Relay messages go through public brokers: anyone who knows the room code could read them, so use a fresh room for anything private.
- URL options (before the `#`): `?server=https://your-peerserver/`, `?relay=wss://your-broker/mqtt` or `?relay=off`, `?direct=off`.
- The board and chat are saved in each player's browser and re-sync on reconnect.
- Puzzles: six built in, `.puz` / `.ipuz` import, or build one from your own list of words and clues.
