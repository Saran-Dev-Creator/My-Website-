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
      color: #333;
      animation: fadeIn 2s ease-in-out;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    img {
      width: 100%;
      max-width: 400px;
    }
  </style>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <img src="https://picsum.photos/300" alt="Random Image">
  <p>This is a sample mobile-friendly site.</p>
  <button onclick="alert('Thanks for clicking!')">Click Me</button><br><br>
  <a href="about.html">Go to About Page</a>
</body>
</html>
