# milka-apartments-<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kwa Milka Apartments Portal</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f6f8;
    }
    header {
      background: #1f3a5f;
      color: white;
      padding: 15px;
      text-align: center;
    }
    .container {
      padding: 20px;
    }
    .card {
      background: white;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .notice-title {
      font-weight: bold;
      color: #1f3a5f;
    }
    .login {
      max-width: 300px;
      margin: 100px auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      text-align: center;
    }
    input {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      background: #1f3a5f;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body><div id="loginPage" class="login">
  <h2>Kwa Milka Apartments</h2>
  <p>Resident Login</p>
  <input type="text" id="username" placeholder="Enter your name">
  <br>
  <button onclick="login()">Login</button>
</div><div id="portal" style="display:none;">
  <header>
    <h2>Kwa Milka Apartments Portal</h2>
    <p id="welcome"></p>
  </header>  <div class="container"><div class="card">
  <div class="notice-title">Water Maintenance Notice</div>
  <p>Water will be unavailable on Wednesday from 10 AM to 2 PM.</p>
</div>

<div class="card">
  <div class="notice-title">Security Update</div>
  <p>Please ensure the gate is locked at all times.</p>
</div>

<div class="card">
  <div class="notice-title">Rent Reminder</div>
  <p>All tenants are reminded to pay rent before the 5th.</p>
</div>

  </div>
</div><script>
  function login() {
    var name = document.getElementById('username').value;
    if(name === '') {
      alert('Please enter your name');
      return;
    }
    document.getElementById('loginPage').style.display = 'none';
    document.getElementById('portal').style.display = 'block';
    document.getElementById('welcome').innerText = 'Welcome, ' + name;
  }
</script></body>
</html>
