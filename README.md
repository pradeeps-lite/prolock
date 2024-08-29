# prolock
#Junk tool Software Frontend
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Junk-Free Notification</title>
    <style>
        /* Basic Reset */
        body, html {
            height: 100%;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            background: url('https://t3.ftcdn.net/jpg/03/36/78/98/360_F_336789869_HaIcJqwCgarVu2mQR09GPTQcIPF3ZeJg.jpg') no-repeat center center/cover;
            color: white;
        }

        /* Center the content */
        #content {
            text-align: center;
            max-width: 500px;
        }

        /* Loading Section */
        #loading {
            text-align: center;
            font-size: 24px;
            font-weight: 600; /* Semi-bold */
            color: #00ff00; /* Neon green */
        }

        /* Spinner icon */
        .spinner {
            border: 8px solid #f3f3f3; /* Light grey */
            border-top: 8px solid #00ff00; /* Green */
            border-radius: 50%;
            width: 70px;
            height: 70px;
            animation: spin 1.5s linear infinite;
            margin-bottom: 20px;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Success Message Section */
        #message {
            font-size: 36px; /* Big Font */
            font-weight: bold;
            display: none; /* Hide the message initially */
            color: #00ff00; /* Neon green */
            text-align: center;
        }

        /* Medium Big Tick Icon */
        #tick-icon {
            width: 120px;
            margin: 20px auto;
            display: none; /* Hide the tick initially */
        }

        /* Big Mobile Phone Icon */
        #mobile-icon {
            width: 80px;
            margin: 20px auto;
            display: none; /* Hide the phone icon initially */
        }

        /* Disclaimer Section */
        #disclaimer {
            font-size: 20px;
            font-weight: 600; /* Semi-bold */
            color: #ffcc00; /* Yellow color for contrast */
            display: none; /* Hide the disclaimer initially */
            margin-top: 30px;
        }

        #disclaimer-icon {
            width: 30px;
            vertical-align: middle;
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <!-- Main Content Container -->
    <div id="content">
        <!-- Loading message with spinner -->
        <div id="loading">
            <div class="spinner"></div>
            <p>Loading, please wait...</p>
        </div>
        
        <!-- Success message with tick and mobile phone icon -->
        <div id="message">
            <img id="tick-icon" src="https://img.icons8.com/color/120/000000/checkmark.png" alt="Success Tick">
            <p>YOUR DEVICE IS NOW SUCCESSFULLY JUNK FREE</p>
            <img id="mobile-icon" src="https://img.icons8.com/ios-filled/100/00ff00/iphone-x.png" alt="Mobile Phone">
        </div>

        <!-- Disclaimer Section -->
        <div id="disclaimer">
            <img id="disclaimer-icon" src="https://img.icons8.com/ios-filled/50/ffcc00/warning-shield.png" alt="Disclaimer Icon">
            <span>Be Safe</span>
        </div>
    </div>

    <script>
        // Set a timeout for 4 seconds (4000 milliseconds)
        setTimeout(function() {
            // Hide the loading message
            document.getElementById('loading').style.display = 'none';
            // Show the tick icon, mobile phone icon, and success message
            document.getElementById('tick-icon').style.display = 'block';
            document.getElementById('mobile-icon').style.display = 'block';
            document.getElementById('message').style.display = 'block';
            // Show the disclaimer at the bottom
            document.getElementById('disclaimer').style.display = 'block';
        }, 4000); // 4 seconds
    </script>
</body>
</html>
