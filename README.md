# Safeguard-bot
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Mini App</title>
  <!-- Load Telegram Web Apps API -->
  <script src="https://telegram.org/js/telegram-webapp.js"></script>
  <script>
    function onLoad() {
      if (window.Telegram && window.Telegram.WebApp) {
        // Notify Telegram that your mini app is ready
        Telegram.WebApp.ready();
        console.log("Telegram WebApp initialized");
      }
    }
    
    // Function to send data back to your bot
    function sendData() {
      if (window.Telegram && window.Telegram.WebApp) {
        // You can customize the data string as needed
        Telegram.WebApp.sendData("User pressed the interactive button!");
        console.log("Data sent to bot");
      }
    }
  </script>
</head>
<body onload="onLoad()">
  <h1>Welcome to My Mini App!</h1>
  <p>This mini app is integrated with Telegram.</p>
  <!-- Interactive Button -->
  <button onclick="sendData()">Press Me!</button>
</body>
</html>
