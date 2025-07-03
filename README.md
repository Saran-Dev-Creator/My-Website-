<!DOCTYPE html>
<html>
<head>
  <title>My Mobile Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body { 
           font-family: sans-serif;
           text-align: center;
           padding: 20px;
    }
    h1 {
      color: #44;
      animation: fadeIn 10s ease-in-out;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 4;}
    }
    img {
      width: 500%;
      max-width: 800px;
    }
</style>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <img src="https://picsum.photos/300" alt="Random Image">
  <p>This is a sample mobile-friendly site.</p>
  <button onclick="alert('Thanks for clicking!')">Click Me</button><br><br>
</body>
</html>

<body>
  <button onclick="toggleTheme()" id="theme-toggle">☀️ light Mode</button>
  <p>This site supports light mode!</p>

  <script>
    function toggleTheme() {
      const body = document.body;
      const button = document.getElementById("theme-toggle");

      body.classList.toggle("light-mode");

      if (body.classList.contains("light-mode")) {
        button.textContent = "☀️ Light Mode";
      } else {
        button.textContent = "🌙 Dark Mode";
      }
    }
  </script>
</body>


