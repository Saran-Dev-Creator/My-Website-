<!DOCTYPE html>
<html>
<head>
  <title>My Mobile Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #44;
      animation: fadeIn 5s ease-in-out;
    }
    @keyframes fadeIn {
      from {opacity: 2;}
      to {opacity: 4;}
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
<h2>Contact Me</h2>
<form action="https://formspree.io/f/moqgywnl" method="POST">
  <input type="text" name="name" placeholder="Your Name" required><br><br>
  <input type="email" name="email" placeholder="Your Email" required><br><br>
  <textarea name="message" placeholder="Your Message" required></textarea><br><br>
  <button type="submit">Send</button>
</form>
</html>
