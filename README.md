# DKV-MARKETING-APP
marketing
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DKV Marketing App</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; background: #f0f2f5; text-align: center; }
        header { background: #002e5d; color: white; padding: 20px; border-radius: 0 0 20px 20px; }
        .card { background: white; margin: 15px; padding: 20px; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .btn { display: block; background: #28a745; color: white; padding: 12px; margin: 10px 0; text-decoration: none; border-radius: 8px; font-weight: bold; border:none; width: 100%; cursor: pointer; }
        .btn-upstox { background: #673ab7; }
        input { width: 90%; padding: 10px; margin: 10px 0; border: 1px solid #ccc; border-radius: 5px; }
    </style>
</head>
<body>

<header>
    <img src="YOUR_DKV_LOGO_LINK" alt="DKV Logo" width="80">
    <h1>DKV Marketing</h1>
    <p>Earn ₹100 Per Account</p>
</header>

<div class="card">
    <h3>Available Tasks</h3>
    <p>Angel One Account Open Karein</p>
    <a href="YOUR_ANGELONE_LINK" class="btn">Open Angel One</a>
    
    <p>Upstox Account Open Karein</p>
    <a href="YOUR_UPSTOX_LINK" class="btn btn-upstox">Open Upstox</a>
</div>

<div class="card" id="submit-section">
    <h3>Submit Details</h3>
    <input type="text" id="userName" placeholder="Apna Naam Likhein">
    <input type="text" id="userUpi" placeholder="UPI ID (e.g. 98765@paytm)">
    <p>Screenshot Upload Karein:</p>
    <input type="file" id="screenshot" accept="image/*">
    <button class="btn" onclick="submitToAdmin()" style="background:#002e5d">Submit for Verification</button>
    <p id="statusMsg" style="color: blue; display: none;">Processing... Please Wait!</p>
</div>

<script>
    function submitToAdmin() {
        const name = document.getElementById('userName').value;
        const upi = document.getElementById('userUpi').value;
        const file = document.getElementById('screenshot').files[0];

        if(name && upi && file) {
            document.getElementById('statusMsg').style.display = "block";
            document.getElementById('statusMsg').innerText = "Submitted! Wait 24-48 Hours.";
            
            // Yahan Firebase logic connect hoga data save karne ke liye
            console.log("Data Sent to DKV Database:", {name, upi, file});
            
            alert("Application Submitted Successfully!");
        } else {
            alert("Please fill all details and upload screenshot!");
        }
    }
</script>

</body>
</html>
