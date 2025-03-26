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
