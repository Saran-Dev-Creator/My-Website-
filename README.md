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
           transition: background-color 0.5s ease, color 0.5s ease;
}
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
   window.onload = () => {
    const savedTheme = localStorage.getItem("theme");
    const body = document.body;
    const button = document.getElementById("theme-toggle");
    if (savedTheme === "dark") {
      body.classList.add("dark-mode");
      button.textContent = "☀️ Light Mode";
    }
  };
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
</body <!-- AOS JS -->
<script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
<script>
  AOS.init();
</script>>
<h1 data-aos="fade-up">Welcome to My Website</h1>

<p data-aos="zoom-in">This paragraph will zoom in on scroll.</p>

<img src="https://picsum.photos/300" data-aos="flip-left" alt="Image">
<h2 data-aos="fade-right">My Projects</h2>
<p data-aos="zoom-in" data-aos-delay="200">Cool stuff I’ve built on mobile!</p>
<div data-aos="fade-up" data-aos-duration="1000" data-aos-delay="300">
  I fade in after 0.3 seconds and take 1 second!
</div>



