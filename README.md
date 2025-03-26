<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Airplane Booking</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #f4f4f9;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background: #fff;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            font-size: 24px;
            color: #333;
        }
        input, select, button {
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background: #007bff;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background: #0056b3;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Airplane Booking</h1>
        <div id="login-section">
            <h2>Login</h2>
            <input id="email" type="email" placeholder="Email">
            <input id="password" type="password" placeholder="Password">
            <button onclick="login()">Login</button>
        </div>
        <div id="booking-section" class="hidden">
            <h2>Book a Flight</h2>
            <input id="destination" type="text" placeholder="Destination">
            <input id="date" type="date">
            <select id="class">
                <option value="economy">Economy</option>
                <option value="business">Business</option>
                <option value="first">First Class</option>
            </select>
            <h3>Payment Details</h3>
            <input id="card-name" type="text" placeholder="Card Name">
            <input id="card-number" type="text" placeholder="Card Number">
            <input id="expiry" type="text" placeholder="Expiry (MM/YY)">
            <input id="cvv" type="text" placeholder="CVV">
            <button onclick="book()">Book & Pay</button>
        </div>
    </div>

    <script>
        const validUser = { email: "raghuraj@234.com", password: "password123" };

        function login() {
            const email = document.getElementById("email").value;
            const password = document.getElementById("password").value;
            if (email === validUser.email && password === validUser.password) {
                alert("Login Successful!");
                document.getElementById("login-section").classList.add("hidden");
                document.getElementById("booking-section").classList.remove("hidden");
            } else {
                alert("Invalid Credentials");
            }
        }

        function book() {
            const destination = document.getElementById("destination").value;
            const date = document.getElementById("date").value;
            const flightClass = document.getElementById("class").value;
            const cardName = document.getElementById("card-name").value;
            const cardNumber = document.getElementById("card-number").value;
            const expiry = document.getElementById("expiry").value;
            const cvv = document.getElementById("cvv").value;

            if (destination && date && flightClass && cardName && cardNumber && expiry && cvv) {
                alert(`Flight booked successfully!\nDestination: ${destination}\nDate: ${date}\nClass: ${flightClass}\nPayment by: ${cardName}`);
            } else {
                alert("Please fill all fields.");
            }
        }
    </script>
</body>
</html>
