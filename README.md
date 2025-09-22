# 1st-website
1st website<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Message Link</title>
  <style>
    /* Page background & text */
    body {
      background-color: #1e1e1e; /* dark background */
      color: #ffffff;            /* white text */
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0;
      padding: 20px;
    }

    /* Heading */
    h1 {
      margin: 15px 0 30px 0;
      color: pink; 
      font-size: 28px;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    h2 {
      margin: 20px 0;
      color: #ffcc00; 
    }

    /* Button styling */
    button {
      background-color: #007bff;
      color: #ffffff;
      border: none;
      padding: 15px 30px;
      font-size: 18px;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #0056b3;
    }

    /* Image row */
    .image-row {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .image-row img {
      width: 180px;
      height: 120px;
      border-radius: 8px;
      object-fit: cover;
      box-shadow: 0 2px 6px rgba(0,0,0,0.5);
      transition: transform 0.3s;
      cursor: pointer;
    }

    .image-row img:last-child {
      width: 220px;
      height: 160px;
      margin-top: -20px; /* thoda upar */
    }

    .image-row img:hover {
      transform: scale(1.05);
    }

    /* Fullscreen image (modal) */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      padding-top: 50px;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.9);
    }

    .modal img {
      margin: auto;
      display: block;
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      color: #fff;
      font-size: 35px;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>
<body>

<h1>BACHALER PARTY</h1>
<h2>Welcome to the celebration night!</h2>
<h3 style="color:pink; font-weight:normal; margin-top:-10px;">
  This online party organisation by Sujal kashyap, Rahul, Suryansh Negi
</h3>
  <div class="image-row">
    <img src="image.jpg" alt="image1" onclick="openModal(this)">
    <img src="image2.jpg" alt="image2" onclick="openModal(this)">
    <img src="image3.jpg" alt="image3" onclick="openModal(this)">
  </div>

  <h2>Click the button to see the message</h2>
  <button onclick="showMessage()">Click Me</button>

  <!-- Fullscreen Modal -->
  <div id="myModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImg">
  </div>

  <script>
    function showMessage() {
      alert("YOU ARE ALL INVITE IN GOOGLE MEET 7:30PM.");
    }

    function openModal(img) {
      document.getElementById("myModal").style.display = "block";
      document.getElementById("modalImg").src = img.src;
    }

    function closeModal() {
      document.getElementById("myModal").style.display = "none";
    }
  </script>
</body>
</html>



