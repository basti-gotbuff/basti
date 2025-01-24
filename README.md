        <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sum-ag National High School Digital Library</title>
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
from PIL import Image, ImageDraw
import qrcode

# Create a yellow background image
width, height = 300, 300
yellow_background = Image.new('RGB', (width, height), color='yellow')

# Generate a QR code
qr = qrcode.QRCode(version=1, error_correction=qrcode.constants.ERROR_CORRECT_L, box_size=10, border=4)
qr.add_data('https://www.example.com')
qr.make(fit=True)
qr_code = qr.make_image(fill_color="black", back_color="yellow")

# Overlay the QR code onto the yellow background
qr_code = qr_code.resize((150, 150))
yellow_background.paste(qr_code, (75, 75))

# Save the final image
yellow_background.save('yellow_background_with_qr.png')
yellow_background.show()

