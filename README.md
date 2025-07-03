<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Mobile Website</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">

  <!-- AOS Animation CSS -->
  <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">

  <style>
    /* Reset and Font */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #f8f9fa;
      color: #222;
      text-align: center;
      padding: 20px;
      transition: background-color 0.5s ease, color 0.5s ease;
    }

    h1 {
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    img {
      width: 100%;
      max-width: 400px;
      border-radius: 8px;
      margin: 15px 0;
    }

    a {
      color: #0984e3;
      text-decoration: none;
      font-weight: bold;
    }

    a:hover {
      text-decoration: underline;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #00b894;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: 0.3s ease;
      margin-top: 10px;
    }

    button:hover {
      background-color: #019875;
    }

    input, textarea {
      width: 90%;
      padding: 10px;
      margin: 5px 0;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }

    /* Preloader */
    #preloader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #fff;
      z-index: 9999;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .loader {
      border: 8px solid #f3f3f3;
      border-top: 8px solid #00b894;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    /* Dark Mode */
    body.dark-mode {
      background-color: #121212;
      color: #f1f1f1;
    }

    body.dark-mode input,
    body.dark-mode textarea {
      background-color: #333;
      color: #fff;
      border: 1px solid #555;
    }

    body.dark-mode a {
      color: #74b9ff;
    }

    body.dark-mode button {
      background-color: #444;
      color: white;
    }
  </style>
</head>
<body>

  <!-- Preloader -->
  <div id="preloader">
    <div class="loader"></div>
  </div>

  <!-- Dark Mode Toggle -->
  <button onclick="toggleTheme()" id="theme-toggle">🌙 Dark Mode</button>

  <!-- Content -->
  <h1 data-aos="fade-up">Welcome to My Website</h1>
  <p data-aos="zoom-in">This site was built using a mobile phone! 📱</p>

  <img src="https://picsum.photos/400" alt="Sample Image" data-aos="flip-left">

  <a href="about.html" data-aos="fade-up">Go to About Page</a>

  <!-- Contact Form -->
  <h2 data-aos="fade-right">Contact Me</h2>
  <form action="https://formspree.io/f/moqgywnl" method="POST" data-aos="fade-left">
    <input type="text" name="name" placeholder="Your Name" required><br><br>
    <input type="email" name="email" placeholder="Your Email" required><br><br>
    <textarea name="message" placeholder="Your Message" required></textarea><br><br>
    <button type="submit">Send Message</button>
  </form>

  <!-- AOS and Theme Script -->
  <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init();

    // Preloader removal
    window.addEventListener("load", function () {
      document.getElementById("preloader").style.display = "none";

      // Load saved theme
      const savedTheme = localStorage.getItem("theme");
      const body = document.body;
      const button = document.getElementById("theme-toggle");
      if (savedTheme === "dark") {
        body.classList.add("dark-mode");
        button.textContent = "☀️ Light Mode";
      }
    });

    // Toggle dark mode and save
    function toggleTheme() {
      const body = document.body;
      const button = document.getElementById("theme-toggle");
      body.classList.toggle("dark-mode");

      if (body.classList.contains("dark-mode")) {
        localStorage.setItem("theme", "dark");
        button.textContent = "☀️ Light Mode";
      } else {
        localStorage.setItem("theme", "light");
        button.textContent = "🌙 Dark Mode";
      }
    }
  </script>
</body>
</html>



