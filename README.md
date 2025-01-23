<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Book Portal</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Digital Book Portal</h1>
        <div class="form-container">
            <form id="login-form">
                <h2>Login</h2>
                <input type="text" id="login-username" placeholder="Username" required>
                <input type="password" id="login-password" placeholder="Password" required>
                <button type="submit">Login</button>
            </form>
            <form id="signup-form">
                <h2>Sign Up</h2>
                <input type="text" id="signup-username" placeholder="Username" required>
                <input type="email" id="signup-email" placeholder="Email" required>
                <input type="password" id="signup-password" placeholder="Password" required>
                <input type="password" id="signup-confirm-password" placeholder="Confirm Password" required>
                <button type="submit">Sign Up</button>
            </form>
        </div>
        <div class="search-container">
            <input type="text" id="search-bar" placeholder="Search for books...">
            <button id="search-button">Search</button>
        </div>
        <div id="qr-code-container">
            <h2>Your QR Code</h2>
            <div id="qr-code"></div>
        </div>
    </div>
    <script src="app.js"></script>
</body>
</html>
/* styles.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;

.container {
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    color: #333;
}

.form-container {
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
}

form {
    width: 48%;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
}

form h2 {
    margin-top: 0;
}

input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
}

button {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

.search-container {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
}

#search-bar {
    width: 70%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
}

#search-button {
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    background-color: #28a745;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
}

#search-button:hover {
    background-color: #218838;
}

#qr-code-container {
    text-align: center;
}

#qr-code {
    margin-top: 20px;
}
// app.js

document.getElementById('login-form').addEventListener('submit', function(event) {
    event.preventDefault();
    // Handle login logic here
    alert('Logged in successfully!');
});

document.getElementById('signup-form').addEventListener('submit', function(event) {
    event.preventDefault();
    const password = document.getElementById('signup-password').value;
    const confirmPassword = document.getElementById('signup-confirm-password').value;
    if (password === confirmPassword) {
        // Handle sign-up logic here
        alert('Signed up successfully!');
    } else {
        alert('Passwords do not match!');
    }
});

document.getElementById('search-button').addEventListener('click', function() {
    const query = document.getElementById('search-bar').value;
    // Handle search logic here
    alert('Searching for: ' + query);
});

// QR Code generation (using a library like QRCode.js)
const qrCodeContainer = document.getElementById('qr-code');
const qrCode = new QRCode(qrCodeContainer, {
    text: "https://example.com",
    width: 128,
    height: 128,
    colorDark: "#000000",
    colorLight: "#ffffff",
});
