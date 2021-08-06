# PictoMsg
Draw in your browser and send them to your friends, just like PictoChat on the DS.

Access PictoMsg quickly through https://jasonqiu1.github.io/PictoMsg or by downloading the index.html file and opening it in your browser locally.


# Current Features
- Draw on a canvas and clear it.
- Connect to one friend using their Peer ID.
- Send a connected friend drawings.
- Receive a connected friend's drawings (overwrites previous received drawings).


# Issues
- The PeerJS Cloud server for connecting peers together is unstable sometimes, so at times it may be possible to connect to a peer but not be able to send drawings. If this happens to you, please try again in a few minutes.


# To-Do (ordered from highest priority at the top)
- Change P2P setup to allow for multiple peers to be connected to a room. Implementation thoughts below:
  + Setup dummy peers (rooms) to run indefinitely on a server.
  + Display the rooms on the index page to connect to.
  + Multiple peers can connect to the rooms.
  + Message sending happens by: peer -> room (dummy peer) -> all connected peers excluding the sender.
- Show history of all received and sent messages with timestamps in a scrolling box.
- Setup custom ICE (or PeerJS if it supports multiple peer connections) server for assigning custom usernames. Also solves PeerJS Cloud instability. Implementation thoughts below:
  + Allow users to change default peer id to any alphanumerical text on index page.
  + If username is currently in use, notify the user and have them pick a different name.
  + Entering a room without setting a name generates a random uuid by default.
  + Disconnecting from a room frees the name, allowing it to be used by others.
- Convert canvas drawing to true 1-bit drawing (Currently has anti-aliasing issues).
- Add more drawing tools to the canvas.
  + Different brush sizes.
  + Eraser brush tool.
  + 1-bit dither brushes.
