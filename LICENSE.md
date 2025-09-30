<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Profile</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      color: white;
      text-align: center;
      background: url("dexter-logo.png") no-repeat center center fixed;
      background-size: cover;
      backdrop-filter: blur(8px);
    }

    header {
      display: flex;
      align-items: center;
      padding: 20px;
    }

    header img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 3px solid white;
      margin-right: 20px;
    }

    h1 {
      font-size: 2.5em;
    }

    section {
      background: rgba(0, 0, 0, 0.6);
      margin: 20px auto;
      padding: 20px;
      border-radius: 12px;
      width: 80%;
    }

    .logos img {
      width: 80px;
      margin: 10px;
    }

    #countdown {
      font-size: 2em;
      margin-top: 20px;
      color: #ffcc00;
    }

    .decor {
      position: fixed;
      bottom: 10px;
      right: 10px;
      width: 120px;
    }

    .soccer-legends img {
      width: 200px;
      margin: 15px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <img src="profile.jpg" alt="My Picture">
    <h1>Welcome to My Website</h1>
  </header>

  <!-- Schedule -->
  <section>
    <h2>My School Schedule</h2>
    <img src="schedule.png" alt="My Schedule" style="width:100%; border-radius: 10px;">
  </section>

  <!-- After school activities -->
  <section>
    <h2>After School Activities</h2>
    <p>⚽ Soccer Practice - Monday & Wednesday at 4:00 PM</p>
    <p>⚽ Soccer Practice - Friday at 4:45 PM</p>
  </section>

  <!-- Logos -->
  <section class="logos">
    <h2>My Favorite Teams</h2>
    <img src="celtics.png" alt="Celtics Logo">
    <img src="redsox.png" alt="Red Sox Logo">
    <img src="realmadrid.png" alt="Real Madrid Logo">
  </section>

  <!-- Soccer Legends -->
  <section class="soccer-legends">
    <h2>Soccer Legends</h2>
    <img src="ronaldo.jpg" alt="Cristiano Ronaldo">
    <img src="kaka.jpg" alt="Kaká">
  </section>

  <!-- Countdown -->
  <section>
    <h2>Countdown to Summer</h2>
    <div id="countdown"></div>
  </section>

  <!-- Sour Patch Kid decoration -->
  <img src="sourpatch.png" alt="Sour Patch Kid" class="decor">

  <script>
    // Countdown Timer
    const endDate = new Date("June 10, 2026 15:00:00").getTime();

    function updateCountdown() {
      const now = new Date().getTime();
      const distance = endDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));

      document.getElementById("countdown").innerHTML = days + " days left until school ends!";
    }

    setInterval(updateCountdown, 1000);
    updateCountdown();
  </script>
</body>
</html>
