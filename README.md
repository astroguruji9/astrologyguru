# astrologyguru
Astrology numberlogy consultant get your solution get yours zudioc here 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>AstrologyGuru – Vedic Astrology & Kundli</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #faf7f0;
            color: #333;
        }
        header {
            background: #b30000;
            color: #fff;
            padding: 20px;
            text-align: center;
            font-size: 28px;
            font-weight: bold;
        }
        nav {
            background: #fff;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            padding: 12px;
            border-bottom: 2px solid #ddd;
        }
        nav a {
            text-decoration: none;
            color: #b30000;
            font-weight: 600;
            padding: 8px 12px;
            border-radius: 6px;
        }
        nav a:hover {
            background: #f2c2c2;
        }
        .hero {
            padding: 40px 20px;
            background: url('https://i.imgur.com/ogwK4S9.jpeg');
            background-size: cover;
            background-position: center;
            color: white;
            text-shadow: 0 0 6px black;
            text-align: center;
        }
        .hero h1 { font-size: 36px; }
        .section {
            padding: 20px 15px;
            max-width: 1000px;
            margin: auto;
        }
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }
        .card {
            background: #fff;
            padding: 15px;
            border-radius: 12px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            text-align: center;
        }
        .pay-box {
            padding: 20px;
            background: #fff3e0;
            border-radius: 10px;
            text-align: center;
            margin-top: 20px;
        }
        .upi-btn {
            display: block;
            width: 100%;
            margin-top: 10px;
            padding: 12px;
            background: #b30000;
            color: #fff;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
        }
        input, select {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border-radius: 6px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        label {
            font-weight: bold;
        }
        .booking-btn {
            background: #b30000;
            color: #fff;
            border: none;
            padding: 12px;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            margin-top: 10px;
        }
        @media(max-width:600px){
            .hero h1 { font-size: 28px; }
            nav { gap: 8px; }
            .card-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <header>AstrologyGuru – Vedic Astrology</header>

    <nav>
        <a href="#kundli">Kundli</a>
        <a href="#horoscope">Horoscope</a>
        <a href="#consult">Consult</a>
        <a href="#payment">Payment</a>
    </nav>

    <div class="hero">
        <h1>Your Trusted Vedic Astrology Platform</h1>
        <p>Daily Horoscope • Kundli • Numerology • Palm Reading • Remedies</p>
    </div>

    <div class="section" id="kundli">
        <h2>Generate Free Kundli</h2>
        <div class="card-grid">
            <div class="card">Janam Kundli</div>
            <div class="card">Kundli Matching</div>
            <div class="card">Numerology Report</div>
            <div class="card">Vastu Consultation</div>
        </div>
    </div>

    <div class="section" id="horoscope">
        <h2>Today's Horoscope</h2>
        <div class="card-grid">
            <div class="card">Aries</div>
            <div class="card">Taurus</div>
            <div class="card">Gemini</div>
            <div class="card">Cancer</div>
        </div>
    </div>

    <div class="section" id="consult">
        <h2>Talk to Astrologer</h2>
        <p>Choose your preferred consultation type:</p>
        <div class="card-grid">
            <div class="card">
                <h3>Chat Consultation</h3>
                <p>Instant chat with expert astrologers</p>
                <strong>₹299 / 15 minutes</strong>
            </div>
            <div class="card">
                <h3>Call Consultation</h3>
                <p>Voice call for detailed guidance</p>
                <strong>₹399 / 20 minutes</strong>
            </div>
        </div>
        <br>
        <h3>Book Your Session & Pay</h3>
        <form class="pay-box" id="bookingForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>

            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" required>

            <label for="type">Consultation Type:</label>
            <select id="type" name="type" required>
                <option value="chat">Chat – ₹299</option>
                <option value="call">Call – ₹399</option>
            </select>

            <label for="date">Preferred Date:</label>
            <input type="date" id="date" name="date" required>

            <label for="time">Preferred Time:</label>
            <input type="time" id="time" name="time" required>

            <button type="submit" class="booking-btn">Book & Pay Now</button>
        </form>
    </div>

    <div class="section" id="payment">
        <h2>Secure UPI Payment</h2>
        <div class="pay-box">
            <p>Choose any Indian UPI App:</p>

            <a class="upi-btn" id="gpayBtn" href="#">Pay with Google Pay</a>
            <a class="upi-btn" id="phonepeBtn" href="#">Pay with PhonePe</a>
            <a class="upi-btn" id="paytmBtn" href="#">Pay with Paytm UPI</a>
        </div>
    </div>

    <script>
        const form = document.getElementById('bookingForm');
        const gpayBtn = document.getElementById('gpayBtn');
        const phonepeBtn = document.getElementById('phonepeBtn');
        const paytmBtn = document.getElementById('paytmBtn');

        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const type = document.getElementById('type').value;
            let amount = 0;
            if(type === 'chat') amount = 299;
            else if(type === 'call') amount = 399;

            // Update payment links with selected amount
            const upiId = 'YOUR_UPI_ID'; // Replace with your UPI ID
            gpayBtn.href = `upi://pay?pa=${upiId}&pn=AstrologyGuru&am=${amount}&cu=INR`;
            phonepeBtn.href = `upi://pay?pa=${upiId}&pn=AstrologyGuru&am=${amount}&cu=INR`;
            paytmBtn.href = `upi://pay?pa=${upiId}&pn=AstrologyGuru&am=${amount}&cu=INR`;

            alert('Booking recorded! Please choose a UPI app below to pay ₹' + amount);
            window.location.href = '#payment';
        });
    </script>

</body>
</html>
