<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="stylesheet" href="login.css" />
  <style>
    body {
      background-color: white;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    #img2 {
      width: 420px;
      height: auto;
      display: block;
    }
    #head {
      height: 50px;
      width: 100%;
      color: white;
      border-bottom: 1px dotted white;
      padding: 10px 0;
      box-sizing: border-box;
      margin-bottom: 20px;
    }
    #login {
      width: 420px;
      height: 270px;
      margin: 0 auto 40px;
      background-color: white;
      margin-top: -10px;
      padding: 20px;
      box-sizing: border-box;
      color: black;
    }
    input {
      border-radius: 5px;
      border: 1px solid black;
      width: 100%;
      height: 50px;
      margin-bottom: 20px;
      padding: 10px;
      box-sizing: border-box;
      font-size: 16px;
      opacity: 1;
    }
    ::placeholder {
      color: rgba(168, 188, 201);
      opacity: 1;
    }
    button {
      background-color: rgba(30, 99, 162);
      border: none;
      padding: 10px;
      width: 100%;
      font-size: 18px;
      cursor: pointer;
      border-radius: 5px;
      color: white;
    }
    button:hover {
      background-color: #ddd;
      color: white;
    }
    #display {
      color: white;
      font-size: 22px;
      font-weight: bold;
      margin-top: 30px;
      display: none;
      text-transform: uppercase;
    }
    #img {
      width: 400px;
      height: auto;
      margin: 20px auto 0;
      display: none;
      border-radius: 8px;
    }
    #img3 {
      width: 420px;
      height: auto;
    }
    label#l1, label#l2 {
      display: block;
      text-align: left;
      margin-bottom: 5px;
      font-weight: bold;
      color: black;
      font
    }
    p#privacy {
      color: light blue;
      font-size: 14px;
      margin-top: 10px;
    }
  footer{
       height: 2px;
       font-size: 0.5px;
       margin-top: -2px
  }
  </style>
  <title>Login Page</title>
</head>
<body>
  <!-- College Image at top -->
  <img src="clg.jpg.jpg" alt="College Image" id="img2" />

  <div id="login">
    <label id="l1" for="name">YOUR USERNAME</label>
    <input type="text" id="name" placeholder="Reg no" autocomplete="off" />
    
    <label id="l2" for="pass">PASSWORD</label>
    <input type="password" id="pass" placeholder="PASSWORD" autocomplete="off" />
    
    <button onclick="login()">Login</button>
    <p id="privacy">Privacy policy & TC</p>
  </div>

  <img src="net.jpg.jpg" alt="Welcome Image" id="img3" />

  <img src="ape.jpg.jpg" alt="Welcome Image" id="img" />

  

  <script>
    function login() {
      let name = document.getElementById("name").value.trim();
      let password = document.getElementById("pass").value;
      const img = document.getElementById("img");
      const box = document.getElementById("login");
      const display = document.getElementById("display");
      const top = document.getElementById("img2");
      const top2 = document.getElementById("img3");
      const truepass = "nicheian@123";

      if (name.length < 5) {
        alert("Username must have at least 5 characters");
        return;
      }
      if (password !== truepass) {
        alert("Incorrect password");
        return;
      }

      box.style.display = "none";
      top.style.display = "none";
      top2.style.display = "none";
      img.style.display = "block";
    }
  </script>
</body>
</html>
