# One-question-
For me 
<!DOCTYPE html>
<html>
<head>
  <title>Just One Question 😌</title>
  <style>
    body {
      background: #020617;
      color: #f8fafc;
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 120px;
    }
    h1 {
      font-size: 28px;
      margin-bottom: 30px;
    }
    button {
      padding: 15px 35px;
      font-size: 18px;
      margin: 15px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
    }
    .yes {
      background: #22c55e;
      color: #020617;
    }
    .no {
      background: #ef4444;
      color: #020617;
    }
    #kiss {
      font-size: 40px;
      margin-top: 20px;
      display: none;
    }
    #boxContainer {
      display: none;
      margin-top: 40px;
    }
    #box {
      font-size: 70px;
      cursor: pointer;
      animation: shake 0.6s infinite;
    }
    @keyframes shake {
      0% { transform: rotate(0deg); }
      25% { transform: rotate(5deg); }
      50% { transform: rotate(0deg); }
      75% { transform: rotate(-5deg); }
      100% { transform: rotate(0deg); }
    }
    #boxText {
      margin-top: 10px;
      font-size: 18px;
      color: #fbcfe8;
    }
    #finalMessage {
      display: none;
      margin-top: 30px;
      font-size: 24px;
      color: #fbcfe8;
    }
  </style>
</head>
<body>
  <!-- Question -->
  <div id="main">
    <h1 id="question">Do you lyk me..! </h1>
    <button class="yes" onclick="yesClick()">YES</button>
    <button class="no" onclick="noClick()">NO</button>
  </div>
  <!-- Small kiss -->
  <div id="kiss">😘</div>
  <!-- Surprise box -->
  <div id="boxContainer">
    <div id="box" onclick="openBox()">🎁</div>
    <div id="boxText">Open if you lyk me </div>
  </div>
  <!-- Final message -->
  <div id="finalMessage">
    😁<br><br>
    If you lyk me…<br>
    Lyk me next year too! ❤️
  </div>
  <script>
    function noClick() {
      document.getElementById("question").innerHTML =
        "Seriyaa yosichu paaru 😄<br>Do you lyk me..!";
    }
    function yesClick() {
      // Hide question & buttons
      document.getElementById("main").style.display = "none";
      // Show small kiss emoji
      document.getElementById("kiss").style.display = "block";
      // Show surprise box
      setTimeout(() => {
        document.getElementById("boxContainer").style.display = "block";
      }, 500);
    }
    function openBox() {
      document.getElementById("box").innerHTML = "😁";
      document.getElementById("box").style.animation = "none";
      document.getElementById("boxText").style.display = "none";
      document.getElementById("finalMessage").style.display = "block";
    }
  </script>
</body>
</html>
