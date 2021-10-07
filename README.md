# PictoMsg
Draw in your browser and send them to your friends, just like PictoChat on the DS.

Access PictoMsg quickly through https://jasonqiu1.github.io/PictoMsg or by downloading the index.html file and opening it in your browser locally.


# Current Features
- Connect to multiple friends using their Peer IDs!
- Draw not only messages, but also your own nickname!
- Send and receive all connected friends drawings!

# To-Do (ordered from highest priority at the top)
- Beef up the UI to more closely mimic PictoChat
- Figure out how to set up dummy peers as rooms like in PictoChat.
- Setup custom ICE (or PeerJS if it supports multiple peer connections) server for assigning custom usernames. Implementation thoughts below:
  + Allow users to change default peer id to any alphanumerical text on index page.
  + If username is currently in use, notify the user and have them pick a different name.
  + Entering a room without setting a name generates a random uuid by default.
  + Disconnecting from a room frees the name, allowing it to be used by others.
- Convert client-side canvas drawing to true 1-bit drawing (Currently has anti-aliasing issues).
- Add more drawing tools to the canvas.
  + Different brush sizes.
  + Eraser brush tool.
  + 1-bit dither brushes.
