<!DOCTYPE html>
<html>
<head>
  <title>My Mobile Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body { 
           <h2>Contact Me</h2>
<form action="https://formspree.io/f/moqgywnl" method="POST">
  <input type="text" name="name" placeholder="Your Name" required><br><br>
  <input type="email" name="email" placeholder="Your Email" required><br><br>
  <textarea name="message" placeholder="Your Message" required></textarea><br><br>
  <button type="submit">Send</button>
</form> 
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
  input, textarea {
  width: 90%;
  padding: 10px;
  margin: 5px 0;
  font-size: 16px;
}
button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #007bff;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #0056b3;
}
</head>
<body>
  <h1>Welcome to My Website</h1>
  <img src="https://picsum.photos/300" alt="Random Image">
  <p>This is a sample mobile-friendly site.</p>
  <button onclick="alert('Thanks for clicking!')">Click Me</button><br><br>
</body>
</html>


