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
/* styles.css */
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yellow Background</title>
</head>
<body style="background-color: yellow;">
    <h1>This page has a yellow background!</h1>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yellow Background</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>This page has a yellow background!</h1>
</body>
</html>
/* styles.css */
body {
    background-color: yellow;
}
