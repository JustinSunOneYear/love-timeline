# love-timeline<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Our Love Story</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #fffafc;
      color: #333;
    }
    header {
      text-align: center;
      padding: 2em 1em;
      background: #fbe3e8;
    }
    header h1 {
      font-size: 2.5em;
      margin: 0;
    }
    .timeline {
      max-width: 800px;
      margin: 0 auto;
      padding: 2em 1em;
    }
    .event {
      background: #ffffff;
      margin-bottom: 2em;
      padding: 1.5em;
      border-left: 4px solid #ec7a94;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      border-radius: 5px;
    }
    .event h2 {
      margin-top: 0;
      color: #d94f6d;
    }
    .event time {
      font-size: 0.9em;
      color: #888;
    }
    .event img {
      max-width: 100%;
      border-radius: 8px;
      margin: 1em 0;
    }
    .footer {
      text-align: center;
      padding: 2em;
      font-size: 0.9em;
      color: #999;
    }
    #overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #fffafc;
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
    }
    #overlay input {
      padding: 10px;
      font-size: 16px;
      margin-top: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    #overlay button {
      margin-top: 10px;
      padding: 8px 16px;
      background-color: #ec7a94;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div id="overlay">
    <h2>💌 Enter the passphrase to view our story</h2>
    <input type="password" id="passInput" placeholder="Passphrase" />
    <button onclick="checkPass()">Enter</button>
  </div>

  <header style="display:none;">
    <h1>Our Love Story</h1>
    <p>One year of memories together</p>
  </header>

  <main class="timeline" style="display:none;">
    <div class="event">
      <h2>First Day We Met</h2>
      <time>June 1, 2024</time>
      <img src="https://via.placeholder.com/700x400?text=First+Photo" alt="First moment">
      <p>It all began with a smile. I still remember how nervous I was...</p>
    </div>
  </main>

  <div class="footer" style="display:none;">
    <p>Made with love 💗</p>
  </div>

  <script>
    const correctPass = "apricot"; // Change this to your chosen passphrase

    function checkPass() {
      const input = document.getElementById("passInput").value;
      if (input === correctPass) {
        document.getElementById("overlay").style.display = "none";
        document.querySelector("header").style.display = "block";
        document.querySelector("main").style.display = "block";
        document.querySelector(".footer").style.display = "block";
      } else {
        alert("Incorrect passphrase. Try again.");
      }
    }
  </script>
</body>
</html>
