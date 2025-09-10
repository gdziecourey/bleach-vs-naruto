import os

# Path to save the index.html again after reset
file_path = "/mnt/data/index.html"

index_html_content = """<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Bleach vs Naruto</title>
    <script src="https://unpkg.com/@ruffle-rs/ruffle"></script>
  </head>
  <body style="background:#000; margin:0; text-align:center; color:white;">
    <h1>Bleach vs Naruto</h1>
    <div id="player"></div>

    <script>
      const ruffle = window.RufflePlayer.newest();
      const player = ruffle.createPlayer();
      document.getElementById("player").appendChild(player);
      player.style.width = "960px";
      player.style.height = "720px";
      player.load("game.swf"); // make sure your SWF is named game.swf
    </script>
  </body>
</html>"""

# Write the file
with open(file_path, "w") as f:
    f.write(index_html_content)

file_path
