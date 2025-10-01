# newtours<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Tours and Travel Website</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background-color: #f0f8ff; /* light sky blue background */
    margin: 0;
    padding: 0;
    color: #333;
  }
  header {
    background-color: #87ceeb; /* sky blue */
    color: white;
    padding: 20px;
    text-align: center;
    font-size: 24px;
  }
  nav {
    background-color: #87ceeb;
    display: flex;
    justify-content: center;
    gap: 40px;
    padding: 15px 0;
  }
  nav button {
    background-color: white;
    border: none;
    padding: 12px 25px;
    border-radius: 5px;
    color: #87ceeb;
    cursor: pointer;
    font-weight: bold;
  }
  nav button:hover {
    background-color: #b0e0ff;
  }
  main {
    max-width: 900px;
    margin: 20px auto;
    background-color: white;
    border: 2px solid #87ceeb;
    padding: 20px;
  }
  /* Advertisement banner styling in middle */
  .ad-display {
    background-color: white;
    margin: 20px 0;
    padding: 15px;
    border: 2px solid #87ceeb;
    text-align: center;
    font-weight: bold;
  }
  section {
    margin-bottom: 25px;
  }
  .sub-section {
    margin-left: 20px;
    border-left: 3px solid #87ceeb;
    padding-left: 10px;
  }
  .back-btn {
    background-color: #87ceeb;
    color: white;
    border: none;
    border-radius: 5px;
    padding: 10px 18px;
    cursor: pointer;
    font-weight: bold;
    margin-bottom: 15px;
  }
  .whatsapp-link {
    display: inline-block;
    margin-top: 15px;
    background-color: #25d366;
    color: white;
    padding: 10px 18px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    font-size: 14px;
  }
  .whatsapp-link:hover {
    background-color: #1ebe57;
  }
  /* Dashboard styling */
  #dashboard {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }
  .dashboard-card {
    border: 2px solid #87ceeb;
    border-radius: 8px;
    padding: 20px;
    width: 250px;
    background-color: #f9fcff;
    text-align: center;
    cursor: pointer;
    font-weight: bold;
    color: #87ceeb;
    transition: background-color 0.3s, color 0.3s;
  }
  .dashboard-card:hover {
    background-color: #87ceeb;
    color: white;
  }
</style>
</head>
<body>
<header>
  Tours and Travel Website
</header>

<nav>
  <button onclick="showSection('tours')">Tours</button>
  <button onclick="showSection('rooms')">Rooms (Homestay)</button>
  <button onclick="showSection('travel')">Travel</button>
</nav>

<main>
  <section id="dashboard">
    <div class="dashboard-card" onclick="showSection('tours')">Tours</div>
    <div class="dashboard-card" onclick="showSection('rooms')">Rooms (Homestay)</div>
    <div class="dashboard-card" onclick="showSection('travel')">Travel</div>
  </section>

  <div class="ad-display">
    Advertisement / Promotional Banner
  </div>

  <section id="tours" style="display:none;">
    <button class="back-btn" onclick="showDashboard()">Back to Dashboard</button>
    <h2>Tours</h2>
    <div class="sub-section">
      <h3>My Tours</h3>
      <p>Display planned tours here.</p>
      <a class="whatsapp-link" href="https://wa.me/919876543210?text=Hello%20I%20want%20details%20about%20Tours" target="_blank" rel="noopener noreferrer">Contact Tours Person via WhatsApp</a>
    </div>
    <div class="sub-section">
      <h3>Regular Tours & Packages</h3>
      <ul>
        <li>Kerala</li>
        <li>Goa</li>
        <li>Mumbai</li>
        <li>Others...</li>
      </ul>
    </div>
  </section>

  <section id="rooms" style="display:none;">
    <button class="back-btn" onclick="showDashboard()">Back to Dashboard</button>
    <h2>Rooms (Homestay)</h2>
    <p>Location-based rooms display here.</p>
    <a class="whatsapp-link" href="https://wa.me/919812345678?text=Hello%20I%20want%20details%20about%20Rooms%20(Homestay)" target="_blank" rel="noopener noreferrer">Contact Rooms Person via WhatsApp</a>
  </section>

  <section id="travel" style="display:none;">
    <button class="back-btn" onclick="showDashboard()">Back to Dashboard</button>
    <h2>Travel</h2>
    <div class="sub-section">
      <h3>Vehicles</h3>
      <ul>
        <li>Car</li>
        <li>Van</li>
        <li>Volvo Bus</li>
        <li>Mini Bus</li>
      </ul>
    </div>
    <div class="sub-section">
      <h3>Tickets</h3>
      <ul>
        <li>Train</li>
        <li>Bus</li>
        <li>Flight</li>
        <li>Others...</li>
      </ul>
    </div>
    <a class="whatsapp-link" href="https://wa.me/919898989898?text=Hello%20I%20want%20details%20about%20Travel%20options" target="_blank" rel="noopener noreferrer">Contact Travel Person via WhatsApp</a>
  </section>
</main>

<script>
  function showSection(sectionId) {
    // Hide all sections
    document.querySelectorAll('main section').forEach(sec => sec.style.display = 'none');
    // Show selected section
    document.getElementById(sectionId).style.display = 'block';
    // Hide ad display when showing a section
    document.querySelector('.ad-display').style.display = 'none';
  }

  function showDashboard() {
    // Hide all sections
    document.querySelectorAll('main section').forEach(sec => sec.style.display = 'none');
    // Show dashboard
    document.getElementById('dashboard').style.display = 'flex';
    // Show ad display in dashboard
    document.querySelector('.ad-display').style.display = 'block';
  }

  // Show dashboard on page load
  document.addEventListener('DOMContentLoaded', () => {
    showDashboard();
  });
</script>
</body>
</html>
